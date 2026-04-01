# UX Workflow Documentation: Three-Column Kanban Board

## Experience Mindset

**User:** Project Manager, Team Member, QA Analyst

**Experience:** Task Management, Progress Tracking, Collaboration, Accessibility

---

### SCENARIO 1: Viewing and Navigating the Kanban Board

#### Scenario A: Project Manager accesses the Kanban board to get an overview of task progress
- **Context:** Project Manager logs in and lands on the Kanban board dashboard.
- **Action:** Views all tasks across 'To Do', 'In Progress', and 'Done' columns.
- **Actor:** Project Manager
- **Goal:** Quickly and accurately assess project status and bottlenecks.

#### Scenario B: Team Member uses keyboard navigation and screen reader to access Kanban board
- **Context:** Team Member with accessibility needs logs in and uses assistive technology.
- **Action:** Navigates columns and cards using keyboard and screen reader.
- **Actor:** Team Member
- **Goal:** Efficiently access and understand task information without barriers.

---

## Workflow Design Variations

### Workflow 1: Standard Visual Navigation
- **User Goal:** To easily view and understand the status of tasks across the project.
- **Business Goal:** To increase transparency and accountability in task progress.

#### Screens:

##### 1.0 Kanban Board Overview
- **Page Goal:** Present a clear, accessible layout of all tasks and columns.
- **Screen Description:**
  - Three horizontally aligned columns: 'To Do', 'In Progress', 'Done'.
  - Column headers styled with distinct colors (as per design tokens).
  - Cards show task title, assignee, and status.
  - Responsive breakpoints: mobile (single column scroll), tablet (two columns), desktop (three columns).
- **Design Problems:**
  - HMW ensure columns remain visually distinct across breakpoints?
  - HMW surface key task info without clutter?
- **Design Opportunities:**
  - What if users can customize column order?
  - What if board auto-highlights overdue tasks?

##### 1.1 Card Details Pop-Up (Pu.1)
- **Page Goal:** Provide in-depth task details without leaving the board.
- **Screen Description:**
  - Pop-up triggered by clicking a card.
  - Includes task description, due date, comments, and attachments.
- **Design Problems:**
  - HMW ensure pop-up is accessible (focus management, ARIA labels)?
- **Design Opportunities:**
  - What if pop-up supports quick actions (mark as done, assign)?

##### Er.1 Error State: Board Load Failure
- **Page Goal:** Inform user of loading issues and offer retry.
- **Screen Description:**
  - Error message with retry button.
- **Design Problems:**
  - HMW make error actionable and not frustrating?
- **Design Opportunities:**
  - What if error state suggests offline mode?

##### Sequence:
1.0 Kanban Board Overview → 1.1 Card Details Pop-Up → Er.1 Error State

---

### Workflow 2: Accessible Navigation (Keyboard/Screen Reader)
- **User Goal:** To allow users with disabilities to navigate the Kanban board efficiently.
- **Business Goal:** To meet accessibility standards and broaden user base.

#### Screens:

##### 2.0 Accessible Kanban Board
- **Page Goal:** Ensure full accessibility for board navigation and task interaction.
- **Screen Description:**
  - Columns and cards have ARIA labels.
  - Keyboard navigation (Tab, Arrow keys) supported.
  - Focus states clearly visible.
  - Screen reader announces column headers and card info.
- **Design Problems:**
  - HMW support screen reader announcements for dynamic content?
  - HMW maintain usability for both mouse and keyboard users?
- **Design Opportunities:**
  - What if board offers personalized accessibility settings?

##### 2.1 Keyboard Navigation Help Pop-Up (Pu.2)
- **Page Goal:** Guide users on keyboard shortcuts and accessibility features.
- **Screen Description:**
  - Pop-up with shortcut list and accessibility tips.
- **Design Problems:**
  - HMW make help easily discoverable but not intrusive?
- **Design Opportunities:**
  - What if help adapts to user's device/context?

##### Er.2 Error State: Accessibility Feature Failure
- **Page Goal:** Alert user if accessibility features (ARIA, keyboard nav) fail.
- **Screen Description:**
  - Clear error message with contact support option.
- **Design Problems:**
  - HMW make accessibility errors actionable?
- **Design Opportunities:**
  - What if error logs auto-send to support?

##### Sequence:
2.0 Accessible Kanban Board → 2.1 Keyboard Navigation Help Pop-Up → Er.2 Error State

---

### Minimum Viable Experience (MVE)

#### Scenario: New User discovers and interacts with Kanban board
- **Context:** New user logs in for the first time.
- **Action:** Views board, clicks a card, tries keyboard navigation.
- **Actor:** New User
- **Goal:** Understand board layout and interact with tasks.

#### Workflow:
- 1.0 Kanban Board Overview
- 1.1 Card Details Pop-Up
- 2.0 Accessible Kanban Board
- 2.1 Keyboard Navigation Help Pop-Up

---

## User and Business Goals
- **User Goal:** To enable users to manage tasks visually and accessibly.
- **Business Goal:** To drive project efficiency, inclusivity, and compliance.

---

## List of Screens and Numbering
- 1.0 Kanban Board Overview
- 1.1 Card Details Pop-Up (Pu.1)
- Er.1 Error State: Board Load Failure
- 2.0 Accessible Kanban Board
- 2.1 Keyboard Navigation Help Pop-Up (Pu.2)
- Er.2 Error State: Accessibility Feature Failure

---

## Design Problems & Opportunities
- HMW maintain distinct columns across devices?
- HMW support both visual and accessible navigation?
- HMW make error states actionable?
- What if board offers customizable layouts?
- What if accessibility settings are user-specific?

---

## Accessibility & Scalability
- ARIA labels for columns/cards
- Focus states for keyboard navigation
- Responsive breakpoints (mobile/tablet/desktop)
- Design tokens for consistent spacing, colors, typography
- Error handling for accessibility features

---

## Summary Sequence for Each Scenario/Workflow

**Workflow 1:**
1.0 Kanban Board Overview → 1.1 Card Details Pop-Up → Er.1 Error State

**Workflow 2:**
2.0 Accessible Kanban Board → 2.1 Keyboard Navigation Help Pop-Up → Er.2 Error State

**Minimum Viable Experience:**
1.0 Kanban Board Overview → 1.1 Card Details Pop-Up → 2.0 Accessible Kanban Board → 2.1 Keyboard Navigation Help Pop-Up
