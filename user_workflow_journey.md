# UX Workflow Documentation: Three-Column Kanban Board

## Experience Mindset

The Kanban board serves users (e.g., project managers, team members) who need to visualize, manage, and track tasks across distinct phases ('To Do', 'In Progress', 'Done'). The experience encompasses scenarios such as task creation, movement, review, and accessibility for all users.

---

## User Scenarios & Minimum Viable Experience

### Scenario 1: Creating and Managing Tasks on Kanban Board

#### Scenario 1A: Standard Workflow
- **Context:** Alex, a project manager, wants to add new tasks, view them in the 'To Do' column, and move them across columns as progress is made.
- **Action:** Alex creates a task, assigns it, and updates its status by dragging it between columns.
- **Actor:** Project manager
- **Goal:** Efficiently visualize and update task status across project stages.

#### Scenario 1B: Accessible Workflow (Keyboard Navigation)
- **Context:** Jamie, a team member with limited mobility, needs to manage tasks using keyboard navigation and screen reader support.
- **Action:** Jamie creates, selects, and moves tasks using keyboard shortcuts and receives ARIA label announcements.
- **Actor:** Team member (accessibility needs)
- **Goal:** Manage tasks without mouse, ensuring accessibility compliance.

---

### Scenario 2: Responsive Use Across Devices

#### Scenario 2A: Mobile Workflow
- **Context:** Sam, a developer, checks project status and updates tasks on a mobile device during commute.
- **Action:** Sam views the Kanban board in a stacked layout, adds tasks, and moves them between columns using touch gestures.
- **Actor:** Developer (mobile user)
- **Goal:** Quickly view and update tasks on-the-go.

#### Scenario 2B: Tablet/Desktop Workflow
- **Context:** Maria, a QA lead, reviews tasks and moves them between columns on her desktop and tablet.
- **Action:** Maria interacts with the board using drag-and-drop or keyboard navigation, with columns displayed horizontally.
- **Actor:** QA lead
- **Goal:** Efficient task management with optimal screen real estate.

---

## User & Business Goals

- **User Goal:** Enable users to create, view, and manage tasks efficiently, with accessible and responsive design for all devices and abilities.
- **Business Goal:** Improve team productivity, ensure inclusivity, and provide scalable design assets compatible with Angular applications.

---

## Workflow Design Variations (for each scenario)

### Scenario 1: Creating and Managing Tasks

#### Variation 1: Drag-and-Drop Workflow
1.0 Kanban Board Homepage
  - **Goal:** Provide overview of all tasks and columns.
  - **Description:** User sees three columns ('To Do', 'In Progress', 'Done') horizontally. Each column header is visually distinct and accessible.
  - **Design Problems:** HMW help users quickly identify task status? HMW ensure visual separation is clear?
  - **Design Opportunities:** What if column headers are color-coded and have ARIA labels?

2.0 Task Creation Modal (Pu.1)
  - **Goal:** Allow user to create a new task.
  - **Description:** Modal pops up with fields for task name, description, assignee, and initial column selection.
  - **Design Problems:** HMW minimize friction in task creation? HMW ensure modal is accessible?
  - **Design Opportunities:** What if modal supports keyboard shortcuts and focus management?

3.0 Task Card in 'To Do' Column
  - **Goal:** Display newly created task.
  - **Description:** Task card appears in 'To Do' column; user can drag card to other columns.
  - **Design Problems:** HMW make drag-and-drop intuitive? HMW provide feedback for movement?
  - **Design Opportunities:** What if card changes color or animates on move?

4.0 Task Card in 'In Progress'/'Done' Columns
  - **Goal:** Update task status visually and functionally.
  - **Description:** Task card moves to respective column; status updates.
  - **Design Problems:** HMW ensure status is clear for all users?
  - **Design Opportunities:** What if status change triggers notification or ARIA update?

#### Variation 2: Keyboard Navigation Workflow
1.0 Kanban Board Homepage
  - **Goal:** Provide accessible overview of tasks and columns.
  - **Description:** Columns are navigable via keyboard; focus states are visually distinct.
  - **Design Problems:** HMW ensure focus is obvious? HMW support ARIA labeling?
  - **Design Opportunities:** What if each column header is announced by screen reader?

2.0 Task Creation via Keyboard Shortcut (Pu.1)
  - **Goal:** Enable task creation without mouse.
  - **Description:** User presses shortcut to open modal, fills fields, and submits.
  - **Design Problems:** HMW design shortcut system? HMW ensure modal is accessible?
  - **Design Opportunities:** What if modal auto-focuses first input?

3.0 Task Movement via Keyboard
  - **Goal:** Move tasks between columns using keyboard.
  - **Description:** User selects task, uses arrow keys to shift column.
  - **Design Problems:** HMW provide feedback for movement? HMW update ARIA status?
  - **Design Opportunities:** What if movement triggers audible feedback?

---

### Scenario 2: Responsive Use Across Devices

#### Variation 1: Mobile Workflow
1.0 Kanban Board Mobile View
  - **Goal:** Adapt layout for small screens.
  - **Description:** Columns stack vertically; cards are swipeable.
  - **Design Problems:** HMW maintain clarity in stacked layout? HMW support touch gestures?
  - **Design Opportunities:** What if swipe gestures move tasks?

2.0 Task Creation Mobile Modal (Pu.1)
  - **Goal:** Create tasks on mobile.
  - **Description:** Modal is full-screen, large touch targets.
  - **Design Problems:** HMW ensure modal is easy to use? HMW support accessibility?
  - **Design Opportunities:** What if modal supports voice input?

#### Variation 2: Tablet/Desktop Workflow
1.0 Kanban Board Desktop View
  - **Goal:** Maximize horizontal space.
  - **Description:** Columns are horizontal, drag-and-drop supported.
  - **Design Problems:** HMW optimize for larger screens? HMW support both mouse and keyboard?
  - **Design Opportunities:** What if columns can be resized?

2.0 Task Creation Desktop Modal (Pu.1)
  - **Goal:** Create tasks efficiently.
  - **Description:** Modal is centered, supports keyboard and mouse.
  - **Design Problems:** HMW support quick input? HMW ensure accessibility?
  - **Design Opportunities:** What if modal remembers last input?

---

## Accessibility & Scalability Considerations

- ARIA labels for all column headers and task cards
- Focus states for keyboard navigation
- Color contrast meeting WCAG standards
- Responsive breakpoints for mobile (320px-767px), tablet (768px-1023px), desktop (1024px+)
- Design tokens for spacing, colors, typography
- Keyboard shortcuts for all major actions
- Screen reader announcements for status changes

---

## Sequence of Screens (Example Workflow)

### Drag-and-Drop Workflow
1.0 Kanban Board Homepage -> 2.0 Task Creation Modal (Pu.1) -> 3.0 Task Card in 'To Do' Column -> 4.0 Task Card in 'In Progress'/'Done' Columns

### Keyboard Navigation Workflow
1.0 Kanban Board Homepage -> 2.0 Task Creation via Keyboard Shortcut (Pu.1) -> 3.0 Task Movement via Keyboard

### Mobile Workflow
1.0 Kanban Board Mobile View -> 2.0 Task Creation Mobile Modal (Pu.1)

### Tablet/Desktop Workflow
1.0 Kanban Board Desktop View -> 2.0 Task Creation Desktop Modal (Pu.1)

---

## Design Problems & Opportunities (Summary)

- HMW help users quickly identify and manage tasks?
- HMW ensure accessibility for all users?
- HMW support responsive layouts without losing context?
- What if the board provides real-time feedback and notifications?
- What if accessibility features are customizable?
- What if design tokens enable easy theme and layout updates?

---

## Business Alignment

- Comprehensive design specs for Kanban board
- Responsive and accessible layouts
- Design tokens compatible with Angular
- User-centric workflows for all scenarios
- Documentation ready for review and implementation
