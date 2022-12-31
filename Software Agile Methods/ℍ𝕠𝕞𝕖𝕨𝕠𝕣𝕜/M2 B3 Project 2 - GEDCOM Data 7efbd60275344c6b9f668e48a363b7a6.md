# M2.B3: Project 2 - GEDCOM Data

```markdown
Assignment:

Since the project teams will not be formed until after this assignment is due,
you will need to do this project assignment on your own. Create a small GEDCOM 
file to use in testing your program. You may reuse the file you submitted for assignment Project 1 or create a new one. Make sure that it includes a NOTE record at the beginning with your name.

Using Python or Visual Basic, write a short program that:

Reads each line of a GEDCOM file

Prints "--> <input line>"

Prints "<-- <level>|<tag>|<valid?> : Y or N|<arguments>"

<level> is the level of the input line, e.g. 0, 1, 2

<tag> is the tag associated with the line, e.g. 'INDI', 'FAM', 'DATE', ...

<valid?> has the value 'Y' if the tag is one of the supported tags or 'N' otherwise. The set of all valid tags for our project is specified in the Project Overview  Download Project Overviewdocument.

<arguments> is the rest of the line beyond the level and tag.

Sample input:

0 NOTE dates after now

1 SOUR Family Echo

2 WWW http://www.familyecho.com (Links to an external site.)

0 bi00 INDI

1 NAME Jimmy /Conners/

Sample output:

--> 0 NOTE dates after now

<-- 0|NOTE|Y|dates after now

--> 1 SOUR Family Echo

<-- 1|SOUR|N|Family Echo

--> 2 WWW http://www.familyecho.com (Links to an external site.) (Links to an external site.)

<-- 2|WWW|N|http://www.familyecho.com (Links to an external site.)

--> 0 bi00 INDI

<-- 0|INDI|Y|bi00

--> 1 NAME Jimmy /Conners/

<-- 1|NAME|Y|Jimmy /Conners/

Caution: Most of the GEDCOM lines have the format

<level> <tag> <arguments>

e.g. 

1 CHIL

1 NAME Jim /Rowland/

2 DATE 31 JAN 2017

There are two exceptions to this rule:

0 <id> INDI

0 <id> FAM

Note that for INDI and FAM tags, the tag is the third token, rather than the second token for most tags.

Caution:

Some online tools include tags that you don't need to support for our project and may cause confusion for your code. Specifically, we are NOT supporting

1 DATE # 2 DATE is supported but not 1 DATE

2 NAME # 1 NAME is supported but not 2 NAME

You'll find a complete list of tags that you'll need to support in the Project Overview  Download Project Overview.

Deliverables:

Submit your program source code, your test GEDCOM file, and the output of your program to the Project 2 Canvas assignment.

Note that you should not include an executable program or instructions on how to create one in your submission. You will execute your program and demonstrate the results to the instructor (playing the role of customer). However, the instructor will review your source code and its history of modification throughout the project. I may also choose to run your code and compare it against the output of my solution for the GEDCOM user stories.
```

[Output.txt](M2%20B3%20Project%202%20-%20GEDCOM%20Data%207efbd60275344c6b9f668e48a363b7a6/Output.txt)

[parser.py](M2%20B3%20Project%202%20-%20GEDCOM%20Data%207efbd60275344c6b9f668e48a363b7a6/parser.py)

[tree.ged](M2%20B3%20Project%202%20-%20GEDCOM%20Data%207efbd60275344c6b9f668e48a363b7a6/tree.ged)

```python
#Jessica Noel
# September 18, 2022
#CS-555 Agile Methods for Software Development

with open("/Users/jessica/Desktop/School/CS-555/M2.B3 Project 2/tree.ged") as f:
    lines = f.readlines()

#List of all supported tags including start, note, end
valid_tags =["TRLR", "HEAD", "NOTE", "SEX", "BIRT", "DEAT", "FAMC", "FAMS","MARR", "HUSB", "WIFE", "CHIL","DIV"]

for line in lines:
    sepLine = line.split()

    #Checks if tag is supported, if yes Y, if not N
    if (sepLine[1] in valid_tags):
        validTag = "Y"

    #Cover the two excpetions, for when INDI and FAM are 3rd token/second index
    elif (len(sepLine) == 3):
        if ((sepLine[2] == "INDI") or (sepLine[2] == "FAM")):
            sepLine[1] = sepLine[2]
            validTag = "Y"

    #Cover 2 DATE, but not 1 DATE
    elif ((sepLine[0] == "2") and (sepLine[1] == "DATE")):
        validTag = "Y"
    
    #Cover 1 NAME, but not 2 NAME
    elif ((sepLine[0] == "1") and (sepLine[1] == "NAME")):
        validTag = "Y"
    
    #All other variations are not supported or valid
    else:
        validTag = "N"

    args = ""
    for x in sepLine[2:len(sepLine)]:
        args += (x + " ")

    print("--> " + line)
    print("<-- " + sepLine[0] + "|" + sepLine[1] + "|" + validTag + "|" + args + "\n")

f.close()
```