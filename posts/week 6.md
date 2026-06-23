---
title: Week 6 - Concept and Functional Requirements
date: 2026-03-20
author: Joyce Pei
summary: Interpreting the brief and defining the core functional requirements for Cyber Grave.
tags:
  - Functional Requirements
  - Concept Development
  - Scope
---

# Week 6 - Concept and Functional Requirements

## Part 1: Interpreting the Brief

At the beginning of the project, I understood the brief as asking for more than a static website. The prototype needed to behave like a small web application: users should be able to create content, make choices, and see the system respond. For my group, this became the starting point for Cyber Grave, a reflective web app for people who want to write emotional posts without turning them into normal public social media content.

The main user need came from a familiar behaviour: people often write notes, private stories, or social media posts when they feel overwhelmed, but later they may delete them because the content feels too personal. This suggested that the app should not simply publish posts. It should give users a softer choice about what to do with emotional writing after it is created.

## Part 2: Core Functional Requirements

The essential requirement is the burning post flow. A user must be able to create a burning post, keep it private at first, and later choose between two actions: Save it or Let it go. Save it means preserving the post as a grave, while Let it go means releasing it into the Ash Field as a dandelion. This makes the main function not just posting, but changing the emotional state of a post.

I separated the requirements into core and optional features. Core features include login, creating a burning post, saving to Grave, releasing to Ash Field, and viewing public graves in Community. Optional features include richer social functions, advanced notifications, real-time chat, or recommendation systems. These were useful ideas, but they were not necessary for proving the main concept.

## Part 3: Early Risks and Constraints

The biggest design risk was that the concept could become too abstract. Fire, graves, ash, and dandelions are symbolic, but users still need to understand what each action does. Another risk was privacy. Because the content may be emotional, the default state should be private, and public sharing should require a clear user choice.

The technical scope also needed control. Building a complete emotional social platform would be too large for the prototype. A smaller full-stack flow using MojoJS, SQLite, templates, and client-side visual effects was more realistic.

## Design Decisions

1. I chose the burning post lifecycle as the core requirement because it connects user need, emotional meaning, and system behaviour.
2. I kept Community as a secondary feature because the private reflection flow needed to work clearly before adding more public interaction.

## Personal Reflection

At first, I imagined a broad grief-tech community. After analysing the brief, I realised the stronger direction was a focused emotional posting flow. This helped me understand that functional requirements are not just a feature list. They are decisions about what the app must do first, and what can wait.
