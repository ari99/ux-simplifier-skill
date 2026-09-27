# UX Simplifier

`ux-simplifier` is a global Agent Skill by `ari99` for turning confusing digital products into clear, goal-oriented experiences.

It focuses first on product structure and task completion:

- user journeys
- information architecture and navigation
- onboarding and next-step guidance
- forms, actions, and feedback
- terminology and UX copy
- progressive disclosure
- cognitive-load reduction

Visual polish comes only after the product experience is understandable.

## What it does

The skill inspects an existing application, identifies its most important user outcomes, audits each major workflow as a first-time user, and classifies friction as:

- remove
- merge
- simplify
- rename
- reorder
- automate
- default
- hide until needed
- explain
- keep

It then redesigns the primary journeys, simplifies navigation and page structure, improves onboarding and UX language, presents a concrete simplification plan, implements the approved direction, and performs a final fresh-user walkthrough.

The intended experience is:

**See what matters → understand the next action → do it → see the result → know what comes next.**

## When to use it in the SDLC

### Product discovery and definition

Use it while defining the product's primary users, jobs, outcomes, and activation moment. It can prevent internal implementation concepts from becoming the application's information architecture.

Best for:

- framing the 3–5 primary user outcomes
- challenging unnecessary features, pages, and decisions
- designing the shortest path to first value
- establishing user-centered terminology

### UX architecture and prototyping

This is the highest-leverage time to use the skill. Apply it before high-fidelity visual design or substantial implementation.

Best for:

- mapping task flows
- deciding which pages should exist
- simplifying navigation
- designing onboarding
- reducing form fields and choices
- validating that every screen has a clear purpose and next action

### Before implementation

Use it as a structural design review before engineering commits to routes, schemas, and component boundaries.

Its simplification plan provides:

- primary journey definitions
- current-to-proposed navigation
- keep/merge/move/hide/delete decisions for pages
- onboarding recommendations
- forms and actions requiring changes
- an explicit removal list

### During implementation

Use it to implement the prioritized UX plan systematically without broad, unrelated architectural rewrites.

It helps engineers:

- preserve important capabilities while simplifying access
- introduce clear primary actions
- improve empty, loading, success, and error states
- move advanced controls behind progressive disclosure
- make defaults and automation replace unnecessary decisions

### Design and code review

Use it to catch structural UX regressions before release. Review completed work from the perspective of someone with no product or domain knowledge.

Verify:

- every page has a user-centered reason to exist
- every important context has one obvious primary action
- labels describe outcomes
- forms explain why information is needed
- users can see completion and the next step

### Pre-release and usability testing

Use its final fresh-user walkthrough alongside real usability testing. The skill can identify likely friction, but it does not replace evidence from actual users.

Apply it before launch to check:

- first-run activation
- empty states
- mistake recovery
- permissions and blocked states
- action feedback
- journey completion

### Post-launch optimization

Use it when analytics, support tickets, session recordings, interviews, or usability tests show that users are lost, abandoning flows, or failing to reach value.

Bring evidence such as:

- funnel drop-off
- time-to-value
- failed or repeated actions
- support themes
- search behavior
- usability observations

The skill should simplify the experience in response to evidence, not merely rearrange the interface.

## When not to use it

This skill is not primarily for:

- visual restyling with no workflow problem
- isolated branding work
- backend-only refactoring
- replacing user research
- maximizing feature visibility
- adding more UI to compensate for unclear structure

For purely visual interface work, use `impeccable` directly.

## Dependent skills

`ux-simplifier` explicitly reads and applies these skills during the relevant phase:

- `evaluate`
- `journey`
- `information-architecture-navigation`
- `onboarding-design`
- `ux-writing`
- `impeccable`

If a dependency is unavailable, the workflow continues using the same principles.

Example global dependency installations:

```bash
npx skills add https://github.com/ghaida/intent --skill evaluate -g -y
npx skills add https://github.com/ghaida/intent --skill journey -g -y
npx skills add https://github.com/hueyexe/frontend-agent-skills --skill information-architecture-navigation -g -y
npx skills add https://github.com/owl-listener/designer-skills --skill onboarding-design -g -y
npx skills add https://github.com/content-designer/ux-writing-skill --skill ux-writing -g -y
```

Install `impeccable` from its current published source if it is not already available.

## Install

Install globally:

```bash
npx skills add https://github.com/ari99/ux-simplifier-skill --skill ux-simplifier -g -y
```

Verify:

```bash
npx skills list -g
```

## License

MIT. See [LICENSE](LICENSE).
