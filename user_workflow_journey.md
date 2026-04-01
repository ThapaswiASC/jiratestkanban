# UX User Workflow Documentation: Three-Column Kanban Board

## Experience Mindset

The Kanban board is a core productivity and workflow management tool for users managing tasks. The experience includes scenarios such as viewing tasks, updating task status, and adapting to different devices (desktop, tablet, mobile). Accessibility and scalability are foundational to the experience.

---

## 1. SCENARIOS & WORKFLOW VARIATIONS

### Scenario 1: User views and interacts with the Kanban board on desktop

**Variation A:** Standard interaction (mouse/trackpad)
**Variation B:** Keyboard-only navigation (accessibility focus)

#### Scenario Context:
- User: Project manager or team member
- Situation: Needs to view, update, and manage tasks for a project
- Action: Views Kanban board, moves tasks between columns, checks status
- Actor: User (with/without accessibility needs)
- Goal: Efficiently manage and update tasks

#### User Goal
- To view all tasks clearly and move them between columns quickly and accurately

#### Business Goal
- To maximize team productivity and ensure all users (including those with disabilities) can efficiently use the Kanban board

##### Workflow 1A: Mouse/Trackpad (Standard)

1.0 Kanban Board Home
- **Page Goal:** Present a clear, organized view of all tasks by status
- **Description:**
  - Board displays three columns: 'To Do', 'In Progress', 'Done'
  - Each column has a header, colored and labeled
  - Tasks (cards) are shown under appropriate columns
  - Visual separators between columns
  - Responsive to window resizing
- **Design Problems:**
  - HMW keep the interface clutter-free with many tasks?
  - HMW visually distinguish columns while maintaining harmony?
- **Design Opportunities:**
  - What if columns can be collapsed/expanded?
  - What if the user can customize column colors?

1.1 Task Card Details Pop-Up (Pu.1)
- **Page Goal:** Show task information without leaving the board
- **Description:**
  - Clicking a card opens details in a modal/pop-up
  - Allows editing task info
- **Design Problems:**
  - HMW prevent users from losing context?
- **Design Opportunities:**
  - What if pop-up is draggable?

1.2 Drag-and-Drop Interaction
- **Page Goal:** Allow intuitive task movement
- **Description:**
  - User drags card to new column
  - Visual feedback shows drop target
- **Design Problems:**
  - HMW ensure accessible drag-and-drop?
- **Design Opportunities:**
  - What if undo/redo is available?

Er.1 Error: Failed to Move Task
- **Goal:** Alert user to action failure, provide recovery
- **Description:**
  - Toast or modal with error message

##### Workflow 1B: Keyboard-Only Navigation

1.0 Kanban Board Home (with focus indicators)
- **Page Goal:** Same as above
- **Description:**
  - All interactive elements reachable via Tab
  - ARIA labels on columns and cards
  - Focus states visually clear
- **Design Problems:**
  - HMW ensure efficient keyboard navigation order?
- **Design Opportunities:**
  - What if user can jump between columns with shortcuts?

1.1 Card Actions Menu (Pu.2)
- **Page Goal:** Manage card without mouse
- **Description:**
  - Pressing Enter/Space opens menu for move/edit/delete
  - All menu items accessible via arrow keys

Er.2 Accessibility Alert
- **Goal:** Inform user of inaccessible actions
- **Description:**
  - Screen reader and visual message if action not possible

##### Sequence Example:
1.0 Kanban Board Home → 1.1 Task Card Details Pop-Up → 1.2 Drag-and-Drop Interaction → Er.1 Error: Failed to Move Task

---

### Scenario 2: User accesses Kanban board on mobile/tablet (responsive behavior)

**Variation A:** Mobile portrait
**Variation B:** Tablet landscape

#### Scenario Context:
- User: Team member on the go
- Situation: Needs to check/update tasks from mobile device
- Action: Views Kanban board, interacts with tasks
- Actor: User
- Goal: Access and manage tasks efficiently on small screens

#### User Goal
- To quickly check and update tasks from any device

#### Business Goal
- To provide a seamless, scalable Kanban experience across all devices

##### Workflow 2A: Mobile Portrait

2.0 Kanban Board Mobile View
- **Page Goal:** Present Kanban in a single-column scrollable layout
- **Description:**
  - Columns stack vertically
  - Sticky headers for each column
  - Cards easy to tap
  - Hamburger menu for board settings
- **Design Problems:**
  - HMW avoid excessive scrolling?
  - HMW maintain clarity with limited space?
- **Design Opportunities:**
  - What if user can filter to show only one column at a time?

2.1 Card Quick Actions (Pu.3)
- **Page Goal:** Fast access to edit/move
- **Description:**
  - Swipe on card reveals actions

Er.3 Mobile Network Error
- **Goal:** Alert user to sync issues
- **Description:**
  - Banner or toast, retry option

##### Workflow 2B: Tablet Landscape

2.0 Kanban Board Tablet View
- **Page Goal:** Show all three columns side by side (with adjusted spacing)
- **Description:**
  - Responsive column widths
  - Touch-friendly drag-and-drop
- **Design Problems:**
  - HMW balance information density and tap targets?
- **Design Opportunities:**
  - What if columns can be resized by user?

---

### Scenario 3: User customizes Kanban board appearance (scalability/design tokens)

**Variation A:** Change color scheme
**Variation B:** Adjust column order

#### Scenario Context:
- User: Project manager
- Situation: Wants to personalize board for team needs
- Action: Accesses settings, adjusts appearance
- Actor: User
- Goal: Make board more usable for team

#### User Goal
- To tailor the Kanban board to fit workflow and preferences

#### Business Goal
- To increase adoption and satisfaction by supporting customization

##### Workflow 3A: Change Color Scheme

3.0 Board Settings
- **Page Goal:** Allow color and theme changes
- **Description:**
  - User selects from preset color palettes
  - Preview updates live
- **Design Problems:**
  - HMW ensure accessibility with custom colors?
- **Design Opportunities:**
  - What if system suggests accessible palettes?

3.1 Save/Reset Confirmation (Pu.4)
- **Page Goal:** Confirm changes
- **Description:**
  - Modal to save or revert

##### Workflow 3B: Adjust Column Order

3.0 Board Settings (same as above)

3.2 Reorder Columns
- **Page Goal:** Drag-and-drop to reorder columns
- **Description:**
  - Accessible via mouse and keyboard
- **Design Problems:**
  - HMW persist changes across devices?
- **Design Opportunities:**
  - What if user can save multiple layouts?

---

## 2. LIST OF SCREENS

- 1.0 Kanban Board Home
- 1.1 Task Card Details Pop-Up (Pu.1)
- 1.2 Drag-and-Drop Interaction
- 1.1 Card Actions Menu (Pu.2)
- 2.0 Kanban Board Mobile View
- 2.1 Card Quick Actions (Pu.3)
- 2.0 Kanban Board Tablet View
- 3.0 Board Settings
- 3.1 Save/Reset Confirmation (Pu.4)
- 3.2 Reorder Columns
- Er.1 Error: Failed to Move Task
- Er.2 Accessibility Alert
- Er.3 Mobile Network Error

---

## 3. ACCESSIBILITY & SCALABILITY PRINCIPLES

- All columns and cards use ARIA labels and roles
- Keyboard navigation with logical tab order and visible focus
- Color contrast meets WCAG 2.1 AA
- Design tokens for color, spacing, typography
- Responsive breakpoints: mobile (320-767px), tablet (768-1023px), desktop (1024px+)
- All pop-ups/modal dialogs are keyboard accessible and labeled
- Error messages announced to screen readers

---

## 4. EDGE CASES

- Large number of tasks: Virtualized list, lazy loading
- No tasks in a column: Show empty state message
- Network failures: Offline mode, retry options
- Custom colors: Automatic contrast checks
- User disables JavaScript: Graceful degradation with static board

---

## 5. SUMMARY

This documentation provides systematic, user-centered design workflows for a responsive, accessible, and scalable Kanban board. It balances user and business goals, ensures every scenario is covered, and highlights design problems and opportunities for continuous improvement.
