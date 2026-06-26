# A/B Testing Analysis for a Subscription-Based Digital Product

## 1. Business Context

### Business Problem Statement

The company must decide whether the new onboarding and activation campaign should be launched to all users. This decision impacts end users, the marketing team, the support team, and business leadership.

The primary objective of the campaign is to improve the  Paid Conversion Rate , which measures the percentage of users who convert into paying subscribers. Improving this metric directly supports revenue growth and long-term business performance.

Before making a rollout decision, the company must also monitor potential risks such as higher refund rates, increased support ticket rates, lower user engagement, and longer conversion times. While a campaign may improve conversion, it should not negatively affect customer experience or revenue quality.

The experiment results are analysed using A/B testing techniques, statistical hypothesis testing, KPI analysis, and guardrail metrics to determine whether the Treatment should be launched.

---

## 2. Dataset Description

The dataset contains user-level experiment data collected from an A/B test conducted for a subscription-based digital product.

Each record represents a user participating in either the  Control  or  Treatment  group.

The dataset contains information related to:

- User demographics and region
- Device type
- Traffic source
- Subscription plan
- Landing page visits
- Trial starts
- Onboarding completion
- Paid conversion
- Revenue generated
- Refund requests
- Support tickets
- Days to convert
- Engagement score

The dataset was cleaned and validated before statistical analysis.

---

## 3. North Star Metric

### Selected North Star Metric: Paid Conversion Rate

The North Star Metric selected for this experiment is  Paid Conversion Rate , which measures the percentage of users who convert into paying subscribers. This metric is the primary success metric because the objective of the onboarding campaign is to increase paid subscriptions.

Supporting metrics such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, and Engagement Score help explain user behaviour but do not directly represent business success.

Optimising Paid Conversion Rate alone may increase refunds, support requests, or reduce long-term engagement. Therefore, guardrail metrics are monitored alongside the North Star Metric to ensure sustainable business growth.

---

## 4. KPI Tree Summary

The KPI Tree was designed using  Paid Conversion Rate  as the North Star Metric.

### Primary Drivers

- Acquisition
- Activation
- Engagement

### Sub-Drivers

 Acquisition 
- Landing Page Visit Rate
- Traffic Source Quality

 Activation 
- Trial Start Rate
- Onboarding Completion Rate

 Engagement 
- Product Usage
- User Interaction Score

### Guardrail Metrics

- Refund Rate
- Support Ticket Rate
- Days to Convert

The KPI tree illustrates how improvements in user acquisition, activation, and engagement contribute to higher paid conversions while ensuring customer experience remains protected through guardrail metrics.

---

## 5. Experiment Analysis Approach

The experiment was analysed using the following approach:

1. Data quality validation
2. Missing value assessment
3. Duplicate user identification
4. Binary field validation
5. Revenue outlier detection using the IQR method
6. Segment distribution comparison
7. KPI comparison between Control and Treatment
8. One-Tailed Two-Proportion Z-Test for Paid Conversion Rate
9. Guardrail metric evaluation
10. Segment-level business analysis
11. Final business recommendation

---

## 6. Hypothesis Test Summary

A  One-Tailed Two-Proportion Z-Test  was performed to determine whether the Treatment group significantly improved Paid Conversion Rate.

### Hypotheses

 Null Hypothesis (H₀) 

The Treatment does not improve the Paid Conversion Rate.

 Alternative Hypothesis (H₁) 

The Treatment improves the Paid Conversion Rate.

### Test Summary

| Metric | Value |
|---------|------:|
| Control Users | 690 |
| Treatment Users | 710 |
| Control Conversion Rate | 3.19% |
| Treatment Conversion Rate | 7.04% |
| Absolute Improvement | 3.85% |
| Relative Lift | 120.69% |
| Z Statistic | 3.26 |
| P-value | 0.000557 |
| Significance Level | 0.05 |

Since the  P-value is less than 0.05 , the Null Hypothesis was rejected.

The Treatment group achieved a statistically significant improvement in Paid Conversion Rate.

---

## 7. Guardrail Metrics Considered

The following guardrail metrics were evaluated before making the rollout recommendation.

- Refund Rate
- Support Ticket Rate
- Average Days to Convert
- Average Revenue per Converted User
- Average Engagement Score

Although Paid Conversion Rate increased significantly, these metrics were reviewed to ensure that the improvement did not negatively affect customer experience or revenue quality.

The analysis identified an increase in Support Ticket Rate, indicating that the onboarding process may require further optimisation.

---

## 8. Final Recommendation

The Treatment achieved a statistically significant improvement in Paid Conversion Rate.

The Mobile segment contributed the majority of paid conversions and generated higher revenue than the Control group. Engagement among converted users also increased across both Mobile and Desktop segments.

However, Support Ticket Rate increased, and Desktop revenue should continue to be monitored because the Control group contained a small number of exceptionally high-value transactions.

 Recommendation:  Proceed with a  phased rollout , prioritising the Mobile segment while continuously monitoring Refund Rate, Support Ticket Rate, Average Revenue per Converted User, and Desktop revenue performance.

---

## 9. Assumptions and Limitations

- Revenue outliers were identified using the IQR method but retained because they represent valid business transactions.
- Missing values in  Days to Convert  were expected for users who did not convert.
- Duplicate user IDs were identified during data validation and excluded from hypothesis testing where unique-user analysis was required.
- Statistical significance does not guarantee long-term business success; ongoing monitoring after rollout is recommended.
- The experiment reflects user behaviour during the experiment period only.

---

## 10. Screenshots Included

The repository includes the following screenshots as supporting evidence.

| Screenshot | Description |
|------------|-------------|
|  summary_metrics.png  | Control vs Treatment summary metrics |
|  hypothesis_test_output.png  | One-Tailed Two-Proportion Z-Test calculations and results |
|  kpi_tree_preview.png  | KPI Tree showing the North Star Metric, KPI drivers, sub-drivers, and guardrail metrics |

