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

Data Cleaning & Preparation

The experiment dataset was reviewed and prepared before performing the KPI and A/B experiment analysis. The following data quality checks were conducted.

1. Missing Values
Total Missing Values: 1,392
Handling

The missing values were reviewed to determine whether they represented data quality issues or expected business scenarios.

Missing values in categorical fields were treated as "Unknown" where appropriate.
Missing values in fields such as conversion-related attributes were retained if they represented users who had not completed the corresponding action.
Since the missing values did not significantly impact the experiment groups, no records were removed.
2. Group Counts

The distribution of users across the experiment groups was checked to ensure a balanced A/B test.

Experiment Group	User Count
Control	693
Treatment	715
Total	1408
Observation

The Control and Treatment groups have similar sample sizes, indicating a reasonably balanced experiment suitable for comparison.

3. Duplicate User IDs

A duplicate check was performed using the user_id field.

Duplicate User IDs Found: 16
Handling

Duplicate records were identified and removed, ensuring that each user is represented only once in the experiment analysis.

4. Invalid Binary Values

The following binary columns were validated:

visited_landing_page
started_trial
completed_onboarding
converted_to_paid
refund_requested
Result
Invalid Binary Values Found: 0
Handling

All binary variables contained only valid values (0 and 1). Therefore, no corrections were required.

5. Revenue Outliers

Outliers in revenue_30d were identified using the IQR (Interquartile Range) method.

Revenue Outliers Detected: 72
Handling

The identified outliers were retained because they represent genuine high-value customers rather than data entry errors. Removing these observations would distort the business analysis and underestimate actual revenue performance.

6. Segment Distribution Across Groups

The distribution of user segments was evaluated using Pivot Tables.

Region Distribution
Region	Control	Treatment
East	158	172
North	203	180
South	184	184
West	148	179
Observation
Region distribution is reasonably balanced across both experiment groups.
No single region dominates either group.
Device Type Distribution
Desktop: 414
Mobile: 864
Tablet: 112
Missing/Blank: 18
Traffic Source Distribution
Email: 130
Organic: 487
Paid Search: 332
Referral: 172
Social: 263
Missing/Blank: 24
Plan Type Distribution
Basic: 458
Free: 729
Premium: 221
Overall Observation

The distributions across region, device type, traffic source, and plan type are reasonably balanced. Minor missing values are minimal and are not expected to introduce bias into the experiment.
* Low-quality users may convert but generate little long-term revenue.
* User engagement may decline even if short-term conversions improve.

Therefore, the North Star metric should always be evaluated alongside guardrail metrics such as **refund_requested**, **support_tickets_30d**, **revenue_30d**, and **engagement_score** to ensure that business growth is both profitable and sustainable.

| **Metric**                             | **Control** | **Treatment** |
| -------------------------------------- | ----------- | ------------- |
| **User Count**                         | **693**     | **715**       |
| **Landing Page Visit Rate**            | **63.64%**  | **72.59%**    |
| **Trial Start Rate**                   | **25.11%**  | **29.09%**    |
| **Onboarding Completion Rate**         | **15.58%**  | **21.26%**    |
| **Paid Conversion Rate**               | **3.17%**   | **6.99%**     |
| **Average Revenue per User**           | **51.75**   | **53.88**     |
| **Average Revenue per Converted User** | **1630.10** | **770.41**    |
| **Refund Rate**                        | **0.00%**   | **0.42%**     |
| **Support Ticket Rate**                | **14.72%**  | **24.58%**    |
| **Average Engagement Score**           | **57.03**   | **62.69**     |
| **Average Days to Convert**            | **8.86**    | **6.40**      |

Guardrail Metric Evaluation

While the Treatment group shows a significant improvement in Paid Conversion Rate (6.99% vs 3.17%), additional guardrail metrics must be evaluated to ensure that the improvement does not negatively impact the overall user experience or business performance.

Guardrail Metric	Control	Treatment	Evaluation
Refund Rate	0.00%	0.42%	Slight increase in refunds, but the rate remains very low and does not represent a major business risk.
Support Ticket Rate	14.72%	24.58%	Significant increase in support requests, indicating that users may require additional assistance during the new onboarding process.
Average Days to Convert	8.86 days	6.40 days	Positive outcome. Users convert more quickly, improving activation and reducing time to revenue.
Average Engagement Score	57.03	62.69	Positive outcome. Higher engagement suggests that users interact more effectively with the new onboarding experience.
Average Revenue per User	51.75	53.88	Slight improvement in revenue generated per user, supporting business growth.
Risk Assessment
1. Refund Rate

The refund rate increased slightly from 0.00% to 0.42%. Although this represents an increase, the overall percentage remains very low and is unlikely to have a significant financial impact.

Risk Level: Low 

2. Support Ticket Rate

The support ticket rate increased from 14.72% to 24.58%.

This suggests that the new onboarding experience may create confusion or require additional customer support.

Risk Level: Moderate 

This metric should be monitored closely after rollout, and improvements to onboarding instructions or FAQs may help reduce support requests.

3. Average Days to Convert

Users in the Treatment group converted in 6.40 days, compared with 8.86 days in the Control group.

This indicates that the new campaign helps users become paying customers more quickly.

Risk Level: None 

4. Average Engagement Score

The Treatment group's engagement score increased from 57.03 to 62.69.

Higher engagement indicates a better user experience and increases the likelihood of long-term retention.

Risk Level: None 

5. Revenue Quality

Average revenue per user increased from 51.75 to 53.88, suggesting that the increase in conversions is accompanied by slightly higher revenue generation rather than low-quality acquisitions.

Risk Level: Low 

Overall Guardrail Evaluation

The Treatment group demonstrates substantial improvements in paid conversion rate, engagement score, average revenue per user, and speed of conversion.

The only notable concern is the increase in support ticket rate, which may indicate onboarding complexity. However, this risk appears manageable and does not outweigh the significant improvement in the primary business metric.

Conclusion: The guardrail metrics do not present sufficient risk to prevent rollout. The Treatment campaign can be recommended for deployment while monitoring customer support requests and optimizing the onboarding experience.

Summary metrices
<img width="649" height="525" alt="image" src="https://github.com/user-attachments/assets/4756c6e6-5da0-40a3-88e8-a9267ac50503" />

Hypothesis metrice
<img width="552" height="337" alt="image" src="https://github.com/user-attachments/assets/564cd4e6-a258-4dcf-ba03-de0a30da9f17" />

k-tree


