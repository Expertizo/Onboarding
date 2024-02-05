# Refactoring


### Table of Contents
1. Definition
2. Why should we refactor?
3. When should we refactor?
4. Types of refactoring
5. When should I not refactor?
6. Two Hats


## 1. Definition

Refactoring could be defined as a "change internal structure of software to make it easier to understand and cheaper to modify without changing observable behavior"

In terms of actions, the task of refactoring could be described as a process to "apply small behavior-preserving steps and make a big change by stringing together a sequence of these steps"


## 2. Why should we refactor?

### 2.1 Refactoring Improves the Design of Software

- People generally change code to achieve short term goals
- There tends to be less focus on architecture during that time
- So, the code loses structure slowly but certainly overtime
- Regular refactoring is a way to keep structure of code and make the design robust


### 2.2 Refactoring Makes Software Easier to Understand

- When working on a problem, we're not thinking of future readability of the code
- We spend more time reading code than writing code, so it's quite important to make it easier for others to read the function
- Refactoring makes it easy to read code (for future)


### 2.3 Refactoring Helps Find Bugs

- Refactoring helps us understand code
- It helps to clarify our assumptions which is a really good thing to have done before working on a codebase
- If bugs are present, refactoring brings them to spotlight


### 2.4 Refactoring Helps Program Faster

- Poor design in codebase will mean that the development pace slows down with time
- With good design of the software, development pace can be maintained or even increased with re-use of components
- Refactoring, in addition to the definitions, is a mechanism to move poor design to good design
- If this is successful, we can go on to make the development easier and make the code stay in active development faster for longer


## 3. When should we refactor?

Sometimes we tend to follow DRY principles too strictly when working in refactoring.
We try to eliminate any duplication of logic and vigorously clean them out.
However, that might not always be the best idea, since these two sections of code could diverge as quickly as they appeared.


*The Rule of Three:*

The first time you do something, you just do it. The second time you do something similar, you wince at the duplication, but you do the duplicate thing anyway. The third time you do something similar, you refactor.
For those who like baseball: Three strikes, then you refactor.


## 4. Types of Refactoring

### 4.1 Preparatory Refactoring: Making It Easier to Add a Feature

- If the code were structured a bit different, the feature would be easier to implement
- Refactor first, then implement the feature
- https://twitter.com/KentBeck/status/250733358307500032

This also has a lot less chance to letting some bug slip through since smaller PRs can be reviewed much more rigorously.


### 4.2 Comprehension Refactoring: Making Code Easier to Understand

- Before adding a feature, we need to understand fully how the code behaves.
- Refactor code to make it more understandable
- We can implement the feature once we understand how the code works


### 4.3 Litter-Pickup Refactoring

- I understand how the code works but realize that it's doing it badly
- It's not exactly necessary to refactor
- If it takes small effort, do it right away
- If it takes longer to fix it, make a note and fix it later
- Work on the feature instead

We could just fix the issue given that the solution doesn't take much time.
Otherwise creating a separate ticket is advised.


### 4.4 Planned Refactoring

- Set aside a time to refactor a piece of code
- Not related to any features
- Need to simplify code that's been giving trouble to the team regularly


### 4.5 Long-Term Refactoring

- Some refactoring work can take a team weeks to complete
- Instead of dedicated/planned refactoring, gradually work on simplifying the code one small chunk at a time.


## 5. When Should I Not Refactor?

- If code is messy but it works and it doesn't need to be modified, it doesn't need to be refactored. You can treat it as a library.


## 6. Two Hats

This is a method for working on any feature, not just refactoring

- While working on any feature, divide the time between two distinct activities: adding functionality and refactoring.
- We should only focus on one thing at a time.
- When adding functionality, don't think about the structure of the code.
- When refactoring, don't change any functionality in the code.
- https://twitter.com/KentBeck/status/1111050408007360512

Again a good example of this approach would be the one discussed under "Preparatory Refactoring"

Here, the PRs are separated clearly such that the feature PRs are really small and just change the functionality, not the structure of the code.

Similarly, the refactor PRs make it easy to have an eventual feat PR which is small and dedicated to fix the required issue.


## The End
