# Task 1: Understand the Business Problem

### Business Problem Summary

The objective of this experiment is to determine whether the new onboarding and activation campaign should be launched to all users. The success of the campaign will be measured using Paid Conversion Rate, while guardrail metrics such as Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert will be monitored. A recommendation will be based on A/B test results, statistical significance, and overall business impact.

# Recommendation Memo

## Executive Summary

An A/B experiment was conducted to evaluate whether a new onboarding and activation campaign improves the Paid Conversion Rate for a subscription-based digital product company. The analysis shows that the Treatment group achieved a statistically significant improvement in the primary business metric. However, guardrail metrics were also evaluated to ensure that the improvement does not negatively impact customer experience or long-term business performance.

---

## North Star Metric

The North Star Metric for this experiment is **Paid Conversion Rate** because it directly measures the percentage of users who become paying subscribers. An improvement in this metric directly supports revenue growth and aligns with the business objective of increasing paid subscriptions.

---

## KPI Tree Explanation

The KPI Tree is structured around **Paid Conversion Rate** as the primary business outcome.

The primary KPI drivers are:

- Acquisition
- Activation
- Engagement

These drivers are supported by sub-drivers such as:

- Landing Page Visit Rate
- Traffic Source Quality
- Trial Start Rate
- Onboarding Completion Rate
- Product Usage
- User Interaction Score

The experiment also monitors the following guardrail metrics:

- Refund Rate
- Support Ticket Rate
- Days to Convert

These guardrails ensure that improvements in conversion do not negatively affect customer experience or business performance.

---

## Experiment Result Summary

The experiment compared the Control and Treatment groups using unique users.

Key findings include:

- Control Users: **690**
- Treatment Users: **710**
- Paid Conversions:
  - Control: **22**
  - Treatment: **50**
- Paid Conversion Rate:
  - Control: **3.19%**
  - Treatment: **7.04%**
- Absolute Improvement:
  - **3.85 percentage points**
- Relative Lift:
  - **120.69%**

The Treatment group achieved a higher Paid Conversion Rate than the Control group.

---

## Hypothesis Test Interpretation

A **One-Tailed Two-Proportion Z-Test** was performed.

**Hypotheses**

- Null Hypothesis (H₀):
  There is no improvement in Paid Conversion Rate.

- Alternate Hypothesis (H₁):
  The Treatment increases Paid Conversion Rate.

**Results**

- Z Statistic: **3.26**
- P-value: **0.000557**
- Significance Level (α): **0.05**

Since the **P-value (0.000557) is less than 0.05**, the Null Hypothesis is rejected.

The increase in Paid Conversion Rate is **statistically significant** and is unlikely to have occurred by random chance.

---

## Guardrail Analysis

Although the Treatment improved the primary metric, additional guardrail metrics were evaluated.

### Positive observations

- Average Days to Convert decreased, indicating faster conversion.
- Average Engagement Score increased, indicating better user engagement.

### Risks identified

- Support Ticket Rate increased.
- Refund Rate increased slightly.
- Average Revenue per Converted User decreased.

The lower Average Revenue per Converted User should be interpreted carefully because the Control group contained a small number of exceptionally high-value customers, which increased the average revenue. The Treatment group converted substantially more users than the Control group.

---

## Segment-Level Insight

Segment-level analysis was performed across:

- Region
- Device Type
- Traffic Source
- Plan Type

The Treatment group generally showed improved performance across user segments while maintaining consistent user distribution between the Control and Treatment groups.

---

## Final Recommendation

**Recommendation: Launch only for selected segments (Phased Rollout).**

The experiment demonstrates a statistically significant improvement in Paid Conversion Rate. However, the increase in Support Ticket Rate and the slight increase in Refund Rate indicate that customer experience should continue to be monitored during rollout.

A phased rollout is recommended while monitoring:

- Support Ticket Rate
- Refund Rate
- Average Revenue per Converted User

If these guardrail metrics remain within acceptable business limits, the Treatment can be rolled out to the remaining users.

---

## Risks and Limitations

- The Control group contained a small number of high-value revenue outliers that influenced the Average Revenue per Converted User.
- Guardrail metrics should continue to be monitored after deployment.
- Business decisions should consider both statistical significance and operational impact.

---

## Next Steps

1. Deploy the Treatment through a phased rollout.
2. Continue monitoring all guardrail metrics.
3. Review Average Revenue per Converted User after rollout.
4. Continue measuring Paid Conversion Rate to confirm long-term business impact.
