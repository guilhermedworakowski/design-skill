# References: Nielsen's Heuristics

> **Instruction for agents:** Consult this file whenever the request involves evaluating interfaces, identifying usability problems, reviewing flows or building screens. The heuristics are this skill's UX quality criteria — every interface decision must be justified by at least one of them.

---

## What Nielsen's Heuristics are

Jakob Nielsen's 10 Usability Heuristics are general principles of interface design, established in 1994 and widely adopted as an industry standard. They aren't rigid rules, but guidelines for identifying usability problems and guiding design decisions.

**When to apply them:**
- Heuristic evaluation of existing interfaces
- Reviewing prototypes before user testing
- Justifying design decisions to stakeholders
- Identifying problems without the need for user research

---

## The 10 Heuristics

---

### H1 — Visibility of system status

**Principle**
The system should always keep users informed about what is going on, through appropriate feedback within a reasonable time.

**Rule**
The user should never wonder: *"Did the system receive my action? What is happening now?"*

**How to apply it**
- Show loading states (spinners, skeletons, progress bars)
- Confirm completed actions (success messages, visual state changes)
- Indicate steps in long processes (e.g. "Step 2 of 4")
- Use colors and icons to communicate states (active, inactive, error, success)

**Common problems when violated**
- Buttons that give no feedback when clicked
- Forms that don't confirm submission
- File uploads without a progress indicator
- Navigation with no indication of the current page

---

### H2 — Match between the system and the real world

**Principle**
The system should speak the user's language — words, phrases and concepts familiar to the user, not technical jargon. Follow real-world conventions, making information appear in a natural and logical order.

**Rule**
The user should never need to learn a new language to use the product.

**How to apply it**
- Use terminology from the user's domain, not from the technology
- Use real-world metaphors when appropriate (trash can, folder, cart)
- Organize information in the order the user processes it mentally
- Avoid abbreviations, acronyms or technical terms without explanation

**Common problems when violated**
- Technical error messages ("Error 404", "Null pointer exception")
- Labels that make sense to the developer but not to the user
- Flows organized by the system's logic, not the user's

---

### H3 — User control and freedom

**Principle**
Users often choose functions by mistake and need a clearly marked "emergency exit" to leave the unwanted state without going through an extended process.

**Rule**
The user should always be able to undo, cancel or go back easily.

**How to apply it**
- Offer undo and redo options
- Confirm destructive actions (deletion, cancellation) before executing them
- Allow in-progress processes to be cancelled
- Make sure the "back" button works predictably

**Common problems when violated**
- Deletion without confirmation and with no way to recover
- Flows without a cancel button
- Modals that trap the user without a clear way out
- Long forms that lose data when the user tries to leave

---

### H4 — Consistency and standards

**Principle**
Users should not have to wonder whether different words, situations or actions mean the same thing. Follow platform conventions.

**Rule**
The same element should behave the same way throughout the system.

**How to apply it**
- Use the same component for the same function on every screen
- Keep terminology consistent (don't mix "save" and "confirm" for the same action)
- Follow platform conventions (iOS, Android, Web)
- Document patterns in the design system and follow them rigorously

**Common problems when violated**
- Primary buttons with different colors on different screens
- Actions with different names doing the same thing
- Components that behave unexpectedly in different contexts

---

### H5 — Error prevention

**Principle**
Even better than good error messages is a careful design that prevents problems from occurring in the first place.

**Rule**
The system should be designed to make errors difficult or impossible to happen.

**How to apply it**
- Disable actions that are impossible or inappropriate in the current context
- Use real-time validation in forms (not only on submit)
- Confirm irreversible actions before executing them
- Limit input options when possible (selects, toggles, date pickers)
- Use smart defaults that reduce the chance of error

**Common problems when violated**
- Forms that only validate on submit
- Free-format date fields without an input mask
- Destructive actions that are easily accessible and have no confirmation

---

### H6 — Recognition rather than recall

**Principle**
Minimize the user's memory load by making objects, actions and options visible. The user shouldn't have to remember information from one part of the interaction to use it in another.

**Rule**
The user should never need to memorize information to complete a task.

**How to apply it**
- Show available options instead of requiring the user to remember them
- Keep context visible during long tasks (e.g. order summary during checkout)
- Use history, suggestions and autocomplete
- Show examples of the expected format in input fields

**Common problems when violated**
- Fields without a placeholder or format example
- Multi-step processes without a summary of what was filled in
- Menus with no indication of where the user is

---

### H7 — Flexibility and efficiency of use

**Principle**
Accelerators — unseen by novice users — can speed up interaction for expert users. Allow users to tailor frequent actions.

**Rule**
The system should serve both beginner and advanced users well.

**How to apply it**
- Offer keyboard shortcuts for frequent actions
- Allow advanced users to customize flows
- Create shortcuts for repetitive tasks
- Don't force experienced users through guided flows unnecessarily

**Common problems when violated**
- Systems that force step-by-step wizards on experienced users
- Lack of shortcuts in heavily used tools
- Inability to skip steps the user already knows

---

### H8 — Aesthetic and minimalist design

**Principle**
Dialogues should not contain information that is irrelevant or rarely needed. Every extra unit of information competes with the relevant units and diminishes their relative visibility.

**Rule**
Every element on the screen must have a purpose. If it doesn't, remove it.

**How to apply it**
- Remove information, fields and elements that don't contribute to the current task
- Prioritize a clear visual hierarchy: what matters most should be most visible
- Avoid decoration without function
- Use white space intentionally to give content room to breathe

**Common problems when violated**
- Dashboards with dozens of metrics and no hierarchy
- Forms with unnecessary optional fields
- Cluttered screens that make it hard to identify the main action

---

### H9 — Help users recognize, diagnose and recover from errors

**Principle**
Error messages should be expressed in plain language (no codes), precisely indicate the problem and constructively suggest a solution.

**Rule**
When an error occurs, the user must understand what happened and know what to do.

**How to apply it**
- Write error messages in human language, not technical language
- Be specific: "Invalid email" is better than "Field error"
- Always offer a next step ("Try again", "Contact us")
- Use color and icon to visually reinforce the error state
- Place the message close to the element with the problem

**Common problems when violated**
- "An unexpected error occurred. Code: 500"
- Generic messages that don't indicate which field has the problem
- Errors with no guidance on how to fix them

---

### H10 — Help and documentation

**Principle**
Even though it is better if the system can be used without documentation, it may be necessary to provide help. Such information should be easy to find, focused on the user's task, list concrete steps and not be too long.

**Rule**
When the user needs help, it should be within reach, contextual and actionable.

**How to apply it**
- Offer contextual tooltips and hints at moments of doubt
- Create a searchable help center
- Use progressive onboarding instead of long upfront tutorials
- Document real use cases, not isolated features

**Common problems when violated**
- Generic help that doesn't solve the user's specific problem
- Outdated or hard-to-find documentation
- Lack of context: help only available outside the flow where the problem occurs

---

## How to run a Heuristic Evaluation

**Recommended process**

1. **Define the scope** — which screens or flows will be evaluated?
2. **Run the evaluation** — go through the flow as a user, identifying violations
3. **Document each problem** with:
   - Heuristic violated (H1 to H10)
   - Description of the problem
   - Severity (1 = cosmetic, 2 = minor, 3 = major, 4 = catastrophic)
   - Suggested fix
4. **Prioritize by severity** for the fix plan

**Severity scale (Nielsen)**

| Level | Description |
|---|---|
| **0** | Not a usability problem |
| **1** | Cosmetic — fix only if extra time is available |
| **2** | Minor — low fix priority |
| **3** | Major — important to fix, affects the experience |
| **4** | Catastrophic — must be fixed before launch |
