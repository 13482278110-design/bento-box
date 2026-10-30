# Development Process — BENTO BOX

## 01. Project Overview

BENTO BOX is an interactive time-planning experience that transforms daily tasks into food arrangements. Each food portion represents one hour of work, allowing users to organise their time by creating a personalised bento box.

The project explores how a playful visual metaphor can make planning more engaging and encourage users to interact with their daily schedules in a different way.

This document records the development process, design iterations, challenges, AI-assisted workflow, and user testing.

---

## 02. Early Development — Concept & Prototype

*This section summarises the work completed before I started documenting the project on GitHub on October 24, 2026.*

### Concept Development

I began by exploring how to turn a traditional to-do list into a more playful and visual experience.

Instead of entering tasks into a standard list, users select food items, assign task names and durations, and arrange their time inside a bento box.

The main interaction rule is simple:

**One food portion = One hour of work.**

I also introduced different container sizes to represent different planning capacities.

### Visual Exploration

I experimented with different illustration styles before choosing a soft, semi-3D visual direction with rounded shapes, matte textures, and a consistent top-down perspective.

I developed six bento themes, each with its own food assets and container design.

### Initial Prototype

With AI-assisted coding, I developed early interactive prototypes, including V4 and V5.

These versions established the basic functions:

- Selecting a bento theme and time capacity
- Adding and editing tasks
- Converting task durations into food portions
- Automatically arranging food
- Generating and exporting a bento card

### Initial Challenges

The main challenge was the automatic food arrangement.

Although the prototype could place food inside containers, the results often looked too mechanical. Some ingredients were arranged in straight rows, while others had inconsistent sizes or left too much empty space.

This led me to focus on improving the visual arrangement system.

---

## 03. Development Log

### October 24, 2026 — Food Arrangement Exploration

**Focus: Improving visual composition and documenting the development process.**

I continued exploring ways to make food arrangements look more natural.

I focused on grouping similar ingredients, improving spacing, and creating more balanced compositions within different containers.

I also started organising the development history and project files on GitHub.

**What I Learned**

A technically functional layout does not always create a good visual experience. The arrangement system needs to consider visual balance as well as interaction rules.

### October 25, 2026 — Plating System Development

**Focus: Food proportions, grouping, and natural arrangement.**

I evaluated the previous prototype and identified several recurring problems:

- Some food items appeared too large or too small.
- Ingredients were often arranged in straight rows.
- Similar ingredients were scattered across the container.
- Some areas looked overcrowded while others remained empty.

I realised that small adjustments to the existing layout algorithm were not enough. I decided to develop a revised V7 plating system while keeping the original interface, interaction rules, and food assets.

#### Visual Comparison

**Previous Prototype**

The earlier version demonstrated the basic interaction system, but the food composition still needed improvement.

![Previous Prototype](images/Previous%20Prototype.png)

**Updated Prototype — October 25**

I explored new arrangements across all six themes, focusing on more natural grouping, consistent proportions, and better use of space.

![Updated Prototype](images/Updated%20Prototype%20%28October%2025%29.png)

**Plating Composition Reference**

I used this reference to study food distribution, spatial relationships, and visual fullness rather than copying its illustration style.

![Plating Composition Reference](images/Plating%20Composition%20Reference.png)

#### Key Improvements

**1. Ingredient Size Classification**

I reviewed the proportions of 144 food assets and simplified the original five size categories into four: XS, S, M, and L.

This helped establish more consistent visual relationships between ingredients.

**2. Food Placement**

I refined the placement rules to keep similar ingredients together and reduce rigid rows or grid-like arrangements.

**3. Visual Composition**

I introduced composition priorities (P1–P4) to distinguish main visual elements from supporting ingredients.

I also considered food quantities, colour balance, and empty space across different container sizes.

**4. AI-Assisted Iteration**

I used ChatGPT to analyse visual problems and organise clearer requirements for Codex.

However, the generated results did not always follow the intended rules, so I repeatedly compared the output with my design references and adjusted the instructions.

#### Outcome & Reflection

This iteration led to the V7.1 prototype and a clearer understanding of how ingredient size, positioning, and visual composition affect the overall experience.

I also learned that creating an attractive static image is different from building a system that can automatically generate balanced arrangements from different user inputs.

### October 27, 2026 — Interaction & Task Management

**Focus: Improving the user flow beyond the initial Bento creation process.**

After focusing on visual arrangement, I shifted my attention to how users manage their tasks after generating a Bento.

#### Key Updates

- **User Flow:** Separated Bento creation from ongoing task management.
- **My Collection:** Introduced In Progress and Completed categories.
- **Task Interaction:** Adjusted food visibility to reflect task completion and progress.
- **Progress Tracking:** Changed the progress display to Completed Hours / Total Planned Hours.
- **UI Refinement:** Standardised Edit buttons, improved text wrapping, and added duplicate task-name validation.

#### Reflection

I used ChatGPT to clarify the interaction rules and Codex to support implementation.

This process helped me realise that functional features are not enough on their own. They also need to form a clear and consistent experience across different stages of use.

### October 29, 2026 — Navigation & Editing Refinement

**Focus: Improving usability and preparing for user testing.**

I reviewed the overall experience and identified several issues related to navigation, saved Bentos, and repeated editing.

#### Key Updates

- **Navigation:** Simplified page headers by removing redundant labels and unnecessary Home links.
- **Bento Management:** Added Rename and Delete options for saved Bentos.
- **Repeated Editing:** Refined the flow so users can save changes and reopen an In Progress Bento without automatically finishing it.
- **Finish Bento:** Defined an explicit action for moving a Bento to Completed.
- **Capacity Extension:** Revised the +4h mechanism so extra capacity is available only when editing an existing In Progress Bento, not during initial planning.
- **Data Consistency:** Focused on preserving task progress, Bento status, and saved information across editing sessions.

#### Reflection

I used ChatGPT to review the interaction logic, identify inconsistencies, and organise clearer implementation instructions for Codex.

One important discovery was that creating a Bento and managing an existing Bento require different interaction rules.

For example, the +4h mechanism should help users adjust an existing plan rather than increase the capacity during initial planning.

This iteration made me pay more attention to predictable behaviour, user control, and the relationship between different parts of the experience.

Some updated interactions still need to be verified in the final prototype.

---

## 04. AI Usage & Reflection

AI played an important role throughout the development of BENTO BOX, but it did not replace my design decisions.

### How I Used AI

**ChatGPT**

I used ChatGPT for brainstorming, analysing design problems, refining interaction rules, organising requirements, and reviewing the development process.

**AI Image Generation**

I used AI-assisted visual exploration and asset generation to develop the food illustration direction and experiment with different arrangements.

**Codex**

I used Codex to support the implementation and refinement of the interactive prototype, including layout logic, task management, and interface behaviour.

### What Worked Well

AI helped me move from an initial concept to an interactive prototype more quickly.

It also allowed me to experiment with different solutions without having to build every variation manually.

### Challenges & Limitations

AI-generated results were not always consistent with my intentions.

For example, the automatic plating system could follow basic placement instructions but still produce unnatural compositions.

Some interaction changes also introduced unexpected behaviour or affected existing functions.

I learned that detailed prompts alone do not guarantee good results. I still needed to review the outputs, identify problems, test the interactions, and decide which changes were necessary.

### My Role in the Process

My main responsibility was to define the concept, establish design rules, evaluate AI-generated results, and guide each iteration.

Through this project, I learned that AI-assisted programming still requires an understanding of interaction logic, visual consistency, and how different functions affect one another.

---

## 05. User Testing

*Planned for October 30, 2026.*

The next step is to test BENTO BOX with a first-time user.

The test will focus on whether users can:

- Understand the concept of converting time into food portions
- Create a Bento without additional instructions
- Understand the capacity limits
- Find and manage saved Bentos
- Edit tasks and track progress
- Understand when a Bento is considered completed

I will record the user's actions, difficulties, and feedback, then document any changes made in response.

*Testing observations and results will be added after the session.*

---

## 06. Next Steps

- Verify the latest navigation and editing interactions.
- Check the capacity extension and saved-data behaviour.
- Conduct user testing and document the results.
- Fix any remaining issues identified during testing.
- Confirm that the GitHub Pages version matches the final prototype.
- Complete the final submission.

---

## 07. Final Reflection

*To be completed after user testing and final development.*

The final reflection will summarise what I learned from building an interactive experience with AI-assisted programming, including the relationship between design decisions, implementation, and user feedback.

## October 30, 2026 — User Testing & V8 Refinement

**Focus:** Improving usability, interaction feedback, and information clarity based on real user testing.

### 1. User Testing

Conducted user testing to evaluate whether first-time users could understand and interact with BENTO BOX.

Key findings:
- Some users did not immediately understand the purpose of the product or how the food-based time planning system worked.
- Users needed more flexibility to record partial task completion rather than marking an entire task as finished.
- The transition between Welcome and Home was confusing.
- Some interface labels and statistics were repetitive or unnecessarily complex.

### 2. Onboarding & Navigation

- Refined the Welcome page to explain the core concept: one food portion represents one hour.
- Added a three-step introduction to help users understand the planning process.
- Improved the navigation structure between Welcome, Home, Bento creation, and Collection.
- Added a more accessible way to return Home after generating a Bento.

### 3. Task Management

- Introduced incremental task progress tracking using +/− controls.
- Allowed users to record completed hours without finishing an entire task.
- Updated Bento progress and remaining hours to reflect task completion.
- Simplified task information by removing redundant status labels.

### 4. Information Hierarchy

- Reduced the main statistics from five categories to three: Planned, Completed, and Remaining.
- Kept original goals and maximum capacity information in smaller indicators.
- Moved available capacity information closer to task creation and editing.
- Improved consistency between the initial planning interface and saved Bento management.

### 5. Interaction & Performance Review

- Identified intermittent click-response issues, particularly when switching between In Progress and Completed in My Collection.
- Reviewed possible rendering and interaction performance problems.
- Prioritized responsiveness, stable food placement, and reliable task updates for the final refinement stage.

### Next Steps

- Verify and fix remaining interaction bugs.
- Complete browser testing and confirm saved data works correctly.
- Update the GitHub Pages deployment to the final V8 version.
- Finalize documentation and submission materials.
