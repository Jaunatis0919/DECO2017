---
title: Week 9 - Data, Routes, and Implementation Decisions
date: 2026-05-04
author: Joyce Pei
summary: How the Cyber Grave prototype connects emotional user actions to database structure and route behaviour.
tags:
  - Data Design
  - Routes
  - Implementation
---

# Week 9 - Data, Routes, and Implementation Decisions

## Part 1: Working Backwards from the Emotional Flow

In Week 9, I started to think about how the emotional flow should become data. The key question was: when a user clicks Save it or Let it go, what actually changes in the system?

This made it clear that the app needed separate data states. A burning post is active and temporary. A grave is saved and more permanent. A dandelion is released and shown visually in the Ash Field. Treating these as different database records made the system easier to reason about than keeping every post in one table with many possible states.

## Part 2: Database Requirements

The main database objects are users, burning_posts, graves, and dandelions. Users are needed for ownership. Burning posts store the title, content, created time, expiry time, and status. Graves store saved posts, visibility, flowers, and candles. Dandelions store released posts and a seed value so their visual form can be generated consistently.

This data structure supports the core functional requirements. Creating a post inserts a row into burning_posts. Saving a post creates a grave and removes the burning post. Releasing a post creates a dandelion and removes the burning post. Making a grave public changes its visibility so it can appear in Community.

## Part 3: Routes, Templates, and System Responses

The prototype uses MojoJS routes to connect user actions to database changes. For example, POST /garden/create creates a burning post, POST /garden/save moves it to graves, and POST /garden/release moves it to dandelions. The Garden template then reads the user's burning posts, graves, and dandelions and renders the correct sections.

This route-model-template structure was useful because each part has a clear responsibility. Routes handle the action, models handle SQLite queries, and templates show the result. Client-side JavaScript and p5-style visuals support the burning effect and dandelion display, but the important state change still happens in the database.

## Part 4: Scope Control

Some ideas had to be reduced. A full emotional social network would require stronger moderation, more privacy controls, and more complex relationships between users. For the prototype, I focused on the private post lifecycle and a simple public grave feature. This kept the implementation achievable while still showing the main concept.

## Design Decisions

1. I used separate tables for burning posts, graves, and dandelions because each one has different behaviour and display needs.
2. I kept the Community logic simple because privacy and emotional safety are more important than adding many social features.

## Personal Reflection

This stage helped me understand that database design is also a design decision. If the data structure is unclear, the emotional flow becomes unclear too. The technical structure needs to support the user's mental model, not just store information.
