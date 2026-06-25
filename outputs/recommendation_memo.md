# Task 1: Understand the Business Problem

### Business Problem Summary

The objective of this experiment is to determine whether the new onboarding and activation campaign should be launched to all users. The success of the campaign will be measured using Paid Conversion Rate, while guardrail metrics such as Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert will be monitored. A recommendation will be based on A/B test results, statistical significance, and overall business impact.

# Task 9: Recommendation Memo

## Executive Summary

An A/B experiment was conducted to evaluate whether a new onboarding and activation campaign improves the Paid Conversion Rate for a subscription-based digital product company. The objective was to determine whether the new onboarding experience increases paid subscriptions while maintaining a positive customer experience and minimizing business risks.

The experiment demonstrated a statistically significant improvement in the primary business metric. However, guardrail metrics and segment-level performance were also evaluated before making the final recommendation.

---

# Experiment Summary

The experiment compared the Control and Treatment groups using unique users.

| Metric               | Control |              Treatment |
| -------------------- | ------: | ---------------------: |
| Total Users          |     690 |                    710 |
| Paid Conversions     |      22 |                     50 |
| Paid Conversion Rate |   3.19% |                  7.04% |
| Absolute Improvement |       - | 3.85 Percentage Points |
| Relative Lift        |       - |                 120.7% |

A One-Tailed Two-Proportion Z-Test was performed to compare the Paid Conversion Rate.

| Metric                 |    Value |
| ---------------------- | -------: |
| Z Statistic            |    3.264 |
| P-value                | 0.000557 |
| Significance Level (α) |     0.05 |

Since the **P-value (0.000557)** is less than **0.05**, the Null Hypothesis was rejected. The increase in Paid Conversion Rate is statistically significant and is unlikely to have occurred due to random chance.

---

# Guardrail Evaluation

In addition to the primary metric, several guardrail metrics were reviewed to evaluate the overall business impact.

### Positive Outcomes

* Paid Conversion Rate increased significantly.
* Average Days to Convert decreased, indicating that users completed the conversion journey more quickly.
* Average Engagement Score increased among converted users, suggesting that the new onboarding experience improved user interaction after conversion.

### Risks Identified

* Support Ticket Rate increased, indicating that some users required additional assistance during onboarding.
* Refund Rate increased slightly and should continue to be monitored.
* Average Revenue per Converted User decreased compared with the Control group.

The lower Average Revenue per Converted User should be interpreted carefully because the Control group contained a small number of exceptionally high-value customers. These revenue outliers increased the average revenue in the Control group and influenced the comparison. Since these were valid customer transactions rather than data errors, they were retained in the analysis.

---

# Segment-Level Insights

## Mobile Segment

The Mobile segment was the primary contributor to the success of the experiment.

* User Count: **426 (Control)** vs **432 (Treatment)**
* Paid Conversions: **11** vs **32**
* Total Revenue increased from **₹17,910.93** to **₹25,649.16**
* Average Engagement Score among converted users increased from **56** to **70**

The Mobile segment generated nearly two-thirds of all Treatment conversions and contributed the highest revenue among all device segments. However, converted Mobile users generated **17 support tickets from 10 unique users**, indicating that although the new onboarding experience successfully increased conversions, additional user support was required. This suggests an opportunity to further optimise the mobile onboarding experience.

## Desktop Segment

The Desktop segment also demonstrated positive behavioural improvements.

* User Count: **200 (Control)** vs **213 (Treatment)**
* Paid Conversions: **9** vs **14**
* Total Revenue decreased from approximately **₹16,989** to **₹8,765**
* Average Engagement Score among converted users increased from **54** to **70**

Although converted Desktop users were more engaged with the product after the new onboarding experience, the segment generated lower total revenue during the experiment. This difference appears to be influenced by a small number of high-value transactions in the Control group. Therefore, Desktop revenue performance should continue to be monitored during rollout.

---

# Final Recommendation

The experiment provides strong statistical evidence that the new onboarding and activation campaign improves Paid Conversion Rate.

However, the business decision should not rely solely on statistical significance. Guardrail metrics indicate that although user engagement and conversion performance improved, Support Ticket Rate also increased, suggesting that some users experienced friction during onboarding.

Based on the overall analysis, a **phased rollout** is recommended rather than an immediate rollout to all users.

The rollout should initially prioritise the **Mobile segment**, as it delivered the strongest improvement in paid conversions and revenue contribution. During deployment, the business should continue monitoring:

* Support Ticket Rate
* Refund Rate
* Average Revenue per Converted User
* Desktop revenue performance

If these guardrail metrics remain within acceptable business limits, the campaign can be confidently expanded to the remaining user segments.

---

# Conclusion

The Treatment successfully achieved the primary objective of increasing Paid Conversion Rate while maintaining positive user engagement. Although a few operational risks were identified, the overall business impact is favourable. A controlled phased rollout with continuous monitoring of guardrail metrics is therefore recommended.
