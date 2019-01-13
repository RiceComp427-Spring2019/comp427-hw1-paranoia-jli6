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
  - Confidentiality and privacy (need to disentangle): grades, submissions, student identities
        In particular, none of the above should be publicly viewable, in particular (student, grade) pairs. A student is not going to want their grades publicly viewable (privacy?), we need to keep submissions confidential to avoid Honor Code type violations, and student identities should be confidential simply because.
  - Integrity of grades and submissions. We don't want a student changing their grade, or changing their submission after the due date.
  - Availability of grades would be good to have. We need availability of submissions so I can grade them. Students want availability of grades so they know how well they're doing.
  - Authenticity of (student, grade, submission) triplets. That is, we don't want a student to be able to "change" their grade by swapping places with someone else.

  - explanatory_paragraph ...
- Threats:
  - An attacker may seek to raise their grade by any of the following methods:
        Editing submission after due date
        Setting or Editing numeric grade value
        Swapping places with another student, so the other student gets the attacker's grade
                An attacker can submit under another student's name, but we'd want to prevent this
  - An attacker may seek to cause chaos by making the grades unavailable, or
        by deleting all grades or submissions
  - explanatory_paragraph
  - explanatory_paragraph ...
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
