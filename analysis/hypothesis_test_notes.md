# Hypothesis Test Notes

## Business Objective

The company wants to determine whether the new onboarding and activation campaign (Treatment group) performs better than the existing onboarding experience (Control group) in converting users into paid subscribers.

---

## Metric Being Tested

**Paid Conversion Rate (converted_to_paid)**

Paid Conversion Rate is calculated as:

Paid Conversion Rate = Number of users converted to paid / Total number of users

This is the primary KPI because it directly measures the success of the onboarding campaign and its impact on business revenue.

---

## Null Hypothesis (H₀)

There is no statistically significant difference in the paid conversion rate between the Control group and the Treatment group.

**H₀:** Paid Conversion Rate (Treatment) ≤ Paid Conversion Rate (Control)

---

## Alternate Hypothesis (H₁)

The Treatment group has a higher paid conversion rate than the Control group.

**H₁:** Paid Conversion Rate (Treatment) > Paid Conversion Rate (Control)

---

## Type of Test

**One-tailed hypothesis test**

A one-tailed test is appropriate because the business objective is specifically to determine whether the new onboarding campaign improves paid conversions, not simply whether it is different.

---

## Significance Level

**α = 0.05 (5%)**

A significance level of 5% is used, meaning that if the p-value is less than 0.05, the null hypothesis will be rejected.

---

## Reason for Choosing This Metric

Paid Conversion Rate is the company's North Star Metric and directly reflects business growth. An increase in this metric means more users become paying customers, resulting in higher subscription revenue and improved return on investment for the onboarding campaign.

---

## Interpretation Logic

- If **p-value < 0.05**, reject the null hypothesis and conclude that the new onboarding campaign significantly improves paid conversion rates. Recommend rolling out the Treatment experience to all users, provided guardrail metrics remain acceptable.

- If **p-value ≥ 0.05**, fail to reject the null hypothesis and conclude that there is insufficient evidence that the Treatment outperforms the Control. Recommend maintaining the existing onboarding experience or conducting further experiments.

---

## Business Decision Connection

The hypothesis test provides statistical evidence for deciding whether the new onboarding campaign should be launched to all users. The final recommendation will consider both the improvement in paid conversion rate and the performance of guardrail metrics such as refund rate, support ticket rate, revenue, and engagement score.
