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

Build the route-and-workflow ledger once. For each route or shared page family, capture the primary task, role, prerequisites, entry/return paths, and empty, populated, loading, failed, stale, and read-only states where relevant. Include public entry and account/workspace selection when they are part of the requested journey. Record exceptions and reuse this map throughout the pass.

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

Read the applicable assessment sections of [NAVIGATION_AND_PAGE_USABILITY.md](NAVIGATION_AND_PAGE_USABILITY.md). Each finding names its location, observed evidence or hypothesis, impact, severity, and proposed correction. Distinguish code review from runtime and participant evidence. Do not score uninspected surfaces.

Baseline representative known-item, exploratory, and recovery tasks. Record destination-finding separately from comprehension, completion, time, and recovery. State participant experience, role, fixtures, and sample limits; small formative rounds identify issues rather than prove population-level lift.

Prioritize structural problems above cosmetic ones, preserving patterns that already work.

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

The main workflow should feel guided, not like unrelated features. Preserve non-secret drafts and return context when users leave to fix a prerequisite. Distinguish saving, approval, queuing, and execution; retain authoritative server checks and invalidate approvals when the approved payload changes. Return links must be safe in-app destinations and work without analytics.

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

Use the navigation and page-hierarchy sections of [NAVIGATION_AND_PAGE_USABILITY.md](NAVIGATION_AND_PAGE_USABILITY.md). Validate label/group changes with failing tasks or other relevant evidence. Keep menu positions stable; make customization user-controlled. Do not impose an arbitrary link count or depth limit as a universal research finding.

Review content within pages as well as routes: main question/task, current status, supporting evidence, controls, and secondary detail. Cover forms, reports, review screens, and collections, not just Home and the sidebar. Do not hide required inputs, blockers, consequences, or essential comparison information.

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
Call out substantial changes, including field correction/input retention, pending and outcome feedback, safe retry, report context, collection filters, and return-to-task behavior. Consult only the applicable page-pattern sections of [NAVIGATION_AND_PAGE_USABILITY.md](NAVIGATION_AND_PAGE_USABILITY.md).

### Simplifications and capability mapping
Identify redundant UI, steps, decisions, and destinations being consolidated or removed. Show where every affected capability remains available.

Removal of interface complexity is a feature. Loss of product capability is not.

### Evidence and verification
Distinguish verified issues from hypotheses. Name baseline tasks, affected page families/states, success criteria, and the behavior checks needed. If producing a milestone document, give work items dependencies and observable acceptance criteria; keep implementation status honest.

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

Implement in coherent slices. Reuse shared page/form/status components and cover meaningful family variants instead of duplicating patterns. Check authorization, payload approval, state retention, and deep links when simplifying presentation. Verify focused behavior after each slice before broad checks.

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

Use the verification section of [NAVIGATION_AND_PAGE_USABILITY.md](NAVIGATION_AND_PAGE_USABILITY.md). Include keyboard-only navigation, focus recovery, screen-reader announcements, responsive/zoomed layouts, and task-state variants. Verify realistic data volume, refresh/Back, validation failure, delayed requests, and safe retry. Automated accessibility checks alone do not establish usability or conformance.

Repeat baseline tasks with comparable fixtures and user experience. Report navigation, comprehension, completion, and recovery independently; disclose what was not tested. Fix newly discovered problems and rerun the affected checks.

Do not stop because the application looks better. It must be substantially easier to use.
