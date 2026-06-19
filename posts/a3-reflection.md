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

Following the Week 11 lecture’s distinction between mechanical correctness and user effectiveness, I first evaluated whether the system technically did what we intended it to do. For this prototype, integration-style validation was the most useful approach because the main technical risk was not whether one isolated function worked, but whether routes, templates, session data, and SQLite database updates worked together across the main user flows.

| Tested flow | What was checked | Result |
| --- | --- | --- |
| Create burning post | Checked whether a user could create a new post and store it in SQLite | Passed. This shows that the basic post creation flow worked across route, template, and database. |
| Save post to grave | Checked whether a burning post could be saved into the grave state | Passed. This shows that the system could update post state and support the “preserve” side of the concept. |
| Let it go / release to Dandelion or Ash Field | Checked whether a post could move into the release state | Passed. This shows that the emotional release flow was technically functional. |
| Grave visibility | Checked whether grave visibility could be changed | Passed. This shows that privacy/public display logic was partially working. |
| Public graves in Community | Checked whether public graves appeared on the Community page | Passed. This shows that content could move from a personal space into the shared community space. |
| Grave deletion ownership | Checked whether deletion was limited by ownership | Passed. This shows that basic user-specific permissions were considered. |
| Lint check | Ran npm.cmd run lint | Passed. This shows the code met the project’s linting rules. |
| Automated test check | Ran npm.cmd test | Passed. This shows the implemented test suite could run successfully. |
| Lighthouse performance audit | Checked browser-level performance score | Performance score: 93. This suggests that the page performed well under the tested Lighthouse conditions. |

![A3 reflection testing evidence figure 1](assets/a3-reflection-figure-1.png)

![A3 reflection testing evidence figure 2](assets/a3-reflection-figure-2.png)

Overall, these results suggest that the prototype was technically reliable for the main assessed flows. The core lifecycle of a post — from creation, to saving or releasing, to being displayed in the correct space — worked as a connected system rather than as isolated pages.

| Limitation / issue | Why it happened | Future improvement |
| --- | --- | --- |
| Testing was mainly conducted under controlled development conditions | The project was evaluated as a coursework prototype rather than a long-term deployed product | Test the application after deployment and collect more realistic usage observations |
| The app was not tested with a large number of posts, users, comments, or notifications | The available test data was small and focused on the main A2 flows | Create a larger seed dataset to test database performance and page loading with more content |
| Slow network conditions, different devices, and different browsers were not fully tested | The testing process prioritised core functional validation first | Add cross-device and cross-browser checks, and test under slower network settings |
| Some secondary features, such as the profile page, were simplified | Development time was prioritised toward the main Burning Post → Grave / Dandelion flow | Expand the profile page with more complete user history, statistics, and interaction records |
| Lighthouse performance was strong, with a score of 93, but this only reflects one tested condition | Lighthouse provides a useful snapshot, but it does not represent all real user environments | Repeat Lighthouse testing across different pages and combine it with manual performance observations |
| Edge cases were not fully covered | The test suite focused on expected successful flows | Add tests for empty input, failed submission, invalid post IDs, and unauthorised actions |

## User Experience

After evaluating the technical behaviour of the prototype, I planned a small user experience evaluation to understand whether users could complete the main flow, understand the purpose of the application, and interpret the emotional meaning behind the interactions.

## Participant

|  | Iris | Max |
| --- | --- | --- |
| Age | 21 | 23 |
| Background | University student | Early-career worker |
| Relevant need | Uses Notes app or journaling apps to record thoughts when stressed. Sometimes posts private stories or close-friends content on social media. | Frequently uses social media to express moods, but often deletes posts later because they feel too personal. |
| Why suitable | This participant fits the target user group because they are familiar with digital self-expression and may understand the value of saving or releasing emotional posts. | Wants a softer way to express unresolved feelings without making them fully public. |

The testing method will be a small task-based think-aloud walkthrough, followed by a short semi-structured interview. During the walkthrough, participants will be asked to speak their thoughts while using the prototype. This will help reveal moments of hesitation, confusion, or misunderstanding that may not be visible from technical testing alone. After the tasks, I will ask a few follow-up questions about what felt clear, what felt confusing, and whether the concept of saving or releasing a post made sense to them.

| Task | Iris | Max |
| --- | --- | --- |
| Create a burning post | Iris understood the create post button quickly and described the action as similar to writing a private journal entry. | Max also completed the task, but expected clearer feedback after submitting the post. |
| Choose Save it or Let it go | Iris understood that Save it felt like preserving a memory, while Let it go felt more symbolic and gentle. | Max understood the difference after seeing the results, but initially wanted a short explanation of what each choice meant. |
| View result in Grave / Ash Field / Community | Iris found the Grave meaningful and understood it as a place for memories. She liked that Let it go created a softer visual result in Ash Field. | Max noticed the result, but said he wanted stronger confirmation that the post had moved successfully. |
| Check posts in Community | Iris understood Community as a shared memorial space, especially for public graves. | Max understood the Community page, but was unsure at first whether burning posts there were public, friends-only, or anonymous. |

The findings will be analysed using thematic analysis. Instead of treating each comment separately, I will group observations into key themes. The main themes I expect to use are navigation and page hierarchy, interaction feedback, conceptual clarity, and emotional consistency.

## Thematic Analysis

| Page Navigation And Hierarchy | Both users were able to complete the main flow, but Max needed more guidance after creating a post. The Garden page contains several important areas, including burning posts, graves, and Ash Field, so the hierarchy can feel slightly dense for a first-time user. Iris moved through the flow more easily because she interpreted the website as a reflective journaling space. Max, however, expected clearer direction after each action, especially after creating or moving a post. | Possible improvement:Add subtle visual cues or status messages after a post is created, saved, or released, so users know where to look next. |
| --- | --- | --- |
| Interaction Feedback | Both users wanted clearer confirmation after actions. For example, after pressing Save it or Let it go, the post disappears from the burning post area and moves elsewhere, but the transition may not be immediately obvious. Max especially wanted feedback such as “Saved to Grave” or “Released to Ash Field.” Iris understood the movement more intuitively, but still found confirmation helpful. | Possible improvement:Use short, gentle confirmation messages or transition animations to show that the post has moved successfully. |
| Conceptual Clarity | The two main actions, Save it and Let it go, were generally understandable, but Max initially needed more explanation. Iris understood Save it as keeping a memory and Let it go as emotional release. Max understood the distinction after seeing the Grave and Ash Field results. This suggests that the concept is strong, but the first-time user experience could benefit from slightly clearer wording. | Possible improvement:Add concise supporting text near the buttons, such as “Save it as a grave” and “Release it into Ash Field,” without over-explaining the emotional metaphor. |
| Emotional Consistency | Both users felt that the visual direction matched the emotional purpose of the prototype. Iris described the Ash Field as soft and calming, while Max felt the burning effect matched the idea of temporary emotional expression. The low-saturation colour palette, grave metaphor, and dandelion visuals helped communicate a reflective and gentle tone. However, Max noted that some interaction states could feel more emotionally responsive, especially when a post disappears after being saved or released. | Possible improvement:Make transitions slower and softer when posts move between states, so the emotional meaning feels more continuous. |

Overall, the simulated testing suggests that users can understand and complete the core A2 flow: creating a burning post, choosing Save it or Let it go, and finding the result in Grave, Ash Field, or Community. The strongest areas are the emotional concept and visual atmosphere. The main areas for improvement are clearer interaction feedback, stronger first-time guidance, and more explicit communication of where a post has moved after each action.

## Functional Requirements

Most of the main functions were built. Users can create a burning post, then choose Save it or Let it go. Saved posts become graves, and released posts appear as dandelions in the Ash Field. The Community page also lets users view public graves.

Some ideas were made smaller. The burning effect, Ash Field, and Community features are working, but they are still prototype-level. The original plan was a bit too big because it included emotional writing, animation, database storage, and social features all together.

The final prototype is simpler than the first idea, but it still shows the main concept: writing something emotional, then deciding whether to keep it or release it.

## Improvement Plan

I learned that users need clear feedback after they click something. For example, after clicking Save it or Let it go, the post moves to another place, but users may not notice immediately. I would add a short message like “Saved to Grave” or “Released to Ash Field.”

I also learned that visual effects are useful, but they cannot explain everything. Because the site uses metaphors like burning, graves, and dandelions, I would add clearer labels and better focus states for accessibility.

If I continued the project, I would improve the Garden flow first before adding more Community features, because that is the most important part of the user experience.
