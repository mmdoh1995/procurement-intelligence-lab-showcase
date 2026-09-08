# Procurement Intelligence Lab

Public progress showcase for a procurement product being built from practical procurement questions, with AI-assisted engineering.

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

This is a local, single-owner development product. Approvals and reminders are simulations. It does not place orders, reserve budget, contact suppliers, connect to an ERP or establish multi-user approval authority. Plan values, requisition values and allocations describe different views of demand and must not be added together as spend.

## AI-01 · Explain a synthetic SLA snapshot

The first AI capability is implemented as an owner-triggered explanation flow. It presents the authoritative SLA facts for review, asks for explicit agreement before sending those facts to OpenAI, and is designed to display advisory observations linked to evidence alongside what remains unknown.

![Actual AI snapshot explainer preview showing authoritative synthetic SLA facts and an explicit disclosure checkbox before requesting an explanation.](assets/chunk-01-ai-preview.png)

*Actual 0.6.0 preview screen. This image shows the review step; no generated answer has been inserted or fabricated.*

This first capability accepts only the unchanged bundled synthetic SLA facts. It cannot change calculations or take procurement actions. A citation points to an input fact; it does not prove that an AI-generated interpretation is correct. The person reviewing the explanation remains responsible for checking it.

**The request path and preview are implemented; live-provider validation and explanation-quality evaluation are still pending.** The screenshots do not demonstrate a successful live AI response. Later candidates include clarifying incomplete requests and identifying missing information, subject to evidence and testing.

## What has been checked

The 0.6.0 release passed **301 automated tests**, with no failures or skips. The suite blocks external network access. Desktop/mobile browser exercises, Windows launcher checks and an isolated installed-package check also passed.

The current screenshots were captured from the running 0.6.0 product with disposable synthetic state. Additional browser checks verify the AI preview at desktop and mobile widths, its required disclosure checkbox and rejection of a request without that disclosure. Provider transport and credential reading were blocked during screenshot capture.

These are development checks on synthetic scenarios; they are not a security certification or evidence of enterprise readiness.

Future priorities will be selected using observed user problems, current market evidence and measurable acceptance criteria. Potential value is a hypothesis until tested with an appropriate baseline.

## Repository boundary

This public repository contains showcase documentation and reviewed synthetic screenshots. The product implementation and its source history are maintained in a separate private repository. Personal publishing tools are a separate private project. This showcase contains no source-code distribution, live application or confidential procurement data.

Public showcase: [Procurement Intelligence Lab on GitHub](https://github.com/mmdoh1995/procurement-intelligence-lab-showcase).

Feedback is welcome: which handoff causes the most avoidable rework in your procurement process—planning, intake completeness, approval ownership or understanding cycle time?
