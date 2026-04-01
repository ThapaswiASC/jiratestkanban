# UX Workflow Documentation: Three-Column Kanban Board

## Experience Mindset
The Kanban board experience focuses on visualizing work, tracking progress, and managing tasks efficiently across devices. Users interact with the board to organize, move, and review tasks while businesses aim for productivity, clarity, and accessibility compliance.

---

## Identified Scenarios

### Scenario 1: User views and manages tasks on the Kanban board (core workflow)
#### Context:
*User*: Project Manager or Team Member
*Situation*: Needs to visualize and update the status of tasks in a sprint
*Action*: Views the board, drags and drops cards between columns, checks task details
*Actor*: User (Project Manager/Team Member)
*Goal*: Efficiently track and update task progress across devices

#### User Goal
To easily visualize, update, and manage tasks across different workflow stages (To Do, In Progress, Done) with minimal friction and maximum clarity.

#### Business Goal
To ensure team productivity, transparency, and compliance with accessibility standards while supporting scalability and device responsiveness.

---

### Scenario 1A: Workflow Variation – Drag-and-Drop Interaction
- User drags cards between columns to update status.
- Focus on mouse/touch interaction and visual feedback.

#### Scenario 1B: Workflow Variation – Keyboard Navigation
- User navigates and moves cards using keyboard shortcuts (Tab, Arrow keys, Space/Enter).
- Focus on accessibility and ARIA compliance.

---

### Scenario 2: User customizes Kanban board layout (advanced workflow)
#### Context:
*User*: Scrum Master or Admin
*Situation*: Wants to adjust column order, rename columns, or change color schemes for clarity
*Action*: Accesses board settings, applies changes, and reviews updated board
*Actor*: User (Scrum Master/Admin)
*Goal*: Personalize the board to fit team needs and improve clarity

#### User Goal
To tailor the Kanban board for specific team workflows without losing usability or accessibility.

#### Business Goal
To support a scalable, flexible product that adapts to various team requirements while maintaining brand consistency and accessibility.

---

### Scenario 2A: Workflow Variation – UI-based Customization
- User interacts with a settings modal/panel to reorder columns and change color schemes.

#### Scenario 2B: Workflow Variation – Accessibility-first Customization
- User customizes columns using a keyboard-accessible interface with full ARIA support and live preview.

---

## Minimum Viable Experience

### User Scenario
Jordan, a team member, opens the Kanban board to review daily tasks. They want to move a task from "To Do" to "In Progress" and check task details on their tablet. The interface must be clear, responsive, and accessible, allowing both drag-and-drop and keyboard navigation.

---

## Screen List & Workflow Details

### 1.0 Kanban Board Overview
- **Page Goal:** Present an at-a-glance view of all tasks organized by status
- **Screen Description:**
    - Three columns: To Do, In Progress, Done
    - Cards display task name, assignee, and priority
    - Board adapts to mobile, tablet, desktop
    - Visual separators, color-coded headers, and clear typography
    - ARIA labels for column headers and cards
- **Design Problems:**
    - HMW ensure clarity across breakpoints without clutter?
    - HMW communicate column purpose to screen readers?
    - HMW maintain visual separation and focus states?
- **Design Opportunities:**
    - What if the board can collapse columns on mobile for focus?
    - What if users can filter or search tasks inline?

### 2.0 Task Card Details (Modal/Drawer)
- **Page Goal:** Show detailed task information and allow quick edits
- **Screen Description:**
    - Opens on card click or keyboard selection
    - Displays description, assignee, due date, comments
    - Accessible close button and focus management
- **Design Problems:**
    - HMW prevent context loss when opening details?
    - HMW support both mouse and keyboard access?
- **Design Opportunities:**
    - What if the modal supports quick status change?
    - What if comments auto-save with keyboard shortcuts?

### 3.0 Board Customization (Settings Modal/Panel)
- **Page Goal:** Allow users to personalize board layout and appearance
- **Screen Description:**
    - Reorder columns, rename, change colors
    - Live preview and reset option
    - Fully accessible with ARIA and keyboard navigation
- **Design Problems:**
    - HMW balance customization with simplicity?
    - HMW ensure accessibility in advanced settings?
- **Design Opportunities:**
    - What if board presets are available for common workflows?
    - What if users can export/import settings?

### Pu.1 Confirmation Pop-Up
- **Page Goal:** Confirm actions (e.g., move task, save customization)
- **Screen Description:**
    - Accessible, focus-trapped pop-up with clear messaging
- **Design Problems:**
    - HMW avoid accidental actions?
    - HMW ensure pop-ups are accessible to all users?
- **Design Opportunities:**
    - What if undo is offered directly in the pop-up?

### Er.1 Error State
- **Page Goal:** Communicate errors (e.g., failed move, save)
- **Screen Description:**
    - Inline or toast message with accessible announcement
- **Design Problems:**
    - HMW provide actionable error messages?
    - HMW ensure errors are announced to screen readers?
- **Design Opportunities:**
    - What if error messages suggest immediate fixes?

---

## Workflow Sequences

### Scenario 1A: Drag-and-Drop
1.0 Kanban Board Overview → Drag card → Pu.1 Confirmation Pop-Up → 2.0 Task Card Details (optional)

### Scenario 1B: Keyboard Navigation
1.0 Kanban Board Overview → Keyboard select card → Move card with keys → Pu.1 Confirmation Pop-Up → 2.0 Task Card Details (optional)

### Scenario 2A: UI-based Customization
1.0 Kanban Board Overview → 3.0 Board Customization → Pu.1 Confirmation Pop-Up → 1.0 Kanban Board Overview

### Scenario 2B: Accessibility-first Customization
1.0 Kanban Board Overview → 3.0 Board Customization (keyboard/ARIA) → Pu.1 Confirmation Pop-Up → 1.0 Kanban Board Overview

---

## Accessibility & Scalability Notes
- All interactive elements have ARIA labels and focus states
- Responsive breakpoints: Mobile (320-767px), Tablet (768-1023px), Desktop (1024px+)
- Keyboard navigation for all actions
- Design tokens for spacing, color, typography
- Error and confirmation states are accessible and announced
- Customization supports both mouse/touch and keyboard users

---

## Summary
This workflow documentation provides multiple user-centered journey variations for Kanban board interaction and customization, balancing user needs with business goals, accessibility, and scalability. It is structured to guide future design, development, and testing for a robust, inclusive Kanban experience.
