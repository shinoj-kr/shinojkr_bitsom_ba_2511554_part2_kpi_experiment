
# Task 6: Frame Hypotheses

## Null Hypothesis (H0)

The paid conversion rate of the Treatment group is equal to the paid conversion rate of the Control group. Any observed difference is due to random chance.

## Alternative Hypothesis (H1)

The paid conversion rate of the Treatment group is greater than the paid conversion rate of the Control group. The new onboarding and activation campaign improves paid conversions.

## Type of Test

A one-tailed hypothesis test will be used because the business objective is to determine whether the new onboarding and activation campaign increases the paid conversion rate. The experiment is not designed to test for any difference in either direction, but specifically for improvement.

## Significance Level

The significance level (α) used for this analysis is 0.05.

## Metric Being Tested

Paid Conversion Rate

Formula:

Paid Conversion Rate = Number of Paid Conversions / Total Users

## Reason for Choosing This Metric

Paid Conversion Rate was selected because it is the North Star Metric of the experiment. It directly measures the percentage of users who become paying subscribers and is closely linked to revenue growth and business success. An increase in paid conversions indicates that the onboarding and activation campaign is effectively encouraging users to subscribe.

## Interpretation Logic

If the p-value is less than 0.05, the null hypothesis will be rejected and the Treatment group will be considered to have achieved a statistically significant improvement in Paid Conversion Rate.

If the p-value is greater than or equal to 0.05, the null hypothesis will not be rejected and the observed difference may be due to random variation.

# Task 7: Hypothesis Test Results

## Summary of Test Inputs

| Metric               | Control | Treatment |
| -------------------- | ------: | --------: |
| Total Users          |     690 |       710 |
| Paid Conversions     |      22 |        50 |
| Paid Conversion Rate |   3.19% |     7.04% |

## Test Output

* Test Used: One-tailed Two-Proportion Z-Test
* Absolute Difference: 3.85%
* Relative Lift: 120.7%
* Pooled Conversion Rate: 5.14%
* Standard Error: 0.01181
* Z-Statistic: 3.264
* P-value: 0.000549

## Decision Rule

* Significance Level (α): 0.05
* Since the P-value (0.000549) is less than 0.05, the Null Hypothesis is rejected.

## Business Interpretation

The Treatment group achieved a statistically significant improvement in Paid Conversion Rate compared to the Control group. The increase from 3.19% to 7.04% is unlikely to have occurred by random chance. Therefore, the new onboarding and activation campaign successfully improved the primary business metric.

## Recommendation

Based on the statistical evidence, the Treatment campaign demonstrates a meaningful improvement in Paid Conversion Rate. However, before recommending a full rollout, the guardrail metrics such as refund rate, support ticket rate, engagement score, and average days to convert should also be reviewed to ensure there are no negative business impacts.

# Task 8: Evaluate Guardrail Metrics

The Treatment group achieved a statistically significant improvement in the primary metric, **Paid Conversion Rate**. However, additional guardrail metrics were evaluated to ensure that the improvement does not negatively impact customer experience or long-term business performance.

| Guardrail Metric                   |   Control | Treatment | Risk Assessment                                                                                                                                                                                                                                                                              |
| ---------------------------------- | --------: | --------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Refund Rate                        |     0.00% |     0.42% | Slight increase. The value is low but should be monitored after rollout.                                                                                                                                                                                                                     |
| Support Ticket Rate                |    14.78% |    24.93% | Increased noticeably, indicating that more users required assistance during onboarding. This is a potential operational risk.                                                                                                                                                                |
| Average Days to Convert            |      8.86 |      6.40 | Improved. Users converted more quickly, indicating a more effective onboarding experience.                                                                                                                                                                                                   |
| Average Engagement Score           |     56.78 |     62.57 | Improved, suggesting better user interaction and product engagement.                                                                                                                                                                                                                         |
| Average Revenue per Converted User | ₹1,630.10 |   ₹770.41 | Decreased. However, this result is influenced by a small number of exceptionally high-value customers in the Control group, which increased the average revenue. The Treatment group converted more than twice as many users (50 vs. 22), so this metric should be interpreted with caution. |

## Risk Assessment

The evaluation shows that the Treatment group improved the primary business objective by significantly increasing Paid Conversion Rate while also improving user engagement and reducing the average time required to convert.

The main concerns are the increase in Support Ticket Rate and the slight increase in Refund Rate, which may indicate that some users require additional guidance during the onboarding process. In addition, the lower Average Revenue per Converted User appears to be influenced by a few high-value customers in the Control group rather than indicating poorer overall revenue quality.

## Recommendation

The experiment provides strong statistical evidence that the new onboarding and activation campaign improves Paid Conversion Rate. Based on the overall results, a **phased rollout** of the Treatment is recommended rather than an immediate rollout to all users.

During the rollout, the business should closely monitor the following guardrail metrics:

* Support Ticket Rate
* Refund Rate
* Average Revenue per Converted User

If these metrics remain within acceptable business limits after rollout, the Treatment can be confidently deployed to the entire user base.


## Connection to Business Decision

The purpose of this hypothesis test is to determine whether the new onboarding and activation campaign should be rolled out to all users. A rollout recommendation will only be made if the Treatment group demonstrates a statistically significant improvement in Paid Conversion Rate and the guardrail metrics remain within acceptable limits.
