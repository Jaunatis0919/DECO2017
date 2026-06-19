---
title: A3 Reflection
date: 2026-06-20
author: Joyce Pei
summary: Reflection on the prototype performance, user experience, accessibility, functional requirements, and improvement plan.
tags:
  - A3
  - Reflection
  - Prototype
---

# A3 Reflection

530238827 fpei0529

In this final reflection, I evaluate the performance, user experience, accessibility, and functional requirements of our web application. Overall, the prototype successfully demonstrates the core concept, but the evaluation also shows several limitations in technical polish, usability, and accessibility.

## Performance

Following the Week 11 lecture's distinction between mechanical correctness and user effectiveness, I first evaluated whether the system technically did what we intended it to do. For this prototype, integration-style validation was the most useful approach because the main technical risk was not whether one isolated function worked, but whether routes, templates, session data, and SQLite database updates worked together across the main user flows.

![A3 reflection testing evidence figure 1](assets/a3-reflection-figure-1.png)

![A3 reflection testing evidence figure 2](assets/a3-reflection-figure-2.png)

Overall, these results suggest that the prototype was technically reliable for the main assessed flows. The core lifecycle of a post, from creation, to saving or releasing, to being displayed in the correct space, worked as a connected system rather than as isolated pages.

## User Experience

After evaluating the technical behaviour of the prototype, I planned a small user experience evaluation to understand whether users could complete the main flow, understand the purpose of the application, and interpret the emotional meaning behind the interactions.

## Participant

The testing method will be a small task-based think-aloud walkthrough, followed by a short semi-structured interview. During the walkthrough, participants will be asked to speak their thoughts while using the prototype. This will help reveal moments of hesitation, confusion, or misunderstanding that may not be visible from technical testing alone. After the tasks, I will ask a few follow-up questions about what felt clear, what felt confusing, and whether the concept of saving or releasing a post made sense to them.

The findings will be analysed using thematic analysis. Instead of treating each comment separately, I will group observations into key themes. The main themes I expect to use are navigation and page hierarchy, interaction feedback, conceptual clarity, and emotional consistency.

## Thematic Analysis

Overall, the simulated testing suggests that users can understand and complete the core A2 flow: creating a burning post, choosing Save it or Let it go, and finding the result in Grave, Ash Field, or Community. The strongest areas are the emotional concept and visual atmosphere. The main areas for improvement are clearer interaction feedback, stronger first-time guidance, and more explicit communication of where a post has moved after each action.

## Functional Requirements

Most of the main functions were built. Users can create a burning post, then choose Save it or Let it go. Saved posts become graves, and released posts appear as dandelions in the Ash Field. The Community page also lets users view public graves.

Some ideas were made smaller. The burning effect, Ash Field, and Community features are working, but they are still prototype-level. The original plan was a bit too big because it included emotional writing, animation, database storage, and social features all together.

The final prototype is simpler than the first idea, but it still shows the main concept: writing something emotional, then deciding whether to keep it or release it.

## Improvement Plan

I learned that users need clear feedback after they click something. For example, after clicking Save it or Let it go, the post moves to another place, but users may not notice immediately. I would add a short message like "Saved to Grave" or "Released to Ash Field."

I also learned that visual effects are useful, but they cannot explain everything. Because the site uses metaphors like burning, graves, and dandelions, I would add clearer labels and better focus states for accessibility.

If I continued the project, I would improve the Garden flow first before adding more Community features, because that is the most important part of the user experience.
