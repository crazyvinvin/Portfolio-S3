# Portfolio S3

## Table of Contents
TODO

## Introduction
This semester has the goal to build a full-stack web application as an individual project. Together with this application there are many learning outcomes which should be achieved. This document will show how I worked towards my so called LO’s. Besides the individual project there is also a group project which you can learn more about in my group project portfolio.

# F1 Guesser

## Project Description
For my individual project, I want to build a web application where you can guess Formula One race outcomes against your friends to compete for the most points at the end of the Formula One season.

## Full-Stack Web Application
The application should consist of a separate front-end and back-end. The back-end should be build using an Object Oriented application framework whereas the front-end needs to use a JavaScript framework.

## Requirements
I’ve created a few simple requirements to give a better understanding about the project and the functionality that will be available.

**FR-01:** The user should be able to create a playgroup.
- B-01.1: A maximum of 8 people are allowed per playgroup.

**FR-02:** A user should be able to join a playgroup using a code from another user’s group.
- B-02.1: If the playgroup is full, the user that wants to join gets a pop-up that says that the playgroup is full.

**FR-03:** The user should be able to see how many points other people in his playgroup have.
- K-03.1: A user’s points is shown next to the user’s username.
- K-03.2: The user should be able to see a bar chart of all the points of the members of his playgroup.

**FR-04:** The user should be able to see a countdown to the next race week.
- K-04.1: A race week is from Monday till Sunday, if there’s a race on Sunday.
- B-04.2: The time to a next race week is only visible if a race week is not already happening

**FR-05:** The user should be able to go through a round of questions
- B-05.1: The user can only go through a round of questions during a race week.
- B-05.2: The user can only go through a round of questions when in a playgroup.
- K-05.1: During the round the user is able to select a F1 driver to answer each question.
- K-05.2: During the round the user gets to see how many points are available for each question.

**FR-06:** The user can see what answers other members of his playgroup have selected.
- B-06.1: The user can only see other member’s answers after having gone through the round of questions himself

**FR-07:** After a race week the user gets the available points for each question answered correctly.

## Conclusion
After a lot of doubt, I have chosen to change projects. Together with a few friends I have been playing on a Minecraft Server which has a mod (expansion) that adds programmable robots and computers to the game. I have a lot of motivation to build a project which uses data from those robots and computers.

Luckily, I will be able to use the knowledges I got in the last few weeks in my next project.

# Project MCS Analyser

## Project Description
I want to build a web application that gives users the ability to see and analyse data produced by robots on a Minecraft server. These Robots are part of a mod called MCS-CC.

## But what is MCS-CC?
MCS-CC, also known as Minecraft Synergy Computer Craft, is a by us (the MCS Team) made modification of the popular mod: “CC: Tweaked” (Which is also on itself a modification of another mod). CC: Tweaked adds programmable turtles and computers to Minecraft (Java edition). These turtles are essentially robots that can perform certain actions like digging blocks or moving items from one place to another. To have a turtle (or computer) perform an action you can write a script in a language called Lua which is then ran in the Lua Virtual Machine to actually make the turtle do something.

Using these computers and turtles you can automate almost everything in the game. 

## User Stories
I’ve created a few user stories to make the project and its functionality more clear. I chose user stories over requirements, because I already created requirements for my last project and want to see the difference.

- US-01: As a user I want to be able to see a system’s data displayed as a graph, so that I can analyse and monitor the system.
- US-02: As a user I want to be able to change a graph’s timespan so that I can analyse data over different amounts of time.
- US-03: As a user I want to see new data as soon as it’s available so that I can react to an unexpected situation quickly.
- US-04: As a user I want to be able to see if a system is turned on or off so that I know why a system is producing different data then before.
- US-05: As a user I want to be able get a description of a system about it’s service and purpose so that I can understand the data more easily.
- US-06: As a user I want to be able to create a custom graph with all the data available so that I can compare different systems with each other.

## Front End
For the front-end part of the application I have to use a JavaScript framework. After a bit of research about what options are available. It quickly comes down to Vue and React.  I haven’t done a lot with JavaScript before so I played around a little with both of the frameworks to see which one I would like more. I found out that anything and everything is possible with both of the frameworks, but React felt more intuitive to me. As a result I have chosen to build my front-end with ReactJS.

## Back End
For the back-end part of the application I want to work with an object oriented language. This means the big options are C# and Java. It’s important for a software engineer to be able to learn and apply new technologies. I have been using C# in the last two semesters and really want to expand my knowledge towards Java. I have no experience with Java at this point, but it’s one of the most used object oriented languages for back-end applications. One of the best Java frameworks for REST applications is Java Spring. This is also what I will be using for my project.

## Persistence
One of the (few) mandatory things this semester is that I learn about an Object-Relational Mapper and how to apply that knowledge in my project. Object relational mapping is, simply said, a technique that lets you manage data in database without having to write data access logic (because the ORM serves as the data access layer!). ORM has a lot of pros and cons, they can for example be very overwhelming to use and aren’t always the most performant. Nonetheless ORM’s can be super useful to abstract your database and save you a lot of time.

Hibernate is a framework that implements object relational mapping for Java applications. Part of the Spring framework is Spring Data JPA, which is an extra layer of abstraction on top of hibernate. Hibernate makes it possible to switch a project’s database without changing the back-end code, while Spring Data JPA reduces the needed back-end code to implement hibernate. I will be using Spring Data JPA together with hibernate and MySQL to achieve persistence in MCS Analyser.

## External Services
MCS Analyser will be using multiple external services made by the MCS Team. Most of these services will be used to gather data to be displayed by the analyser. There has also been the idea to authorize all of the MCS Services. This would mean that MCS Analyser would use the MCS Authentication Provider to authenticate our users.

To create a better understanding of how the different MCS Services interact with each other, I have designed a system context diagram following level 1 of the C4 model pattern.

![Context diagram of MCS Services](images/SystemContextDiagramMCS.PNG "MCS Services Diagram")
 
## Systems and Services
In this document there has been spoken alot about MCS Systems and MCS Services, but what is the difference? MCS Systems are the systems inside the Minecraft server. For example a farm that produces melons and pumpkins is called a MCS System. All the systems are registered at the MCS Systems API. MCS Services are the things we build outside of the Minecraft server. For example the MCS Analyser and the MCS Turtle Tracker are both MCS Services.

