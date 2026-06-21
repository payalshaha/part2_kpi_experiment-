
## Business Problem Statement

The company has introduced a new onboarding and activation campaign designed to improve user conversion and early engagement for its subscription-based digital product. To evaluate the effectiveness of the new experience, users were randomly assigned to either a Control group (existing onboarding experience) or a Treatment group (new onboarding campaign).

The key business decision is whether the new onboarding experience should be rolled out to all users. This decision impacts multiple stakeholders, including the Product Team, Marketing Team, Customer Success Team, Revenue Team, company leadership, and future users of the platform.

The primary metric expected to improve is the **Paid Conversion Rate**, which measures the percentage of users who become paying subscribers after onboarding. Improvements in engagement, onboarding completion, and revenue generation are also important supporting outcomes.

Before making a launch decision, several risks must be monitored. These include increased refund requests, higher support ticket volumes, lower user engagement quality, slower conversion times, and poor performance within specific user segments. An improvement in conversion alone may not justify a full rollout if it negatively affects the overall user experience or business performance.

A recommendation will only be made after analyzing experiment results, comparing Control and Treatment performance, evaluating guardrail metrics, and conducting statistical hypothesis testing. The evidence must demonstrate that the Treatment group delivers a meaningful and statistically significant improvement in the primary success metric without creating unacceptable business risks.

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement. Users were randomly assigned to one of two groups:

* **Control Group:** Existing onboarding experience
* **Treatment Group:** New onboarding experience

The objective of this experiment was to determine whether the new onboarding campaign should be launched to all users based on its impact on conversion, engagement, and overall business performance.

# Dataset Description

The dataset contains user-level experiment data collected during the A/B test.

### Key Variables

* user_id
* group (Control/Treatment)
* landing_page_visit
* trial_started
* onboarding_completed
* converted_to_paid
* revenue_30d
* refund_requested
* support_ticket
* engagement_score
* days_to_convert
* region
* device_type
* traffic_source
* plan_type

The dataset was cleaned and validated before analysis.

### Data Validation Performed

* Missing value check
* Group count verification
* Duplicate User ID check
* Invalid binary value check
* Revenue outlier review
* Segment distribution comparison

Revenue was highly zero-inflated because only converted users generated revenue. High revenue values were retained because they represented legitimate customer purchases rather than data errors.

---



## North Star Metric: Paid Conversion Rate

### Definition

Paid Conversion Rate is defined as the percentage of users who become paying subscribers after experiencing the onboarding process.

Formula:

Paid Conversion Rate = (Number of Paid Conversions / Total Users) × 100

### Why This Is the Main Success Metric

Paid Conversion Rate is the most important metric for this experiment because the primary goal of the new onboarding campaign is to increase the number of users who convert into paying customers. Since the company operates a subscription-based business model, converting users into subscribers directly contributes to revenue generation and long-term business growth.

Unlike engagement or activity metrics, Paid Conversion Rate measures whether the onboarding experience successfully moves users to the company's desired business outcome: becoming paying customers.

### Why Other Metrics Are Supporting Metrics

Several metrics provide valuable insights into user behavior, but they do not directly measure business success. These metrics support the North Star Metric by helping explain why conversion rates increase or decrease.

Supporting Metrics:

* Landing Page Visit Rate: Indicates campaign reach and initial interest.
* Trial Start Rate: Measures how many users begin exploring the product.
* Onboarding Completion Rate: Shows whether users successfully complete onboarding.
* Average Revenue Per User (ARPU): Measures revenue generated across all users.
* Average Revenue Per Converted User: Evaluates the quality of converted customers.
* Engagement Score: Indicates user interaction and product adoption.

These metrics help identify drivers of conversion but do not independently represent the ultimate business objective.

### Connection to Business Growth

Paid Conversion Rate is directly linked to business growth because higher conversion rates result in more paying subscribers, increased recurring revenue, improved customer acquisition efficiency, and stronger return on marketing investment.

A successful onboarding experience that increases Paid Conversion Rate can significantly improve revenue without increasing user acquisition costs.

### Risks of Optimizing This Metric Blindly

Focusing only on Paid Conversion Rate may create unintended negative consequences. For example:

* Users may be pressured into converting before fully understanding the product.
* Refund requests may increase if users are dissatisfied after purchase.
* Support ticket volume may rise if the onboarding process becomes confusing.
* User engagement may decline even if conversions initially increase.
* Certain customer segments may perform worse despite overall improvements.

## KPI Tree Summary

The North Star Metric for this experiment is Paid Conversion Rate. This metric is influenced by four primary business drivers: Acquisition, Activation, Engagement, and Monetization.

Acquisition measures the ability to attract users to the product through Landing Page Visit Rate and Traffic Quality. Activation evaluates whether users successfully begin and complete onboarding through Trial Start Rate and Onboarding Completion Rate.

Engagement measures how actively users interact with the product using Engagement Score and Days to Convert. Monetization evaluates the financial impact through Average Revenue Per User and Average Revenue Per Converted User.

To ensure improvements in conversion do not create unintended negative effects, guardrail metrics including Refund Rate, Support Ticket Rate, and Segment-Level Performance are monitored throughout the experiment.

For this reason, Paid Conversion Rate must be evaluated together with guardrail metrics such as Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert before making a final recommendation.

# Experiment Analysis Approach

The experiment compared Control and Treatment groups across key business metrics.

### Metrics Analyzed

* User Count
* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Average Revenue Per User
* Average Revenue Per Converted User
* Refund Rate
* Support Ticket Rate
* Engagement Score
* Average Days to Convert

### Segment Analysis

The following dimensions were analyzed:

* Region
* Device Type
* Traffic Source
* Plan Type

The objective was to identify overall treatment performance and detect any segment-level risks.

## Data Cleaning and Preparation

Before performing experiment analysis, the dataset was reviewed for data quality issues to ensure accurate and reliable results.

### 1. Missing Values Check

A missing value assessment was performed across all columns.

Findings:

| Column           | Missing Values |
| ---------------- | -------------: |
| device_type      |              9 |
| traffic_source   |             18 |
| engagement_score |              8 |
| days_to_convert  |            657 |

Handling:

* Missing values in `device_type` were replaced with **"Unknown"** for segment analysis.
* Missing values in `traffic_source` were replaced with **"Unknown"**.
* Missing values in `engagement_score` were retained and excluded from average calculations.
* Missing values in `days_to_convert` were expected because most users did not convert to paid status. These values were not treated as data quality issues and were excluded from conversion-time calculations.

### 2. Group Count Validation

The distribution of users across experiment groups was checked to confirm a balanced experiment design.

| Group     | User Count |
| --------- | ---------: |
| Control   |        693 |
| Treatment |        715 |

The group sizes were reasonably balanced and suitable for comparison.

### 3. Duplicate User ID Check

A duplicate check was performed on the `user_id` field.

Findings:

* 8 duplicate user IDs were identified.

Handling:

* Duplicate records were investigated and flagged for review.
* User-level analyses were performed carefully to avoid potential double-counting effects.

### 4. Invalid Binary Value Check

The following binary fields were validated:

* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* refund_requested

Findings:

* All values were valid.
* No values outside the expected range of 0 and 1 were detected.

### 5. Revenue Outlier Check
Revenue values were examined to identify potential outliers.

The revenue distribution was highly zero-inflated because only users who converted to a paid subscription generated revenue. As a result, more than 75% of the revenue observations were equal to zero, causing both the first quartile (Q1) and third quartile (Q3) to be calculated as zero.

Q1 = 0
Q3 = 0
IQR = Q3 − Q1 = 0

Because the Interquartile Range (IQR) was zero, the traditional IQR-based outlier detection method was not informative for this dataset. Therefore, a Box & Whisker chart and descriptive review of the revenue values were used to identify unusually large revenue observations.

High revenue values were retained in the dataset because they represent legitimate customer purchases and business outcomes rather than data entry errors or invalid records.

**Conclusion:** No revenue records were removed from the analysis.

### 6. Segment Distribution Check

Segment distributions were compared between Control and Treatment groups.

Region Distribution:

| Region | Control | Treatment |
| ------ | ------: | --------: |
| North  |     203 |       180 |
| South  |     184 |       184 |
| East   |     158 |       172 |
| West   |     148 |       179 |

Additional checks were also performed for:

* Device Type
* Traffic Source
* Plan Type

The distributions were reasonably balanced across experiment groups, indicating that randomization was successful and no major segment bias was detected.

### Summary

The dataset was determined to be suitable for experiment analysis after addressing missing values, validating binary fields, reviewing duplicates, examining revenue outliers, and confirming balanced segment distributions across Control and Treatment groups.

## Data Cleaning and Preparation

The dataset was reviewed before analysis to ensure data quality and reliability.

The following checks were performed:

1. Missing values were identified using COUNTBLANK() and reviewed for all columns.
2. Group counts were verified using Pivot Tables to confirm a balanced Control and Treatment distribution.
3. Duplicate User IDs were detected using COUNTIF() and flagged for review.
4. Binary variables were validated to ensure values contained only 0 or 1.
5. Revenue outliers were identified using the IQR (Interquartile Range) method .
6. Segment distributions across Region, Device Type, and Traffic Source were compared between Control and Treatment groups using Pivot Tables.

The dataset was determined to be suitable for experiment analysis after completing these validation checks.

# Hypothesis Test Summary

## Business Question

Does the Treatment onboarding experience significantly improve Paid Conversion Rate compared to the Control experience?

### Null Hypothesis (H₀)

Treatment Conversion Rate ≤ Control Conversion Rate

### Alternative Hypothesis (H₁)

Treatment Conversion Rate > Control Conversion Rate

### Test Used

Two-Sample t-Test Assuming Unequal Variances

### Significance Level

α = 0.05

### Results

| Metric                    |    Value |
| ------------------------- | -------: |
| Control Conversion Rate   |    3.17% |
| Treatment Conversion Rate |    6.99% |
| One-Tailed P-Value        | 0.000533 |

### Interpretation

Since:

0.000533 < 0.05

The null hypothesis was rejected.

The Treatment group demonstrated a statistically significant improvement in Paid Conversion Rate.

# Guardrail Metric Evaluation

While the Treatment group demonstrated a statistically significant improvement in Paid Conversion Rate, additional guardrail metrics were evaluated to ensure that the increase in conversions does not negatively impact overall business performance.

## 1. Refund Rate

| Group     | Refund Rate |
| --------- | ----------: |
| Control   |       0.00% |
| Treatment |       0.42% |

### Evaluation

The Treatment group shows a slight increase in refund requests compared to the Control group.

### Risk Assessment

Low Risk

Although refunds increased, the overall refund rate remains below 1% and is not currently large enough to outweigh the conversion gains. However, this metric should continue to be monitored after launch.

---

## 2. Support Ticket Rate

| Group     | Support Ticket Rate |
| --------- | ------------------: |
| Control   |              9.23% |
| Treatment |              16.08% |

### Evaluation

The Treatment group generated substantially more support tickets than the Control group.

### Risk Assessment

Moderate Risk

The increase in support tickets suggests that some users may be experiencing confusion, onboarding friction, or technical issues with the new experience. A higher support workload may increase operational costs and negatively affect customer satisfaction.

This is the most significant guardrail concern identified in the experiment.

---

## 3. Average Days to Convert

| Group     | Average Days to Convert |
| --------- | ----------------------: |
| Control   |               8.86 Days |
| Treatment |               6.40 Days |

### Evaluation

Users in the Treatment group converted approximately 2.5 days faster than users in the Control group.

### Risk Assessment

Positive Outcome

Faster conversion indicates a more effective onboarding experience and allows the business to generate revenue sooner. No risk was identified for this metric.

---

## 4. Average Engagement Score

| Group     | Average Engagement Score |
| --------- | -----------------------: |
| Control   |                    57.03 |
| Treatment |                    62.93 |

### Evaluation

The Treatment group achieved a higher engagement score than the Control group.

### Risk Assessment

Positive Outcome

Higher engagement suggests that users interact more actively with the product after onboarding. Increased engagement is generally associated with stronger retention and long-term customer value.

---

## 5. Revenue Quality

| Group     | Average Revenue Per User | Average Revenue Per Converted User |
| --------- | -----------------------: | ---------------------------------: |
| Control   |                    51.75 |                            1630.10 |
| Treatment |                    53.88 |                             770.41 |

### Evaluation

The Treatment group generated slightly higher revenue per user, but lower revenue per converted user.

### Risk Assessment

Moderate Risk

The campaign successfully converts more users, but the average spending per converted customer is lower. This may indicate that additional lower-value customers are being acquired.

Further monitoring is recommended to determine whether these users generate long-term value.

---

## Overall Guardrail Assessment

### Positive Findings

* Paid Conversion Rate increased significantly.
* Engagement Score improved.
* Days to Convert decreased.
* Revenue Per User increased slightly.

### Risks Identified

* Support Ticket Rate increased substantially.
* Refund Rate increased slightly.
* Revenue Per Converted User decreased.

### Conclusion

The Treatment campaign delivers strong conversion improvements and positive engagement outcomes. However, the increase in support tickets and decline in revenue per converted customer indicate potential operational and revenue-quality risks.

# Final Recommendation

## Launch

The Treatment onboarding experience is recommended for launch.

### Supporting Evidence

* Paid Conversion Rate increased from 3.17% to 6.99%
* Statistical significance confirmed (p-value = 0.000533)
* Engagement Score improved
* Users converted faster
* Revenue per user increased slightly

Although Support Ticket Rate increased, the overall business impact remains positive and the conversion gains outweigh the identified risks.

---

# Assumptions and Limitations

## Assumptions

* Users were randomly assigned to experiment groups.
* Experiment data accurately reflects user behavior.
* Revenue values represent valid customer purchases.

## Limitations

* Analysis focuses on short-term outcomes.
* Long-term retention was not measured.
* Customer Lifetime Value (CLV) was unavailable.
* Results may vary after full-scale deployment.

# Screenshots Included

### summary_metrics.png

Control vs Treatment experiment summary table.

### hypothesis_test_output.png

Statistical test output and p-value evidence.

### kpi_tree_preview.png

Preview of the KPI Tree used in the analysis.

These risks are not severe enough to offset the conversion gains, but they should be monitored closely if the Treatment experience is launched.

