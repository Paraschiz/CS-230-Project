# CS 230 Project: Draw It or Lose It Software Design

This repository contains the software design document I created for The Gaming Room in CS 230: [Software Design Document](CS_230_Project_Three_Software_Design_Document.docx)

## Who was the client, and what did they want?
The client was The Gaming Room, which wanted to expand its Android game, Draw It or Lose It, into a web-based game that runs on many platforms. In the game, teams guess a puzzle from drawings that render over time. The requirements were that a game could have one or more teams, each team could have multiple players, game and team names had to be unique, and only one instance of the game service could exist in memory at a time.

## What did I do particularly well?
I connected each technical decision back to the client's actual requirements. I explained how the singleton and iterator patterns met the uniqueness and single-instance rules, compared Windows, macOS, Linux, and mobile in a clear evaluation table, and made a final recommendation (Linux in the cloud) that addressed storage, memory, networking, and security for this specific game.

## How did the design document help with the code?
Writing the design document first made the code easier to plan. The UML diagram showed how Game, Team, and Player could share an Entity base class, and thinking through the design constraints made me notice issues like thread safety in the singleton and where name checks should happen before writing the code.

## What would I revise?
I would add a system architecture diagram to the System Architecture View section. A diagram showing the players' devices, the load balancer, the game servers, and the database would explain the distributed design faster than text, and I would shorten the Recommendations section to match.

## How did I interpret the user's needs?
I turned each requirement into a design decision: unique names became iterator-based checks, the single game service became a singleton, and support for many devices became a server-based design with a browser client. I also considered that the client's staff had limited server experience, so I recommended managed cloud services. Considering the user's needs matters because software that is technically sound but doesn't solve the client's real problem still fails, and catching mismatches early is much cheaper than rework later.

## How did I approach the design, and what would I do in the future?
I started with the requirements, identified the constraints, modeled the domain with UML, applied design patterns, evaluated the platforms, and then made recommendations. In the future, I would also write user stories, ask the client about unclear requirements early (like whether names should be case-sensitive), build a small prototype sooner, and review the design with the client at each stage.
