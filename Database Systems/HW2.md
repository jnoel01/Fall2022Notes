# HW2

***QUERY 1***

```sql
/*QUERY 1*/

with q1 as (
    select cust, prod, month, state, quant
    from sales
),

q2 as (
    select q1.month, q1.state, avg(q1.quant) as CUST_AVG
    from q1
    group by q1.month, q1.state
),

q3 as(
    select q1.month, q1.state, avg(q1.quant) as OTHER_PROD_AVG
    from q1, sales
    where q1.prod != sales.prod
    group by q1.month, q1.state
),

q4 as(
    select q1.prod, q1.state, avg(q1.quant) as OTHER_MONTH_AVG
    from q1, sales
    where q1.month != sales.month
    group by q1.prod, q1.state
),

q5 as (
    select q1.prod, q1.month, avg(q1.quant) as OTHER_STATE_AVG
    from q1, sales
    where q1.state != sales.state
    group by q1.prod, q1.month
)

select distinct(q1.cust) as CUSTOMER, q1.prod as PRODUCT, q1.month, q1.state, round(CUST_AVG, 3) as CUST_AVG, round(OTHER_PROD_AVG, 3) as OTHER_PROD_AVG, round(OTHER_MONTH_AVG, 3) as OTHER_MONTH_AVG, round(OTHER_STATE_AVG, 3) as OTHER_STATE_AVG
from q1, q2, q3, q4, q5
where q1.prod = q4.prod and q1.prod = q5.prod and q1.month = q2.month and q1.month = q3.month and q1.month = q5.month and q1.state = q2.state and q1.state = q3.state and q1.state = q4.state
group by q1.cust, q1.prod, q1.month, q1.state, CUST_AVG, OTHER_PROD_AVG, OTHER_MONTH_AVG, OTHER_STATE_AVG
```

*********************QUERY 2*********************

```sql
/* QUERY 2*/

with q1 as (
  select cust, prod, month, state, quant, extract(month from date) as dt_mon
  from sales
),

q2 as (
  select cust, prod, state, dt_mon, avg(quant) avgq
  from q1
  group by cust, prod, state, dt_mon
),

q3 as (
  select q2.cust, q2.prod, q2.state, q2.dt_mon, x.avgq avgb
  from q2
  join q2 as x on q2.cust = x.cust and q2.prod = x.prod and q2.state = x.state 
    and x.dt_mon = (q2.dt_mon - 1)
),

q4 as (
  select q3.cust, q3.prod, q3.state, q2.dt_mon, 
    case when q2.dt_mon = 1 then null else q3.avgb end avgb
  from q2
  join q3 on q2.cust = q3.cust and q2.prod = q3.prod and q2.state = q3.state
  where q3.dt_mon = q2.dt_mon or q2.dt_mon = 1
),

q5 as (
  select cust, prod, state, dt_mon, cast(null as numeric) avgb
  from q1
  where dt_mon = 1
  group by cust, prod, state, dt_mon
),

q6 as (
  select * from q3 
  union 
  select * from q5
),

q7 as (
  select q2.cust, q2.prod, q2.state, q2.dt_mon, x.avgq after_avg
  from q2
  join q2 as x on x.dt_mon = (q2.dt_mon + 1) 
    and q2.cust = x.cust and q2.prod = x.prod and q2.state = x.state
), 

q8 as (
  select cust, prod, state, dt_mon, cast(null as numeric) after_avg
  from q1
  where dt_mon = 12
  group by cust, prod, state, dt_mon
),

q9 as (
  select * 
  from q7
  union
  select * 
  from q8
)

select q6.cust as CUSTOMER, q6.prod as PRODUCT, q6.state, q6.dt_mon as MO, round(q6.avgb, 3) as BEFORE_AVERAGE, round(q9.after_avg, 3) as AFTER_AVG
from q6
join q9 on q6.cust = q9.cust and q6.prod = q9.prod and q6.state = q9.state and q6.dt_mon = q9.dt_mon 
group by q6.cust, q6.prod, q6.state, q6.dt_mon, round(q6.avgb, 3), round(q9.after_avg, 3)
```

*********************QUERY 3*********************

```sql

/*QUERY 3*/

with q1 as(
    select distinct(prod), quant as MEDIAN_QUANT
    from sales
),

q2 as (
    select row_number() over() as TROWS, PROD, MEDIAN_QUANT
    from q1
),

q3 as (
    select prod as PRODUCT, count(MEDIAN_QUANT)/2 as COUNTS
    from q1
    group by PRODUCT
)

select PRODUCT, MEDIAN_QUANT
from q2, q3
where COUNTS = TROWS
group by PRODUCT, MEDIAN_QUANT
```

*********************QUERY 4*********************

```sql
/* Query 4 */

with q1 as (
  select cust, prod, month, quant
  from sales
),

q2 as (
  select cust, prod, sum(quant) as TOTAL
  from q1
  group by cust, prod
),

q3 as (
  select cust, prod, month, sum(quant) as TOTAL
  from q1
  group by cust, prod, month
),

q4 as (
  select q3.cust, q3.prod, q3.month, sum(y.total) as QUANT_MONTH
  from q3
  inner join q3 as y
  on q3.cust = y.cust and q3.prod = y.prod and q3.month >= y.month
  group by q3.cust, q3.prod, q3.month
)

    select q4.cust as CUSTOMER, q4.prod as PRODUCT, min(q4.month) as "75%_purchased_by_month"
    from q2
    inner join q4
    on q4.cust = q2.cust and q4.prod = q2.prod and q4.quant_month >= q2.total * (0.75)
    group by CUSTOMER, PRODUCT
```

/