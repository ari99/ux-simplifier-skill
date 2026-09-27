---
name: ux-simplifier
description: Simplifies confusing digital products by improving user journeys, navigation, onboarding, forms, actions, terminology, and UX copy before visual polish. Use when workflows are unclear, users feel lost, there are too many pages or choices, or first-time users cannot identify what to do next.
---

# UX Simplifier

## Execution contract
One `/ux-simplifier` invocation is authorization to audit, plan, implement, test, and refine the full product experience.

Stay in Agent mode. Do not switch to Plan mode merely because the task is broad. Phase 7 is the plan; keep it as a compact working checkpoint and continue directly into implementation without waiting for a Build click.

If the session is already in Plan mode, switch to Agent mode before continuing. Use Plan mode only when the user explicitly requests a plan without implementation.

Honor any user pause, stop, correction, or narrowing immediately.

## Default scope
When the user does not provide a narrower scope, simplify the full product.

Do not ask how broad the pass should be or offer audit-only, core-loop-only, and full-product choices. Automatically:

1. prioritize setup → first useful result → repeat use
2. include trust-critical account, permission, billing, error, and recovery states
3. continue through the remaining routes, pages, forms, and workflows

Ask only when a decision cannot be safely inferred and would change product policy, remove a real capability, cause data loss, alter pricing, or create another irreversible consequence.

## Goal
Design the shortest clear path from the user's starting point to their desired outcome.

The user should understand:

1. what the product does
2. what they can accomplish
3. where to start
4. what to do next
5. why each page and form exists
6. what each action does
7. what happens afterward
8. how to reach the main value moment

Treat the current UI as an implementation, not the product specification.

Prefer fewer pages, decisions, concepts, navigation items, fields, and competing actions. Use progressive disclosure, sensible defaults, contextual explanation, and concrete outcome-oriented language.

Never add complexity merely to make the product appear sophisticated.

## Preserve capabilities
Simplification means making functionality easier to find, understand, and use. It does not mean reducing what the product can do.

Preserve all existing user capabilities by default, including advanced workflows, settings, permissions, integrations, billing behavior, and recovery paths.

You may remove, merge, hide, or redirect UI only when the same capability remains available clearly elsewhere or the element is genuinely redundant:

- merged pages retain every action
- advanced options remain discoverable when relevant
- reduced form fields are inferred, defaulted, automated, or deferred without eliminating necessary control
- moved routes retain appropriate redirects or compatible entry points
- duplicate controls leave one clear way to perform the action

`DELETE` means delete a redundant destination or presentation, not the underlying capability.

Never remove a real feature or change business behavior without explicit user approval. Present potential capability removal separately as an optional product decision and continue with a capability-preserving simplification.

## Token and context discipline
Minimize repeated context without skipping work:

- create one shared product map and reuse it across all phases
- search broadly first, then read focused files and sections
- do not reread unchanged files or repeat route, form, and copy inventories
- do not launch a separate subagent for every phase
- if delegation helps, partition non-overlapping scopes and request compact structured findings
- never have multiple workers inspect the same files
- do not paste skill text, raw searches, full files, or long audit prose into chat
- group repetitive pages and findings
- maintain one compact working brief containing journeys, major friction, page decisions, capability mapping, and implementation order
- implement coherent slices and run focused checks before broad verification
- report decisions and outcomes, not an exploration transcript

Spend tokens resolving uncertainty and implementing improvements, not repeatedly describing the product.

## Dependent skills
Use these skills just in time:

- Phase 2: `evaluate`
- Phase 3: `journey`
- Phase 4: `information-architecture-navigation`
- Phase 5: `onboarding-design`
- Phase 6: `ux-writing`
- Phase 9: `impeccable`

At the corresponding phase, locate and read that skill's complete `SKILL.md` once, then apply it. Do not load all dependencies up front, reread them, quote them, or produce separate reports for each.

If a dependency is unavailable, continue using the phase instructions and equivalent principles.

## Required process
Run all phases in order. Do not jump to visual redesign.

Detailed instructions are in [UX_PHASES.md](UX_PHASES.md). Do not read the whole reference up front. Search its headings and read one phase immediately before executing it.

1. **Understand the product** — build the shared map; do not edit yet.
2. **Usability audit** — apply `evaluate`; classify friction.
3. **Redesign journeys** — apply `journey`; optimize the primary outcomes.
4. **Simplify information architecture** — apply `information-architecture-navigation`; decide keep, merge, move, hide, or delete presentation.
5. **Design onboarding** — apply `onboarding-design`; optimize time to first value.
6. **Rewrite UX language** — apply `ux-writing`; make purpose, actions, and consequences explicit.
7. **Create the working plan** — compact decisions and capability mapping; do not stop unless approval is genuinely required.
8. **Implement** — make the prioritized changes while preserving functionality.
9. **Polish visually** — apply `impeccable` only after structural simplification.
10. **Fresh-user walkthrough** — reuse `evaluate`; fix remaining friction.

## Critical rules
1. Stay in Agent mode unless the user explicitly asks for plan-only work.
2. UX structure comes before visual design.
3. User goals come before existing routes.
4. Remove interface complexity before adding UI.
5. Preserve every existing product capability by default.
6. Use one obvious primary action per context.
7. Use progressive disclosure for advanced features.
8. Prefer defaults and automation to unnecessary questions.
9. Do not expose implementation concepts unnecessarily.
10. Buttons describe outcomes.
11. Forms explain their purpose.
12. Empty states tell users what to do.
13. Every workflow has an obvious completion state.
14. Every successful action makes the next step clear.
15. Do not turn onboarding into a slideshow.
16. Do not solve structural problems with tooltips.
17. Do not solve confusing navigation by adding navigation.
18. Do not preserve pages merely because they exist.
19. Do not visually polish a fundamentally confusing workflow.
20. Optimize for successful task completion, not feature visibility.
21. Read each relevant file, skill, and reference section at most once unless it changes.
22. When uncertain ask: "What is the smallest amount the user needs to understand right now?"

## Desired outcome
The product should guide the user without feeling restrictive.

A first-time user should progress toward value without documentation:

**See what matters → understand the next action → do it → see the result → know what comes next.**
