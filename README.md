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
  - We have a system where the only people with read access to all submissions and write access to the grading records are the grader and instructors. This system will also be completely inaccessible to people outside of the class. Additionally, this system will also be able to identify the grader such that nobody can impersonate the grader to gain their privileges and access. In this system, submissions can't be changed after the due datetime, and submission datetimes can't be forged. We will also assume each submission was actually submitted by the person whose name or other identifier is indicated on the submission (i.e. Alice didn't submit work under Bob's name).
- Assets:
  - We want to protect the confidentiality and privacy of several things. The names or identities of students shall remain unknown to everybody except for the grader and instructors. Each student's submissions should not be accessible to anybody except the particular student, the grader, and instructors. Furthermore, each student's grades should not be viewable to anyone except for the particular student, the grader, and instructors. Imagine the uproar if Alice could see Bob's grade!
  - We also want to protect the integrity of grades and submissions. By assumption, submissions can't be changed. And for grades, we want to make sure a student can't change their (or anyone else's) grade.
  - The availability of submissions and grades also needs to be protected. If submissions are unavailable, I won't be able to grade them. If grades are unavailable, the students will be displeased. If grades are somehow erased from the system, then there will have been a lot of wasted effort!
  - Lastly, we need to protect the authenticity of submissions and grades. The authenticity of submissions is by assumption. The authenticity of grades, namely that a particular submission was actually graded by the grader, rather than someone else, is also by assumption. Specifically, we assume only the grader (and instructors) have write access to the grading records.
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
