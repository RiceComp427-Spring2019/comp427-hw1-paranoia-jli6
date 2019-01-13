# <img src="http://www.rice.edu/_images/rice-logo.jpg" width=180> Comp427, Spring 2018, Homework 1
## Rational Paranoia
The homework specifications, as well as the corresponding course slide decks,
can be found on the [Comp427 Piazza](https://piazza.com/class/jqifhp864b37ju).
This assignment is due **Thursday, January 17 at 6 p.m.**

You will do this homework by editing the _README.md_ file. It's in
[MarkDown format](https://guides.github.com/features/mastering-markdown/)
and will be rendered to beautiful HTML when you visit your GitHub repo.

## Student Information
Please also edit _README.md_ and replace your instructor's name and NetID with your own:

_Student name_: Dan WALLACH

_Student NetID_: dwallach

Your NetID is typically your initials and a numeric digit. That's
what we need here.

_If you contacted us in advance and we approved a late submission,
please cut-and-paste the text from that email here._

## Problem 1
- Scenario: Grading
- Assumptions:
  - ??????
- Assets:
  - Various properties (AIC, etc.) of:
    - Grades
	- Student identities
	- Submissions
  - Recall that privacy and confidentiality are related but distinct. Privacy is more at the individual level, while confidentiality is more at the organizational level. So a student would want grade privacy but we'd want grade confidentiality so as to avoid running afoul of applicable confidentiality laws.
  - Assuming that Regulations mandate confidentiality as follows:
    - list of students not be publicly viewable. In other words, the general public should not know if Alice is in the class or not.
	- grades not be viewable to the public nor other students (i.e. Alice can see Alice's grade, but not Bob's). Imagine the uproar otherwise!
	- submissions not be viewable to the public nor other students
  - Integrity, as follows:
    - grades: a student shouldn't be able to change their (or anyone else's) grade. As an example, let's say I graded Alice's submission to be 84/100. She should not be able to change it to be 100/100 in whatever system I'm using to store the grades.
	  - A student should also not be able to somehow swap two entries in the grade datastructure. That is, Alice should not be able to swap herself and Bob in the grade database in the hopes of getting a better grade.
	- submission: a student shouldn't be able to change their (or anyone else's) submission. As an example, let's say Alice submitted something on time, but it would deserve only 86/100. She should not be able to update her submission past the due date to get a 100/100 or whatever.
  - Availability, as follows:
    - Submissions need to be available so I can grade them
	- Grades need to be available to the students and the professors, or else there will be complaints. They need to know how well they're doing!
  - Authenticity, as follows:
  	- We need to make sure Alice's submission was actually submitted by Alice.
	  - Of course, we can't guarantee this 100%. But we can have policies that punish Alice if she submits her work on Bob's behalf, and vice versa. This is known as the Honor Code.
  - Authenticity of (student, grade, submission) triplets. That is, We don't want a student to be able to "change" their grade by swapping places with someone else.
  - explanatory_paragraph ...
- Threats:
  - Confidentiality/Privacy:
    - An attacker may seek to see other people's grades. Of course, Alice isn't going to want some arbitrary Bob to see her grade, especially if it's low.
	- An attacker (or stalker) may seek to see who's in the class
	- An attacker, perhaps someone due to take the class next year, may seek to see the submissions!
  - Integrity: An attacker may seek to raise their grade by any of the following methods:
    - Editing submission after due date
    - Setting or Editing numeric grade value
	- An attacker, Alice, may seek to lower their worst enemy, Bob's, grade by sending in a crappy submission while posing as Bob
  - Availability: An attacker may seek to cause chaos by making the submissions or grades unavailable, or by deleting all grades or submissions
  - Authenticity:
    - Alice submitting her work while posing as Bob, so Bob doesn't have to do any work
- Countermeasures:
  - Permissions system / Login system
  - Tamper-proof submission timestamp via Travis-CI builds (GH commits can be fooled)
  - If submissions are done by email, an "unhackable" "secure" server
  - If submissions are done on paper, a secure room to store submissions
        In one case, somebody snuck into an office via social engineering and the ceiling
  - If grading is done over the web, use HTTPS when:
        submitting grade values
        reading submissions
        basically everything!
  - explanatory_paragraph
  - explanatory_paragraph ...

## Problem 2
- Scenario: Stadium
- Assumptions:
  - explain_your_assumptions
- Assets:
  - The game
  - The game score
  - Human lives
  - Human money (e.g. threat of robbery)
  - Human safety, whether from natural factors like building collapse to targeted attacks like terrorism
  - Revenue
  - explanatory_paragraph ...
- Threats:
  - Pranks on the stadium before a game (when stadium is empty), which would affect the audience experience
  - Streakers
  - Game manipulation
  - Terrorism
  - Building collapse
  - Petty crime (e.g. robbery/theft)
  - Unauthorized persons in general
  - Unauthorized viewing
        Drones
  - explanatory_paragraph
  - explanatory_paragraph ...
- Countermeasures:
  - Ticket system to ensure only authorized persons enter
  - Policies of penalties for game manipulation
  - Security cameras
  - Locking gates and doors
  - Security guards
  - Anti-drone equipment
  - explanatory_paragraph
  - explanatory_paragraph ...

## Problem 3
- Scenario: Your choice (give a brief explanation)
- Assumptions:
  - explain_your_assumptions
- Assets:
  - explanatory_paragraph
  - explanatory_paragraph ...
- Threats:
  - explanatory_paragraph
  - explanatory_paragraph ...
- Countermeasures:
  - explanatory_paragraph
  - explanatory_paragraph ...
