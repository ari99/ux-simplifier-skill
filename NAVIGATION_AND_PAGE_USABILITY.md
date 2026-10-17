# Navigation and page usability

Use the relevant sections during audit, information architecture, implementation, and verification. These are decision criteria, not requirements to add every pattern. Reuse working components and record where a recommendation is a hypothesis pending task validation.

## Navigation and wayfinding

- Identify the top tasks, users' vocabulary, and likely entry points before choosing a hierarchy. Give destinations distinct, predictable labels; reserve verbs for actions and use familiar nouns for objects/places where they fit better.
- Distinguish global navigation, local navigation, object tabs, and contextual next steps. Tabs represent peer views; keep information together when users need to compare it. Breadcrumbs show canonical location, not click history.
- Keep primary menu positions stable. Separate recents from the main menu and make pinning/hiding/reordering user-controlled. Fewer visible links and shallower trees are hypotheses to test, not automatic improvements; no universal seven-item or three-tier limit applies.
- Maintain a route-to-navigation map, canonical location, title, main heading, parent, and relevant cross-links. Document intentional duplicates, redirects, hidden variants, and routes reached through object detail or tabs. Protect external deep links and bookmarks when moving destinations.
- On deep entry, explain the page's purpose and location and provide a relevant parent/return path. A fresh bookmark must work without prior navigation history. Do not add multiple competing orientation bars merely to expose every ancestor.
- When volume or known-item lookup warrants search, make it visible as well as keyboard-accessible. Define its scope, indexed metadata, synonyms/old labels, result paths, ranking, and no-result recovery. Search complements understandable organization; a command palette is not a substitute for visible navigation.
- Search, recents, pins, related links, and direct routes must respect authorization. User-hidden advanced content may remain findable; permission-denied content does not. Offer a disabled feature's enable/setup link only when the user may perform that operation. Navigation filtering never replaces backend access checks.
- Keep query/filter/sort/page state restorable where useful and safe. Never put credentials or sensitive record content in URLs or telemetry. Return targets must be validated in-app destinations, scoped to the relevant workspace/account.
- Use tree tests for category/label findability; use real page tasks for comprehension and completion. Card sorting suggests grouping, not proof that the proposed navigation works. Do not require live analytics before fixing an evident accessibility or task blocker.

## Page hierarchy and disclosure

- Classify pages by the job they support: overview, setup/form, collection, report, or review/action. State the main task or question, current state, relevant prerequisites, and likely next step before technical or optional detail.
- Use meaningful headings and concise, scannable text. Prefer explicit purpose and action labels over tooltips that explain an otherwise opaque interface.
- Give actions a clear priority within their context. A read-only report may need a clear question, answer, and drill-down rather than a manufactured primary button. Do not turn every useful section into an equal-weight card.
- Disclose advanced/rare controls when useful, keeping required fields, errors, blockers, approval scope, costs, and material consequences visible at the point of decision. Hidden content must remain reachable by keyboard and supported deep links; reveal sections containing active errors.
- Do not move uncertainty or required work behind a generic “More.” Do not force cross-tab memory when the task requires side-by-side comparison.
- Check whether users understand what the page is for, what its status means, and what to do next. Use observed answers to guide layout changes rather than optimizing arbitrary card counts or above-the-fold quotas.

## Forms and correction

- Ask only for information needed now; distinguish required, optional, inferred/defaulted, and advanced values. Group related fields and show units, formats, examples, and consequences where needed. Defaults retain necessary user control.
- Preserve visible labels, programmatic names, help associations, and logical field groups. Placeholders are not labels. Do not add a wizard automatically: frequent operators may benefit from one grouped form, while an unfamiliar dependent sequence may warrant stages.
- Validate when a user can act on the result; do not flag unfinished intermediate typing as an error. Keep server validation authoritative and align client checks with it.
- On invalid submit, identify the fields and correction, preserve entered non-secret values, and provide a field-linked summary for multiple errors. Move focus deliberately; associate errors with fields and reveal invalid fields inside collapsed sections.
- Separate validation, missing permission/prerequisites, and service failure: each needs a different recovery path. Avoid replacing a specific error with a generic “try again” message in a shared form wrapper.
- Explain whether values are unsaved, saved as a draft, or submitted. Retain safe work across recoverable failures and supported Back/return flows. Do not persist secrets in browser storage or URLs; explain when a credential must be re-entered.

## Action feedback and recovery

- Define the meaningful states of each important action: idle, submitting, queued/running where applicable, success, recoverable error, and blocked. A request accepted for background work is not completed work.
- Show pending feedback near the action and prevent duplicate pending submissions. Announce meaningful status changes without unnecessary focus shifts. Do not fabricate progress percentages, completion, or success.
- Differentiate loading, never configured, no records yet, filtered-out results, stale/partial data, and failure. Empty states explain the actual cause and offer a relevant role-aware next step. Preserve usable previous data during refresh with a clear stale indicator when appropriate.
- Recovery identifies what happened and what can be done. For a request with an uncertain outcome, check authoritative server state before offering a retry that could send, spend, publish, or duplicate records. Preserve existing idempotency protections.
- State what success changed and offer a useful continuation. Do not rely exclusively on a transient toast for a consequential outcome. Undo is appropriate only when the operation is actually reversible.

## Reports and AI-supported decisions

- Organize reports around the user's question and decision. Make the relevant period, comparison, units, data mode, and freshness clear; keep that context consistent through supported drill-down and return paths.
- Missing is not zero. Explain unavailable comparisons, partial coverage, small denominators, and stale inputs where they affect interpretation. Use accessible text/table alternatives for chart values needed to complete the task.
- Distinguish measured evidence, estimated values, and generated interpretation. Keep source/provenance inspectable and claims traceable to the relevant data. Regenerating narrative must not imply that underlying metrics were refreshed.
- Make AI recommendations inspectable, correctable, and dismissible where appropriate. Explain material limitations when relevant to the decision; do not hide them in generic disclaimers or imply certainty unsupported by evidence.
- Preserve strong existing patterns. Improve the decision and evidence path rather than replacing working summaries with a rigid metric/card quota.

## Collections, tables, and filters

- Use a table when cross-row comparison matters, cards when discrete tasks need context, and neither solely for appearance. Test realistic record counts, long values, missing values, and meaningful variations.
- Add filters and sorts for demonstrated lookup/comparison needs. Expose current scope, result count, active filters, and a reset. Explain filtered-out results differently from an unpopulated collection.
- Restore supported non-sensitive filter/sort/pagination and selection context after detail views, refresh, and Back. Do not reuse another workspace's view state or expose unauthorized records.
- Provide semantic headers, announced sort state, meaningful row-action names, and predictable focus. Keep essential values and actions available at narrow widths; two-dimensional tables may need contained scrolling rather than losing comparison data.
- Bound rendering with pagination or another appropriate strategy when volume warrants it. Avoid adding virtualization or complex facets for a small list without a demonstrated benefit.
- When bulk actions already exist or are justified by the task, state whether selection applies to visible rows, the current page, or all matches. Keep permissions and consequence review intact; do not introduce bulk mutations as cosmetic cleanup.

## Workflow continuity and review

- Carry users from a blocked task to its exact prerequisite and back, preserving safe drafts and context. Use existing authoritative workflow state instead of a second checklist that can disagree with it.
- Review screens summarize the actual payload and consequences and allow targeted correction. For example, campaign review may need audience, sender, copy, schedule/time zone, caps, and cost. Keep required review evidence accessible.
- Clearly distinguish save, approve, queue, launch/send, and confirmed completion. Approval alone must not appear to execute an operation when a separate step is required.
- Revalidate prerequisites and roles on the server. Editing an approved payload preserves the product's invalidation and reapproval rules. Presentation simplification must not bypass exact-payload checks, spending limits, consent, or execution gates.
- Test the complete round trip, including a fresh deep link, missing prerequisite, correction failure, successful correction, return, and completion. Offer a canonical fallback when origin context is unavailable.

## Verification and evidence

- Record one shared inventory and baseline. For representative tasks, specify role, starting route, fixtures, success condition, and meaningful states. Include known-item lookup, exploration, and mistake/no-result recovery.
- Evaluate finding the destination separately from understanding content, completing the action, recognizing its result, and recovering from failure. Fewer clicks, shorter copy, search use, and time on page alone are not success measures.
- Record unassisted completion, errors/correction, time, and a consistently worded ease question when participants are available. Small moderated rounds are formative. Report samples by task and role; do not transfer card-sort sample rules to tree tests or page usability studies.
- Label code-review hypotheses, browser observations, participant findings, and analytics separately. Score only evaluated surfaces. Define baseline-relative targets before comparing results; do not claim causal lift from different users or different weeks without an appropriate design.
- Check the relevant page families with empty, populated, loading, failed, stale, and read-only states. Inspect delayed responses, double clicks, invalid submissions, safe retry, refresh/Back, and stale approval where applicable.
- Test keyboard operation, visible/unobscured focus, heading/landmark structure, labels/errors, status announcements, contrast, and target sizes. Use expected disclosure/dialog/tab behavior; ordinary navigation links do not require application-menu arrow-key behavior.
- Target the project's accessibility standard, normally WCAG 2.2 AA for web. Include 200% text resizing and 320 CSS-pixel reflow or equivalent 400% zoom; assess applicable two-dimensional-content exceptions individually. Record the browser/screen-reader combination and manual checks; automated scans alone cannot establish conformance.
- Use behavior tests for important state transitions and protections, with representative checks for meaningful shared-component variants. Run repository-required checks and inspect changed layouts. Report coverage, exclusions, unresolved severity/owners, and actual outcomes without claiming untested work is complete.

## Research grounding

Use these as starting points when research is useful, not mandatory reading for every task. Verify the relevant source before quoting a result; distinguish a standard, maintained design pattern, primary study, and practitioner interpretation. Do not promise an improvement percentage or universal numerical UI limit from these references.

- [NN/g: How Users Read on the Web](https://www.nngroup.com/articles/how-users-read-on-the-web/) — original research on scannable content; old web-writing evidence, not a modern SaaS lift forecast.
- [NN/g: Progressive Disclosure](https://www.nngroup.com/articles/progressive-disclosure/) — practitioner guidance on secondary complexity; what to hide depends on the task.
- [GOV.UK: Recover from validation errors](https://design-system.service.gov.uk/patterns/validation/) — retained input and field-linked correction. GOV.UK-specific implementation choices need not be copied wholesale.
- [GOV.UK: Check answers](https://design-system.service.gov.uk/patterns/check-answers/) — review and targeted changes before committing; adapt it to repeat operator workflows.
- [GOV.UK: Table](https://design-system.service.gov.uk/components/table/) — comparison-oriented tabular presentation.
- [Bach et al.: Dashboard Design Patterns](https://arxiv.org/abs/2205.00757) — taxonomy and design workshop evidence, not proof that one layout wins universally.
- [Microsoft Research: Guidelines for Human-AI Interaction](https://www.microsoft.com/en-us/research/project/guidelines-for-human-ai-interaction/) — research-based guidance for initial use, ongoing interaction, and failures.
- [W3C: WCAG 2.2](https://www.w3.org/TR/WCAG22/), [Status Messages](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html), and [Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) — accessibility requirements and explanatory guidance, not usability lift claims.
