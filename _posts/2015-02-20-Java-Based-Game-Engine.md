---
layout: post
title: Java Based Game Engine
---

Searched for a decent Java-based game engine for use as a possible alternative for the project. Aims: 1) animations, 2) collison detection.

Overall a very tight week for me personally. Got a puppy (not really necessary information, but relevant), so time is really stretched even more than usual. Exams, other class work, etc.
Also, Michael and I had a tough time coordinating our schedules this week, so we weren't able to meet and discuss/collaborate on the task. Need to aim higher for the upcoming weeks.

So far, my most promising lead is an engine called JGame. In the README.txt, it states that JGame "features sprites with automatic animation and collision detection," which sounds perfectly suited to the task.
(It is an open-source project, home page at http://www.13thmonkey.org/~boris/jgame/)


Need to:
1) Get Apache Ant?

Other options: Slick2d, JBox2D

Slick2D came with many example games: one of them (Ramjet) utilizes exactly the features we need (animation and collision detection); the game is the classic rocket-ship-avoiding-asteroids-in-a-static-window layout (collision with asteroids results in explosion, animation of asteroids' and ships' movement is fluid).


*****************************************

Edit: It's March 10; we have pretty much abandoned the Java-based game engines at this point. I (and Shaurya and Maxim) am now working on plain Android/Java code, which we'll then translate to Ruby and run in RubyMotion. Michael is working with Cocos2dx (C#).
Coding is moving along, but it's uphill going trying to figure out the best way to implement this in Java/Android, which I have never developed apps with before.