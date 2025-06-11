---
title: Site Expectations
date: 2025-05-30 20:00:00 -400
categories: [devlog, gamedev]
tags: [game]
toc: true
---

## Whack-a-mole like project
Today I will be starting a new project! My goals for this project is to complete it as fast as possible, and release a working demo by the end of this week. It is only three, four days, but as I have been struggling a lot with releasing stuff, I want to focus on creating simple, and fast projects so I can get it out in the market. I just want to have a completed project in my portfolio really.

## Project details
Many of these information might be subject to change, but here are the details I have in my mind as of right now.

### Core Concept
This project will be a round based game. Creating an open ended game feels hard, especially as a Solo Dev. I am not the best at creating maps and assets, and even though I have some familiarity with Blender, its not enough to create whole bunch of assets. All in all, I am not very confident in my modeling skills, which is why I want to keep it to minimum for this project.

For each round, players will participate in a whack a mole like game. There will be a NxN grid, and from each cell, an item will impulse up, and then fall down. Our goal is to "break" the item before it falls down. And thats it really. Become the person who breaks the most items.

We will have a concept of winning. Top three of each round will be awarded with some extra cash, or some other rewards like case keys and so on. However, there will be a main progression system which allows you to slowly unlock more items. Some of them will be paid game passes. I also want to play around with implementing some in game currency and microtransactions.

## Goals of the Project
I have few main goals in this project

### Releasing it FAST FAST FAST
Most of my projects, while starting off simple, becomes more and more complex as I feel like the project isn't ready to be released without adding some new features. This usually causes me to spend months on a project and no release, nothing to show for really even in my portfolio. This is such a waste of time. I am really trying to change that for this project.

My goal is to implement the round system fully, and just few tools and few items. And that is really all that is needed to finish this game. Once it is completed, I want to do some playtesting and continue to add some more contents, and monetize the game more.

I also originally had an idea of creating this as an open ended game like [Fisch](). I realized however that I didn't have enough details drawn out for the game, and realized that would take many days just to figure stuff out. Perhaps once this game is out, I will transition over to the open ended concept as I believe that is the better choice in the long run.

### Making the system as reusable as possible
Despite using ECS (Entity Component System), I sometimes still couple too many feature concepts, which makes my systems either awkward or difficult to reuse. The goal of this project is to create the systems such that, I am able to drag and drop it into some other projects, and it just *works*. Of course sometimes, that isn't always fesible.
