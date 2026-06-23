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


# Task 2: North Star Metric

## Selected North Star Metric

**North Star Metric:** **Paid Conversion Rate (`converted_to_paid`)**

This metric measures the percentage of users who successfully become paid subscribers after experiencing the onboarding process.

## Why This Is the Main Success Metric

The objective of the experiment is to determine whether the new onboarding and activation campaign increases the number of users who convert into paying customers. Paid conversions directly contribute to the company's subscription revenue and indicate that the onboarding experience is effectively guiding users toward purchasing the product.

Unlike intermediate metrics, this metric represents the final business outcome that leadership wants to improve before deciding on a full rollout.

## Why Other Metrics Are Supporting Metrics

The remaining metrics provide additional insight into user behavior and campaign quality but do not directly measure business success.

| Metric                   | Why It Is a Supporting Metric                                                                    |
| ------------------------ | ------------------------------------------------------------------------------------------------ |
| **visited_landing_page** | Indicates initial interest but does not generate revenue.                                        |
| **started_trial**        | Shows user intent but does not guarantee payment.                                                |
| **completed_onboarding** | Measures process completion rather than business value.                                          |
| **revenue_30d**          | Complements conversion by measuring monetary value but can be influenced by pricing or user mix. |
| **engagement_score**     | Reflects user activity but does not necessarily lead to subscriptions.                           |
| **support_tickets_30d**  | A guardrail metric used to monitor user experience.                                              |
| **refund_requested**     | A guardrail metric used to measure conversion quality and customer satisfaction.                 |

These metrics help explain *why* conversions increase or decrease and ensure that business growth is sustainable.

## Connection to Business Growth

Improving the paid conversion rate directly impacts the company's growth by:

* Increasing the number of paying subscribers.
* Growing recurring subscription revenue.
* Improving customer acquisition efficiency.
* Increasing the lifetime value of acquired users.
* Maximizing the return on marketing and product investments.

A sustained increase in paid conversions enables the business to scale revenue without proportionally increasing acquisition costs.

## Risks of Optimizing This Metric Blindly

Focusing only on paid conversion rate can lead to poor business decisions.

Possible risks include:

* Users may convert initially but request refunds shortly afterward.
* Aggressive onboarding tactics may increase support tickets and reduce customer satisfaction.
* Low-quality users may convert but generate little long-term revenue.
* User engagement may decline even if short-term conversions improve.

Therefore, the North Star metric should always be evaluated alongside guardrail metrics such as **refund_requested**, **support_tickets_30d**, **revenue_30d**, and **engagement_score** to ensure that business growth is both profitable and sustainable.


