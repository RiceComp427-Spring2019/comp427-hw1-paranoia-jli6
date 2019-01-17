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
  - We have a system where the only people with read access to all submissions and write access to the grading records are the grader and instructors. This system will also be completely inaccessible to people outside of the class. Additionally, this system will also be able to identify the grader such that nobody can impersonate the grader to gain their privileges and access. In particular, we assume the grader won't get phished or be robbed of their physical keys. In this system, submissions can't be changed after the due datetime, and submission datetimes can't be forged. We will also assume each submission was actually submitted by the person whose name or other identifier is indicated on the submission (i.e. Alice didn't submit work under Bob's name).
- Assets:
  - We want to protect the confidentiality and privacy of several things. The names or identities of students shall remain unknown to everybody except for the grader and instructors. Each student's submissions should not be accessible to anybody except the particular student, the grader, and instructors. Furthermore, each student's grades should not be viewable to anyone except for the particular student, the grader, and instructors. Imagine the uproar if Alice could see Bob's grade!
  - We also want to protect the integrity of grades and submissions. By assumption, submissions can't be changed. And for grades, we want to make sure a student can't change their (or anyone else's) grade.
  - The availability of submissions and grades also needs to be protected. If submissions are unavailable, I won't be able to grade them. If grades are unavailable, the students will be displeased. If grades are somehow erased from the system, then there will have been a lot of wasted effort!
  - Lastly, we need to protect the authenticity of submissions and grades. The authenticity of submissions is by assumption. The authenticity of grades, namely that a particular submission was actually graded by the grader, rather than someone else, is also by assumption. Specifically, we assume only the grader (and instructors) have write access to the grading records.
- Threats:
  - There are several threats to the confidentiality and privacy of student identities, submissions, and grades. If the grading occurs in a room, an attacker could place a camera, microphone, or other bug in the room to obtain information, especially grades. Or an attacker could pull a fire alarm during grading and run into the room and view graded submissions. If all of the class happens to be managed on an insecure analogue of the Canvas LMS, an attacker could simply sniff packets.
  - An attacker may also seek to violate the integrity of grades and submissions. One could affect submissions by physically entering the grading room and throwing away or changing answers on paper submissions. Another way is by submitting a GitHub commit with a forged timestamp. To change grades on a paper gradebook, an attacker can sneak into the grading room and erase the grader's grade and write in their preferred grade. If grading is digital, an attacker could hack into the digital gradebook and modify the values, possibly by using remote desktop malware on the grader's computer.
  - An attacker may also seek to violate the availability of submissions or grades. One way is by accessing the gradebook or submissions and deleting or throwing away everything. Another way is by shutting off the power to and spraying asbestos all over the grading room, ensuring grades for in-paper submissions can't come out until the room is made safe again.
  - Lastly, an attacker Alice may seek to violate authenticity by making a low-quality submission under the name of Bob, or by hiring a friend to make a good submission under the name of Alice.
- Countermeasures:
  - To counter an attacker targeting confidentiality, integrity, availability, or authenticity, we can store submissions and grades under lock and key to which only the grader would have access, and restrict access to the grading room by the same methods. For online systems, we can also use a secure and encrypted service with a proper login system with permissions, and train the grader to not give out their login credentials. These countermeasures are all low-cost and have decent benefits. At Rice University, these are usually sufficient countermeasures, because there isn't a rampant cheating culture for most classes.
  - The following countermeasures are more costly, but can confer necessary benefits if we are operating in a situation with a rampant cheating culture. We can check the grading room for espionage equipment, and restrict access to whatever grading room we use. This includes securing the ceiling to ensure nobody sneaks in through it (this has actually happened before). Auto-closing and auto-locking doors can defend against the fire alarm approach. We can also install security cameras and security guards everywhere around the grading room, so any attacker will be more discouraged via prosecution.
  - We will need additional countermeasures to defend against the "forged timestamp GitHub commit" attack. One countermeasure is simply for the submission server to record its own time when the submission is made. In the case of COMP 215, this was achieved by using the timestamps of Travis-CI builds. This is low-cost and confers decent benefits.
  - A decent countermeasure for protecting authenticity is the combination of names, student IDs, and the Rice University Honor Code. Although this doesn't work 100% of the time, the assumptions take care of the rest.

## Problem 2
- Scenario: Stadium
- Assumptions:
  - We assume the stadium has good build quality and therefore won't collapse under normal conditions. We also assume a car-dominated society, so people attending stadium games will be arriving in their own personal cars.
- Assets:
  - We value the confidentiality of a couple things. In order to prevent scandals, we want to ensure fair games by maintaining the confidentiality of team communication and what goes on in the locker room. We also want the attendance records (aside from the amount of people in attendance) a secret.
  - We also value the integrity of several things. We want to protect the integrity of any games the stadium will host. There would be a scandal if people could manipulate the high-profile football games. Additionally, we need to preserve the integrity of the people in attendance. As an example, people can be "modified" by being robbed.
  - We also value the stadium's availability. In particular, the stadium needs to be fully capable of hosting a packed game. Parking availability is also an important factor. If there aren't enough available parking spaces, attendance will take a hit.
  - The privacy of stadiumgoers must also be protected. Nobody wants their bathroom activities to be viewable by another person.
  - We also care about authenticity. In particular, we need to make sure whoever enters the stadium is who they claim to be.
- Threats:
  - One could attack confidentiality and privacy in several ways. One way is by placing cameras or other recording devices in various places in the stadium. If it's in the bathroom, it's attacking privacy. If it's in the locker room or wherever on the field the team discusses plays with each other, it's an attack on confidentiality. If the cameras are at the stadium entrances, the attacker will know everybody who's attending the game, which is attack on the stadiumgoers' privacy. Lastly, we want to keep the game confidential, specifically preventing unauthorized viewing of the game in order to protect the stadium revenue.
  - Integrity can be threatened in several ways. During a game, by eavesdropping on the teams as discussed in confidentiality attacks, a team can gain an unfair advantage. Another possible attack is for a fan with a fan to blow powerful streams of wind at the football, possibly leading to a missed field goal or an incompleted pass. One could also manipulate the game by breaking into the scoreboard and changing the numbers, which even in the best case will disrupt the game. Streakers, throwing projectiles onto the field, or even shooting are other ways to disrupt the game as well.
  - Another threat to integrity concerns the stadiumgoers' welfare. In particular, people need to be safe from being robbed, injured, or otherwise having their integrity compromised.
  - There are some threats to availability as well. The night before a big game, a rogue drone operator could dump asbestos all over the seating and the field, which would make the stadium unavailable for quite a while. Other attacks on availability include pranks requiring a stadium closing and people unaffiliated with the games using the parking lot.
  - There is basically one type of threat to authenticity. One person will pretend to be another. Anybody could pretend to be a coach, player, referee, security guard, custodian, ticket holder, or other personnel in order to gain undeserved privileges. At best, it is simply a fan who will do anything to meet a star player, and at worst, it is somebody who seeks to cause death.
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
