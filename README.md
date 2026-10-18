# Procurement Intelligence Lab

Public progress showcase for a procurement product being built from practical procurement questions, with AI-assisted engineering.

## Chunk 05 - What happens when a feature is paused?

Version 0.10.0 adds feature controls, an enhancement roadmap, release records and separate AI readiness evidence to the local synthetic workspace.

| Choice | Effect on authorized work |
| --- | --- |
| Enabled | Work can proceed under the current business rules. |
| Read only | Existing records remain readable; optional feature changes and reminder dispatch stop. |
| Disabled for new activity | New feature work stops; permitted existing work may continue. Already reserved reminders may dispatch unless a dependency is read only. |

![Actual feature administration page showing a fictional entity's sourcing module set to read only, impact preview controls and retained configuration history.](assets/chunk-05-feature-controls.png)

*Actual screenshot of local build 0.10.0, captured 18 October 2026 in Asia/Dubai using disposable fictional records. The saved setting and history were created through the real forms. No message or procurement transaction was sent.*

The owner can set global defaults. A separately authorized feature administrator can manage settings for their own entity; this role grants no access to procurement records or documents. Changes require an impact preview, a current revision and a reason. Access checks, audit history, intake and mandatory approval controls cannot be disabled. Planned modules cannot be activated before implementation.

Putting reminders or their scheduling dependency into read-only mode holds reserved reminders. Turning the feature back on does not replay those held attempts. Existing deadlines and history remain intact; further contact needs an explicit new schedule action.

The roadmap records each enhancement's problem, scope, dependencies, acceptance criteria and evidence. Material scope changes invalidate earlier verification and value claims without deleting history. Release records require a version, exact commit and verification evidence. These are maintained local records; they are not automatically certified by the interface.

AI readiness keeps five claims separate: implementation, offline tests, live-provider tests, model quality and measured business value. Missing credits can block live checks while development and offline testing continue. This increment adds governance and feature enforcement; quotation extraction remains planned, and no successful live AI generation is claimed.

Fewer disruptive configuration changes and clearer delivery decisions are value hypotheses to measure, not demonstrated customer outcomes.

## Chunk 04 - Are these quotations really comparable?

A low headline price is useful only when the scope and costs are clear. Version 0.9.0 turns a currently approved request into a versioned RFQ and compares manually recorded fictional quotations against its saved requirements.

| Fictional offer | What the comparison shows |
| --- | --- |
| AED 1,000 | Both requested lots, shipping and tax are recorded; the declared total matches the calculation. |
| AED 600 in recorded line prices | Installation is missing and shipping is unknown. A complete total remains unknown. |
| AED 900 declared | The recorded components add up to AED 1,000. The difference needs clarification. |

![Actual quotation comparison showing a complete AED 1,000 offer, a partial offer with missing installation and unknown shipping, and an AED 900 declared total against AED 1,000 of recorded components.](assets/chunk-04-quotation-comparison.png)

*Actual screenshot of local build 0.9.0, captured 17 October 2026 in Asia/Dubai using disposable fictional identities and quotations. No supplier invitation, award or purchase order is sent.*

The comparison keeps unknown amounts separate from explicit zero. Missing lots, quoted currency or unit differences, and arithmetic discrepancies are visible. It does not rank suppliers or choose a winner.

Each quotation belongs to an RFQ version. Changes to the request, route or approval authority make the old comparison require fresh review. A new RFQ version preserves earlier quotations as history; their prices are not carried into the new comparison.

Buyers can record and revise offers in their authorized entity. Approvers and viewers can review them; requester-only accounts cannot access sourcing records. The entity pause control blocks sourcing changes while keeping existing comparisons readable.

This increment uses one whole lot per requested line and records shipping and tax as explicit additions. It does not infer quantities, convert currencies, calculate tax rates, score technical quality or automate an award. The comparison is deterministic; quotation AI analysis is a future candidate.

Less manual checking and fewer incomplete comparisons are value hypotheses to measure, not demonstrated customer savings.

## Chunk 03 - Who is allowed to approve this request?

An approval needs an identifiable person, the right entity and current permission for the exact request. Version 0.8.0 adds named local accounts with requester, buyer, approver and viewer roles.

| Practical check | Demonstrated behavior |
| --- | --- |
| Can the requester approve their own request? | The original creator cannot approve it, even if they also hold the approver role. |
| Can another entity see the request? | Record views, history, exports and document downloads check the selected entity and current permissions. |
| What if the approver's permissions change? | The earlier decision remains in history but loses current authority. Restoring permissions does not revive it; a buyer must reopen review for a fresh decision. |
| Does record access grant every document? | Documents require parent-record visibility and an explicitly allowed role. |

![Actual synthetic work queue showing Fictional North Entity, the current Approver role, a request created by requester, and its simulated approval by a different named user.](assets/chunk-03-current-approval-authority.png)

*Actual screenshot of local build 0.8.0, captured 14 October 2026 using disposable fictional identities and records. Approvals are simulations. The sample amount is not a delegation threshold.*

The scope is deliberately precise: the approver must differ from the original creator. A person holding both buyer and approver roles may edit, route and approve another creator's request. Separate editor/router approval duties and monetary delegation rules are future work.

Clearer responsibility and less unauthorized rework are value hypotheses to measure; this demonstration does not claim customer outcomes.

## Chunk 02 · Remind while there is time to act

A useful first reminder helps prevent a missed deadline. Version 0.7.1 corrects the earlier overdue-only example and clearly separates preventive reminders from overdue follow-ups.

| Sample task event | Asia/Dubai time |
| --- | --- |
| Task ready | Friday 11 September 2026, 15:00 |
| First preventive reminder | **Friday, 16:00** |
| Task deadline | **Friday, 17:00** |
| Separate overdue follow-up, only if incomplete | Monday 14 September, 10:00 |

Fictional rules: Monday–Friday 09:00–17:00, quiet hours 16:30–10:00, two working hours to complete, one working hour of preventive notice, and an optional overdue follow-up one working hour after due. The first reminder is Friday; Monday is a separate overdue follow-up.

![Actual synthetic schedule preview showing a Friday 16:00 preventive reminder before a Friday 17:00 deadline, followed by a separate optional overdue follow-up.](assets/chunk-02-task-deadline-and-reminder.png)

*Actual screen from local build 0.7.1, captured with disposable synthetic data. Actions create local simulation receipts; no message is sent.*

The product looks for an allowed contact before due, moving a planned contact earlier when quiet hours require it. If the target time passed but useful notice is still possible, it labels the reminder delayed. If no safe contact remains before due, it flags the missed preventive window. A preventive reminder cannot execute at or after the deadline or quietly become an overdue reminder.

Task completion, changed recipients and stale rules cancel pending attempts. Both reminder phases retain duplicate protection, cooldown and stable lifetime limits. Old policies require explicit review and reapplication; task deadlines and historical receipts remain preserved.

Reduced chasing and fewer missed deadlines remain user-value hypotheses to measure. The demonstration establishes the implemented rule and its local checks, not customer outcomes.

## Chunk 01 · Traceable demand, explainable SLA measurement and a bounded AI assistant

The first question is simple: can a reviewer follow a business need through its plan, requisition, changes and next responsible action—and understand the numbers shown along the way?

The current local build demonstrates:

| Procurement question | Implemented demonstration |
| --- | --- |
| Where did this request come from? | Versioned plans and demand lines, linked to planned requisitions; ad-hoc requests record a reason. |
| Can one request combine needs, or one need be split? | Value allocations support combined and split demand, with remaining-capacity checks. |
| What needs review when the source changes? | Affected intake loses its prior valid review state; unaffected intake retains its state. Revision history remains inspectable. |
| What should happen next? | A fictional routing policy, explicit simulated approval and dependent tasks make the next action visible. |
| Is the SLA number defensible? | Working calendars, pauses, reporting snapshots, exclusions and the completed-stage denominator are explicit. |

![Actual SLA control room showing synthetic data, a 66.7% sample completion rate with its denominator, and an example comparing 67 elapsed hours with 3 working hours.](assets/chunk-01-sla-control-room.png)

*Actual screenshot of local build 0.6.0, captured on 8 September 2026 from disposable synthetic data. This is a viewport capture of the running application.*

The worked example runs from Friday at 16:00 to Monday at 11:00. Under the displayed Monday–Friday, 09:00–17:00 demonstration calendar, that is **67 elapsed hours and 3 working hours**. The sample completion rate is **2 of 3 eligible completed stages (66.7%)**. Neither figure is a customer result or an end-to-end procurement performance claim.

## Current limits

This is a local development product supporting named accounts and entity-scoped permissions in one application process, alongside a preserved legacy owner exercise. Approvals and reminders are simulations. It does not place orders, reserve budget, contact suppliers, connect to an ERP or establish enterprise identity and monetary delegation. Plan values, requisition values and allocations describe different views of demand and must not be added together as spend.

## AI-01 · Explain a synthetic SLA snapshot

The first AI capability is implemented as an owner-triggered explanation flow. It presents the authoritative SLA facts for review, asks for explicit agreement before sending those facts to OpenAI, and is designed to display advisory observations linked to evidence alongside what remains unknown.

![Actual AI snapshot explainer preview showing authoritative synthetic SLA facts and an explicit disclosure checkbox before requesting an explanation.](assets/chunk-01-ai-preview.png)

*Actual 0.6.0 preview screen. This image shows the review step; no generated answer has been inserted or fabricated.*

This first capability accepts only the unchanged bundled synthetic SLA facts. It cannot change calculations or take procurement actions. A citation points to an input fact; it does not prove that an AI-generated interpretation is correct. The person reviewing the explanation remains responsible for checking it.

**The request path and preview are implemented; live-provider validation and explanation-quality evaluation are still pending.** The screenshots do not demonstrate a successful live AI response. Later candidates include clarifying incomplete requests and identifying missing information, subject to evidence and testing.

## What has been checked

**The 0.10.0 release passed 844 automated tests**, with no failures, errors or skips. Five sandboxed browser flows cover administration and existing procurement workflows at desktop/mobile widths. A fresh runtime-only installation passed 34 checks and all 54 packaged product files matched source; nine Windows launcher checks passed. These checks include feature boundaries, preserved history, scope-change invalidation and independent AI readiness records. No live AI request or real procurement message was sent.

**The historical 0.9.0 release passed 707 automated tests**, with no failures, errors or skips. Four sandboxed browser flows checked the new sourcing comparison and the existing demand, approval, document-access and preventive-reminder workflows at desktop and mobile widths. The sourcing exercise recorded three fictional offers through the actual forms and verified role boundaries and source-change invalidation. A fresh runtime-only installation passed 28 checks and all 42 packaged product files matched source; nine Windows launcher checks passed. No live AI call, supplier invitation or real procurement message was sent.

**The historical 0.8.0 release passed 639 automated tests**, with no failures, errors or skips. Actual sandboxed desktop/mobile browser checks covered named roles, entity and document boundaries, self-approval denial and approval by someone other than the original request creator. Existing SLA, demand and preventive-reminder flows passed. A fresh runtime-only installation passed 25 checks and all 36 packaged files matched source; nine Windows launcher checks passed. No live AI call or real message was sent.

The historical corrected 0.7.1 release passed 517 automated tests, with no failures, errors or skips. Real sandboxed desktop/mobile browser checks demonstrated preventive contact before due and a separately identified overdue follow-up. A fresh runtime-only installation and nine Windows launcher checks passed. No live AI call or real message was sent.

The historical 0.7.0 release passed **448 automated tests**, with zero failures, errors or skips. Sandboxed desktop/mobile browser checks exercised both existing workflows and the new schedule controls, including early-dispatch rejection and duplicate prevention. A fresh runtime-only installation and nine Windows launcher checks also passed. Those 0.7.0 checks used disposable synthetic state and made no live AI calls; they are historical and do not verify this correction.

The preceding 0.6.0 release passed 301 tests; that count is historical.

The Chunk 01 screenshots were captured from the running 0.6.0 product with disposable synthetic state. Additional browser checks verified the AI preview at desktop and mobile widths, its required disclosure checkbox and rejection of a request without that disclosure. Provider transport and credential reading were blocked during screenshot capture. They remain historical evidence for that release.

These are development checks on synthetic scenarios; they are not a security certification or evidence of enterprise readiness.

Future priorities will be selected using observed user problems, current market evidence and measurable acceptance criteria. Potential value is a hypothesis until tested with an appropriate baseline.

## Repository boundary

This public repository contains showcase documentation and reviewed synthetic screenshots. The product implementation and its source history are maintained in a separate private repository. Personal publishing tools are a separate private project. This showcase contains no source-code distribution, live application or confidential procurement data.

Public showcase: [Procurement Intelligence Lab on GitHub](https://github.com/mmdoh1995/procurement-intelligence-lab-showcase).

Feedback is welcome: which handoff causes the most avoidable rework in your procurement process—planning, intake completeness, approval ownership or understanding cycle time?
