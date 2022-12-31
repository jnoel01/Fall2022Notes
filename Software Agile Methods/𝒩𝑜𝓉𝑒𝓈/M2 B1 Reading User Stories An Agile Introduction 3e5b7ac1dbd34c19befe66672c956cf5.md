# M2.B1: Reading: User Stories: An Agile Introduction

[https://webspace.science.uu.nl/~dalpi001/papers/luca-dalp-werf-brin-15-re.pdf](https://webspace.science.uu.nl/~dalpi001/papers/luca-dalp-werf-brin-15-re.pdf)

## ***NOTES***

- user stories only capture the essential elements of a requirement: who it is for, what it expects from the system, and, optionally, why it is important

![https://i.gyazo.com/c47fc0dd9183c398b6d7358355fb6d58.png](https://i.gyazo.com/c47fc0dd9183c398b6d7358355fb6d58.png)

- Example of User Stories that Breach Quality Criteria
    - “*As a User, I’m able to click a particular location from the map and thereby perform a search of landmark associated with that latitude and longitude combination”* This example is not atomic: two stories in one
    - “*Add static pages controller to application and define static pages”*  Missing Role

- Minimal: User stories should contain a role, means
and, optionally, ends. Nothing more.

- Well-formed: Before it can be considered a user story,
the core requirements text needs to define a role and what the
expected functionality entails

- Conflict-free: To prevent implementation errors and
rework, a user story should not conflict with any of the
other user stories in the database.

- Problem-oriented: A user story should only specify
the problem, not the solution.

- Unambiguous: Ambiguity is inherent to natural language requirements, but the requirements engineer writing user
stories should avoid it as much as possible.

- Complete: Implementing a set of user stories should
create a feature-complete application.

- Explicit dependencies: Whenever a user story has
a non-obvious dependency, it should explicitly link to the
user story tag of the user story it depends on.

- Full sentence: A user story should read like a full
sentence, without typos or hindering grammatical errors.

- Independent: User stories should not overlap in concept and should be schedulable and implementable in any
order.

- Scalable: As user stories grow in size, it becomes
more difficult to accurately estimate the effort required for the
entire set of user stories. Therefore, each user story should
not become so large as to avoid their estimation and planning
with reasonable certainty.

- Uniform: All user stories should follow the same,
agreed upon template. Minimal deviations are allowed when
this better suits the narrative structure of the user story.

- Unique: A user story should not be a duplicate of
another user story nor epic.

- An **epic** is a label for a large user story,
which is broken down into smaller, implementable user stories.

- A **theme** is a collection of user stories grouped according to
a given criterion

- A user story should follow some pre-defined template as
agreed upon among the stakeholders.

- A user story always defines one relevant role

- We define three possible variants of a well-formed end:
    1. **Clarification of means:** The end explains the reason of the
    means. Example: “As a User, I want to edit a record, so
    that I can correct any mistakes”.
    2. **Dependency on another (hidden) functionality:** Small example: “As a Visitor, I want to view the homepage, so that I can learn about the project”.
    3. **Qualitative requirement:** For example: “As a User, I want to sort the results, so that I can more easily review the results” indicates that the means contributes maximizing easiness