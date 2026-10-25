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
