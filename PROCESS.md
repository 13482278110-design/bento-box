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

---

## 04. User Testing — October 30, 2026

**Focus: Observing first-time use and refining the prototype into V8.**

I conducted a first-time-use testing session to see whether the concept and main workflow were understandable without additional explanation. I observed the Welcome and Home transition, Bento creation, capacity selection, task management, progress tracking, and Collection.

### Observed Problems

- The purpose of BENTO BOX was not immediately clear. The relationship between a task, a food type, and its portions needed a more direct explanation.
- Welcome and Home felt too similar, so it was unclear whether **Start Packing** and **Create a Bento** performed the same action.
- Progress was too rigid. A long task could only be treated as unfinished or fully completed, even when only some planned hours were done.
- Capacity guidance was easy to miss, especially the rule that one portion represents one hour and that the Bento does not need to be completely filled.
- Repeated status labels and five summary statistics made the task-management screen harder to scan.
- During later V8 quality checks, the **Completed** tab in My Collection sometimes required more than one click, which made the interface feel unreliable.

### Changes Made in V8

**1. Clearer onboarding and navigation**

- Kept Welcome and Home as separate stages. Welcome explains the idea; **Start Packing** enters Home; **Create a Bento** begins planning.
- Added a compact three-step guide using the existing container and food assets: choose time, pack tasks, and track progress.
- Kept Home and the BENTO BOX logo as consistent routes back to the dashboard, and added a direct route back from the result page.

**2. Progress by hour**

- Replaced all-or-nothing task completion with `+` and `−` controls for completed hours.
- Kept the rule **one portion = one hour**, so an eight-hour task can show progress such as 4/8 without creating fractional food.
- Calculated task and Bento progress from completed hours while keeping **Finish Bento** as a separate, explicit action.
- Saved partial progress with the existing Bento record so it can be restored when the plan is reopened.

**3. Clearer information hierarchy**

- Reduced the main summary to **Planned**, **Completed**, and **Remaining**.
- Kept Original Goal and Maximum Capacity as smaller contextual indicators.
- Moved **Available** capacity into the Add/Edit Task area, where it affects the user's decision.
- Removed redundant “Not started” and “Done” labels because the TO DO and DONE sections already communicate status.
- Added concise capacity instructions using the same “one portion = one hour” terminology as the Welcome page.

**4. Interaction reliability**

- Refined the Collection tab interaction so the whole visible tab area responds consistently.
- Preserved saved Bento data, explicit In Progress/Completed states, and the existing food arrangement system while making these interface changes.

### Testing Outcome

The test changed my priorities. Instead of adding more features, I focused on explaining the existing concept, supporting realistic partial progress, and reducing unnecessary interface information. V8 keeps the original visual identity and planning metaphor while making the main actions and states easier to understand.

---

## 05. AI Usage & Reflection

AI supported ideation, visual exploration, requirement writing, implementation, and debugging, but I remained responsible for selecting, testing, and revising the results.

### Tools and Uses

- **ChatGPT:** brainstorming, interface critique, clarifying interaction rules, and turning feedback into structured implementation requirements.
- **AI-assisted image generation:** exploring the food illustration direction and producing visual assets that were then selected and refined for this project.
- **Codex:** implementing and debugging the HTML, CSS, JavaScript, plating logic, local storage, task management, and export behaviour.

### Decisions I Accepted, Modified, or Rejected

I accepted the AI-assisted suggestion to separate saving a plan from finishing it. This became the distinction between **In Progress** and **Completed**, with an explicit **Finish Bento** action. It gave users more control and allowed the same Bento to be reopened and edited.

I modified or rejected several early AI-generated plating solutions. Fixed grids, uniform scaling, and widely separated food groups were technically valid but visually weak. I replaced these results with my own rules for XS–L ingredient sizes, P1–P4 visual priorities, same-food grouping, container-aware boundaries, and compact composition. I also rejected interface changes when they added duplicate labels or made existing interactions less predictable.

These examples showed me that AI output is a proposal, not a final design decision. Detailed prompts helped, but visual judgement, user testing, regression checks, and repeated adjustment were still necessary.

---

## 06. Final Reflection

BENTO BOX taught me that interaction design is not only about making features work. The visual metaphor must be explained clearly, state changes must be predictable, and the interface must support how people actually complete work. User testing revealed problems that were difficult to notice while designing alone, especially the confusing Welcome/Home relationship and the need to record partial hours.

AI helped me explore and implement ideas quickly, but it also produced layouts and interactions that looked complete before they were truly usable. My role was to set the rules, compare outputs, reject weak solutions, and protect the coherence of the experience. The final prototype is stronger because visual design, interaction logic, testing, and AI-assisted development were treated as one iterative process.

---

## 07. Credits & References

- The 144 food illustrations and six container designs were developed for BENTO BOX through AI-assisted visual exploration and iterative art direction. I selected, reviewed, processed, and integrated the assets into the final interface.
- The **Plating Composition Reference** was generated with AI during visual exploration. It was used to study food grouping, spacing, and composition rather than as a final asset.
- ChatGPT was used for ideation, critique, and requirement development. Codex was used for implementation and debugging support.
- The October 30 findings in this document come from the project’s first-time-use testing session and the subsequent V8 refinement process. No participant quotes or performance statistics have been added because they were not recorded.
