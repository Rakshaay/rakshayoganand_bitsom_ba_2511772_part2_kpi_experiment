# Business Problem Statement

## Overview

A subscription-based digital product company has introduced a new onboarding and activation campaign to improve the user journey and increase the number of paying customers. An A/B experiment was conducted where users were randomly assigned to either the existing onboarding experience (Control group) or the new onboarding experience (Treatment group).

## Business Decision

The primary business decision is whether the new onboarding campaign should be:

* Launched to all users,
* Rejected,
* Tested further, or
* Rolled out only for selected user segments.

## Stakeholders Impacted

This decision impacts:

* Product Management Team
* Marketing Team
* Business Leadership
* Customer Success Team
* New users interacting with the onboarding experience

## Primary Success Metric

The key metric that should improve is **converted_to_paid**, which measures whether a user becomes a paid customer after onboarding. An increase in paid conversions directly contributes to business growth and revenue.

## Risks and Guardrail Metrics

While improving conversion is important, the company must ensure that the campaign does not negatively affect customer experience or business quality. The following guardrail metrics should be monitored:

* **refund_requested** – Higher refunds may indicate poor-quality conversions.
* **support_tickets_30d** – An increase may suggest onboarding confusion or user frustration.
* **revenue_30d** – Revenue should remain stable or improve.
* **engagement_score** – User engagement should not decline after the new onboarding experience.

## Evidence Required

Before recommending a full rollout, the experiment should provide evidence that:

1. The Treatment group achieves a higher paid conversion rate than the Control group.
2. The improvement is statistically significant and not due to random variation.
3. Guardrail metrics do not deteriorate significantly.
4. Revenue and engagement remain stable or improve alongside higher conversions.

Only if both the primary KPI and the guardrail metrics produce favorable results should the new onboarding campaign be recommended for wider deployment.

