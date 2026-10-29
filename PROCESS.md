# Development Process — BENTO BOX

## Project Overview

BENTO BOX is an interactive task planner that turns time into food. Each food portion represents one hour of work, allowing users to organise their daily tasks by creating a personalised bento box.

The project explores how visual interaction can make time management more playful and engaging.

## Previous Development — Retrospective

*This section summarises work completed before I started documenting the project on GitHub on 24 October 2026.*

### 1. Concept and Interaction Design

I started with the idea of transforming a traditional to-do list into an interactive food arrangement experience.

I established the main interaction rules: users select a food item, enter a task name, choose its duration, and add it to their bento box. Each food portion represents one hour.

I also introduced different container sizes for different planning durations.

### 2. Visual Exploration and Food Assets

I explored different illustration styles before choosing a soft, semi-3D visual direction with rounded shapes, matte textures, and a top-down perspective.

I developed six food themes and experimented with different food assets to make the experience more customisable.

### 3. Prototype Development

I used AI-assisted coding to develop the interactive prototype.

The prototype includes task creation and editing, time capacity selection, food arrangement, and exporting a completed plan.

I iterated through several prototype versions, including V4 and V5, and explored automated tests to check the functionality.

### 4. Problems Identified

One of the biggest challenges was the automatic arrangement of food.

Although the system could place food inside containers, the results sometimes looked too mechanical. Food proportions, spacing, and grouping needed further refinement.

This became the main focus of the next development stage.

## 24 October 2026 — Development Log

**Focus: Improving food arrangement and documenting the development process.**

Today, I continued exploring a more natural food arrangement system. I focused on grouping similar food items, improving spacing, and creating a more balanced composition.

I also reviewed previous project files and started organising the development history on GitHub.

**What I learned:** A layout that works technically does not necessarily produce a good visual experience. I need to consider both interaction logic and visual composition.

**Next steps:** Refine the food arrangement, test the interactive experience with a user, and document the feedback and changes.

## AI Usage and Reflection

I used AI throughout the project for brainstorming, visual exploration, asset generation, coding assistance, and testing.

AI helped me explore ideas and build prototypes more quickly. However, I found that generated results often needed significant refinement, especially in visual consistency and layout quality.

My role was to define the interaction rules, evaluate the outputs, identify problems, and decide how the design should evolve.

## User Testing

*To be completed after conducting a real user test.*

## Next Steps

- Refine the visual arrangement of food.
- Verify the final prototype's functionality.
- Conduct and document a user test.
- Prepare the final GitHub submission.


## October 25, 2026 — Plating System Evaluation

Today, I continued improving the automatic food arrangement in BENTO BOX.

Although the main interactions were working, the generated layouts still had several problems. Some food items were arranged in straight rows, others had inconsistent sizes, and the plates often looked too empty.

I used AI to test different layout approaches and analyse the results. Based on these tests, I refined four design principles:

- **Food Priority:** Main dishes should form the visual focus, supported by smaller ingredients.
- **Full Plating:** Food should fill the available space naturally without adding extra portions.
- **Size Consistency:** Different ingredients should maintain balanced visual proportions.
- **Natural Arrangement:** Similar ingredients should be grouped together without rigid grid layouts.

After several iterations, I realised that small adjustments to the existing algorithm were not enough. I decided to plan a new V7 plating system while keeping the original V5 interface, interaction rules, and food assets.

### Reflection on AI

AI helped me explore different solutions quickly, but the generated results did not always meet my design expectations. I found that giving more detailed instructions was not enough on its own. I also needed to compare the actual results, identify recurring problems, and reconsider the overall approach.

### Next Steps

- Develop six 8-hour plating examples.
- Compare the results with the visual references.
- Improve the layout algorithm based on these tests.
- Conduct user testing once the prototype is stable.

## October 25, 2026 — Plating System Development

Today, I continued improving the food arrangement system in BENTO BOX.

The previous prototype could successfully turn task durations into food portions, but the arrangement still looked too mechanical. Some food items were placed in straight rows, and the overall composition lacked balance.

I worked with AI to explore a revised version, focusing on food proportions, grouping, and different layouts for the six containers.

### Visual Development

**1. Previous Prototype**

The earlier version demonstrated the basic interaction and food arrangement, but the composition still needed improvement.

![Previous Prototype](images/Previous%20Prototype.png)

**2. Updated Prototype — October 25**

I explored new arrangements for all six food themes, aiming for more natural grouping, balanced proportions, and better use of space.

This version is still being refined, especially the automatic arrangement system.

![Updated Prototype](images/Updated%20Prototype%20%28October%2025%29.png)

**3. Plating Composition Reference**

I used this reference to study how food can be distributed more naturally within different containers.

The main focus is on spatial relationships, food grouping, and visual fullness, rather than copying the illustration style or ingredients.

![Plating Composition Reference](images/Plating%20Composition%20Reference.png)

### Reflection on AI

AI helped me generate and compare different design approaches quickly. However, I realised that creating an attractive static composition is different from developing a system that can automatically arrange food based on user input.

I still need to refine the rules and test whether the results remain visually consistent with different food combinations.

### Next Steps

- Improve the automatic plating algorithm.
- Test different food combinations and task durations.
- Compare generated results with the intended visual direction.
- Conduct user testing once the prototype is stable.

Over the past two days, I noticed several problems with the automatic food arrangement in BENTO BOX. Some ingredients appeared too large or too small, the food was sometimes arranged in straight lines, and certain areas of the plate looked too crowded while others were almost empty. The overall result did not always look like a naturally arranged meal.

Today, I mainly focused on improving these problems.

1. Adjusting Ingredient Sizes

I reviewed the sizes of all 144 ingredients and simplified the original five size categories into four: XS, S, M, and L. This helped create more consistent proportions between different foods, especially when several ingredients appeared together.

2. Improving Food Placement

I refined the arrangement rules so that the same ingredients would stay together instead of being scattered across the plate. I also adjusted the positioning logic to create more natural groupings rather than simple rows or evenly spaced grids.

3. Improving Visual Balance

I introduced composition priorities (P1–P4) to help determine which foods should become the main visual elements and which should support the arrangement. I also considered the balance of colors, food quantities, and empty space, so that the plate would look more natural at different planning capacities.

4. Using AI to Refine the Rules

I used ChatGPT to analyze the problems, organize the ingredient classifications, and write more specific instructions for Codex. During this process, I found that AI did not always apply the rules correctly, so I needed to review the generated results and make further adjustments.

This iteration helped me better understand how ingredient size, positioning, and visual composition work together. V7.1 is now the latest version of the prototype, and my next step is to explore more direct interactions with the food itself.

## October 27, 2026 — Interaction & Task Management Update

Yesterday, I focused on improving food arrangement. Today, I worked on the interaction flow and task management system.

### Key Updates
- **User Flow:** Separated Bento creation from task management.
- **My Collection:** Added In Progress and Completed categories.
- **Task Interaction:** Completed tasks remove their food from the active Bento, while the final card displays completed portions.
- **Progress:** Changed to Completed Hours / Total Planned Hours.
- **UI Refinement:** Standardised Edit buttons, improved text wrapping, and prevented duplicate task names.

### AI Reflection
I used ChatGPT to clarify interaction rules and Codex to implement changes. This helped me realise that functional features also need a clear and consistent user flow.

### Next Steps
Test the updated prototype, fix remaining issues, and conduct user testing.

## October 29, 2026 — Navigation & Interaction Refinement

Today, I focused on improving the overall user flow and task management system, preparing BENTO BOX for user testing tomorrow.

### Key Updates

- **Navigation:** Simplified the page headers by removing repeated page labels and unnecessary Home links, creating a clearer navigation structure.
- **Bento Management:** Added Rename and Delete options for both In Progress and Completed Bentos. Users can customise Bento names while keeping the automatically generated names as defaults.
- **Repeated Editing:** Adjusted the editing flow so users can save changes and reopen the same Bento multiple times. A Bento should only move to Completed when the user explicitly selects "Finish Bento".
- **Capacity Extension:** Refined the +4h mechanism. Initial planning must stay within the selected capacity (4h / 8h / 12h / 24h). The extra 4 hours should only become available when editing a saved In Progress Bento.
- **Data & Progress:** Focused on keeping task progress, Bento status, and saved information consistent across multiple editing sessions.

### AI Reflection

I used ChatGPT to review the interaction logic and organise clearer instructions for Codex. During this process, I identified several problems that were not obvious when designing individual screens, especially the difference between creating a Bento and managing it later.

This helped me understand that a working prototype needs more than functional buttons. Users also need clear navigation, predictable behaviour, and the freedom to adjust their plans.

### Next Steps

Verify the updated interactions, check for remaining bugs, and prepare for user testing on October 30. The testing will focus on whether first-time users can understand the concept, complete the planning process, and manage their Bentos without additional instructions.
