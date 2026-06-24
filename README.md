# Task 1: Understand the Business Problem
## Business Problem Statement

The company must decide whether the new onboarding and activation campaign should be launched to all users. This decision impacts end users, the marketing team, the support team, and business leadership.

The primary objective of the campaign is to improve the Paid Conversion Rate, which measures the percentage of users who convert into paying subscribers. Improving this metric directly supports business growth and revenue generation.

Before making a rollout decision, the company must monitor potential risks such as higher refund rates, increased support ticket rates, lower user engagement, and longer conversion times. While a campaign may improve conversion, it should not negatively affect customer experience or revenue quality.

To support the recommendation, the experiment results must be analyzed using A/B testing techniques. The treatment group's performance should be compared with the control group, statistical significance should be verified through hypothesis testing, and guardrail metrics should be evaluated to ensure that the treatment delivers sustainable business value.

# Task 2: Define the North Star Metric

## Selected North Star Metric: Paid Conversion Rate

The North Star Metric selected for this experiment is **Paid Conversion Rate**, which measures the percentage of users who convert into paying subscribers. This metric is the primary success metric because the main objective of the onboarding and activation campaign is to increase the number of users who become paying customers. An improvement in Paid Conversion Rate directly contributes to revenue growth and business performance.

Other metrics such as Landing Page Visit Rate, Trial Start Rate, Onboarding Completion Rate, and Engagement Score are considered supporting metrics because they represent different stages of the customer journey that influence conversion. While these metrics help explain user behavior and identify improvement opportunities, they do not directly measure business success in the same way as Paid Conversion Rate.

Paid Conversion Rate is closely linked to business growth because an increase in paying customers leads to higher recurring revenue, improved customer lifetime value, and stronger overall business performance. A successful onboarding experience should ultimately result in more users converting to paid subscriptions.

However, this metric should not be optimized blindly. A higher Paid Conversion Rate may not always indicate a better customer experience. For example, aggressive onboarding tactics could increase conversions while also increasing refund requests, support tickets, or reducing long-term user engagement. Therefore, guardrail metrics such as Refund Rate, Support Ticket Rate, Days to Convert, and Engagement Score must be monitored alongside the North Star Metric to ensure sustainable and high-quality growth.

# Task 4: Clean and Prepare Experiment Data

The dataset was reviewed and validated before performing experiment analysis. Data quality checks were conducted separately for the Control and Treatment groups.

## 1. Missing Values

| Column           | Control | Treatment |
| ---------------- | ------: | --------: |
| device_type      |       9 |         9 |
| traffic_source   |       6 |        18 |
| days_to_convert  |     671 |       665 |
| engagement_score |       6 |         8 |

**Observations:**

* Missing values were found in device_type, traffic_source, days_to_convert, and engagement_score.
* Missing values in days_to_convert are expected because many users did not convert to a paid subscription during the experiment period.
* No records were removed during the audit.

---

## 2. Group Counts

| Experiment Group | Count |
| ---------------- | ----: |
| Control          |   693 |
| Treatment        |   715 |

**Observations:**

* The experiment groups are reasonably balanced and suitable for comparison.

---

## 3. Duplicate User IDs

| Metric            | Control | Treatment |
| ----------------- | ------: | --------: |
| Duplicate Pairs   |       3 |         5 |
| Duplicate Records |       6 |        10 |

**Observations:**

* Duplicate user IDs were identified in both groups and documented for review.

---

## 4. Invalid Binary Values

The following binary fields were checked:

* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* refund_requested

| Group     | Invalid Values Found |
| --------- | -------------------: |
| Control   |                    0 |
| Treatment |                    0 |

**Observations:**

* All binary fields contained only valid values (0 or 1).
* No invalid binary values were identified.

---

## 5. Revenue Outliers

Revenue contains a large number of zero values because most users did not convert to paid subscriptions. Therefore, revenue outlier analysis was performed only on converted users using the IQR method.

| Metric           | Control | Treatment |
| ---------------- | ------: | --------: |
| Converted Users  |      22 |        50 |
| Revenue Outliers |       3 |         2 |

**Observations:**

* Three revenue outliers were identified in the Control group.
* Two revenue outliers were identified in the Treatment group.
* Outliers were identified using the IQR method on converted users only.

---

## 6. Segment Distribution Across User Groups

#### Region Distribution

| Region | Control | Treatment |
| ------ | ------: | --------: |
| North  |     203 |       180 |
| South  |     184 |       184 |
| East   |     158 |       172 |
| West   |     148 |       179 |

#### Device Type Distribution

| Device Type | Control | Treatment |
| ----------- | ------: | --------: |
| Mobile      |     428 |       436 |
| Desktop     |     200 |       214 |
| Tablet      |      56 |        56 |
| Missing     |       9 |         9 |

#### Traffic Source Distribution

| Traffic Source | Control | Treatment |
| -------------- | ------: | --------: |
| Organic        |     246 |       241 |
| Paid Search    |     156 |       176 |
| Social         |     130 |       133 |
| Referral       |      81 |        91 |
| Email          |      74 |        56 |
| Missing        |       6 |        18 |

#### Plan Type Distribution

| Plan Type | Control | Treatment |
| --------- | ------: | --------: |
| Free      |     361 |       368 |
| Basic     |     223 |       235 |
| Premium   |     109 |       112 |

**Observations:**

* Region, Device Type, Traffic Source, and Plan Type distributions are reasonably balanced across Control and Treatment groups.
* No major segment imbalance was identified that would invalidate experiment comparisons.

