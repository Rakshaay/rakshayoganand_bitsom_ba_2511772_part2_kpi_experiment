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


# Hypothesis Test Results

## Test Used

Two-Sample Proportion Z-Test

## Test Inputs

Control Users: 693

Treatment Users: 715

Control Conversions: 22

Treatment Conversions: 50

Control Conversion Rate: 3.17%

Treatment Conversion Rate: 6.99%

## Test Output

Z-score: 3.25

P-value: 0.00058

Significance Level: 0.05

## Decision Rule

If p-value < 0.05, reject the null hypothesis.

## Result

Since the p-value (0.00058) is less than the significance level (0.05), the null hypothesis is rejected.

There is statistically significant evidence that the new onboarding campaign increases the paid conversion rate.

## Business Interpretation

The Treatment group achieved a paid conversion rate of 6.99%, compared to 3.17% for the Control group.

This represents more than a twofold improvement in paid conversions and is statistically significant.

However, before recommending a full rollout, leadership should also review guardrail metrics such as refund rate and support ticket rate to ensure that the increase in conversions does not negatively impact customer experience.
