# UX Simplifier Phase Reference

Read one phase immediately before executing it. Do not load this entire file up front.

## Phase 1 — Understand the product
Inspect the actual project before suggesting major changes.

Study:

- routes, pages, layouts, and navigation
- dashboard and primary components
- forms, empty states, and onboarding
- authentication and settings
- important API-backed actions
- existing product copy

Infer the major jobs users are trying to accomplish and identify the 3–5 most important outcomes.

For each outcome identify:

- user starting point and desired result
- existing path and number of steps
- decisions and prerequisites
- confusing terminology and unnecessary detours
- dead ends, missing feedback, and unclear next actions

Do not modify code yet.

## Phase 2 — Usability audit
Locate and read the complete `evaluate` skill once, then apply its workflow and principles.

Evaluate as a brand-new user with no codebase or internal terminology knowledge.

For every major workflow ask:

- Where would I naturally start?
- Is the primary action obvious?
- Do I understand the page and form purpose?
- Do I know what information is expected and why?
- Do I know what happens after submission?
- Are primary actions competing?
- Is internal knowledge required?
- Can I see completed and remaining work?
- Do I know where to go next?
- Can I recover from mistakes?
- Are empty states instructive?

Classify friction as:

- REMOVE
- MERGE
- SIMPLIFY
- RENAME
- REORDER
- AUTOMATE
- DEFAULT
- HIDE UNTIL NEEDED
- EXPLAIN
- KEEP

Prioritize structural problems above cosmetic ones.

## Phase 3 — Redesign user journeys
Locate and read the complete `journey` skill once, then apply its workflow and principles.

For each primary goal, redesign the journey from starting point to successful outcome. Ignore existing page boundaries when necessary.

At every step the user should understand:

1. Where am I?
2. What am I doing here?
3. Why does this matter?
4. What should I do now?
5. What happens afterward?

Reduce unnecessary steps. Combine steps when it improves comprehension. Split screens that create excessive cognitive load.

Automate choices that do not require user judgment. Prefer sensible defaults. Do not expose configuration before it is needed.

The main workflow should feel guided, not like unrelated features.

## Phase 4 — Simplify information architecture
Locate and read the complete `information-architecture-navigation` skill once, then apply its workflow and principles.

Inventory significant pages, routes, navigation items, sidebar items, tabs, settings sections, dashboards, and major modals.

For each decide:

- KEEP
- MERGE
- MOVE
- HIDE
- DELETE

`DELETE` applies only to a redundant destination or presentation. Preserve the underlying capability in a clearer destination.

Pages should represent meaningful user destinations, not implementation resources or database concepts.

Reduce top-level navigation reasonably. Group features around user intent. Use labels users understand rather than internal nouns.

The dashboard or home screen should answer:

**What should I do next?**

Do not create a wall of equal-weight cards.

## Phase 5 — Design onboarding and guidance
Locate and read the complete `onboarding-design` skill once, then apply its workflow and principles.

Design first run from account creation to the first meaningful result.

Do not create a long feature tour. Prefer learning by doing through:

- setup checklists
- a guided initial workflow
- contextual hints and useful empty states
- progress indicators
- recommended defaults
- examples, templates, or demonstrations
- clear completion states

Every important screen should make the likely next action obvious and show, when relevant:

- what is complete
- what happens next
- why it matters

Never teach future features before they are needed. Optimize time to value.

## Phase 6 — Rewrite UX language
Locate and read the complete `ux-writing` skill once, then apply its workflow and principles.

Review:

- titles, subtitles, navigation labels, and headings
- descriptions, labels, placeholders, and helper text
- validation messages, buttons, links, and tooltips
- empty states, confirmations, success messages, warnings, and errors

Prefer language describing the user's outcome.

Avoid vague labels such as `Submit`, `Continue`, `Next`, `Proceed`, `Execute`, `Process`, `Manage`, or `Configure` when a specific outcome is possible.

Examples:

- `Submit` → `Create campaign`
- `Continue` → `Connect Stripe`
- `Save` → `Save billing rules`
- `Create` → `Create first report`

Explain why information is requested when it is not obvious. Do not use placeholders as labels.

## Phase 7 — Create the working plan
Before broad changes, create a compact working summary. Do not stop for approval unless it contains an irreversible decision requiring the user.

Include:

### Primary journeys
The 3–5 most important outcomes.

### Navigation
Show `CURRENT → PROPOSED`.

### Page decisions
For meaningful pages show `PAGE → KEEP / MERGE / MOVE / HIDE / DELETE` with a short reason.

Group repetitive pages instead of repeating identical reasoning.

### Biggest confusion
Rank only the highest-impact structural problems.

### Onboarding
Summarize the first-run journey.

### Forms and actions
Call out substantial changes.

### Simplifications and capability mapping
Identify redundant UI, steps, decisions, and destinations being consolidated or removed. Show where every affected capability remains available.

Removal of interface complexity is a feature. Loss of product capability is not.

Continue directly into implementation.

## Phase 8 — Implement
Work systematically through the prioritized plan while preserving all product capabilities.

Where appropriate:

- merge pages and redirect redundant routes
- simplify navigation
- establish clear primary actions and hierarchy
- infer, default, automate, or defer form fields without removing necessary control
- move advanced options behind discoverable progressive disclosure
- improve empty, loading, progress, success, and error states
- introduce setup or checklist flows
- eliminate unnecessary decisions

Do not make unrelated architectural rewrites solely for UX cleanup. Keep implementation maintainable.

Implement in coherent slices. Verify focused behavior after each slice before broad checks.

## Phase 9 — Visual design and polish
Only after structure, workflows, information architecture, onboarding, and wording are simplified, locate and read the complete `impeccable` skill once and apply it.

Improve:

- visual hierarchy
- spacing and typography
- grouping, contrast, and alignment
- affordances and interaction states
- responsive behavior
- accessibility and consistency

Do not reintroduce unnecessary cards, sections, navigation, controls, decorative complexity, information overload, or ambiguous actions.

One primary action should look primary. Secondary and rare actions should not compete.

## Phase 10 — Fresh-user walkthrough
Reuse the `evaluate` principles loaded in Phase 2. Do not read the skill again unless its source changed.

Walk through each major journey as a first-time user.

At every screen verify:

- Is the purpose immediately understandable?
- Is there an obvious next step and one primary action?
- Is progress visible?
- Are labels understandable without internal knowledge?
- Does every requested input have a reason?
- Is anything unrelated to the task present?
- Can another step, page, field, or decision be removed without losing capability?
- Is feedback clear after every important action?

Fix newly discovered problems and rerun focused checks.

Do not stop because the application looks better. It must be substantially easier to use.
