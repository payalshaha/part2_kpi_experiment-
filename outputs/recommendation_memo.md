## Business Problem Summary

The purpose of this experiment is to determine whether the new onboarding campaign should be launched to all users. The decision impacts product, marketing, customer success, revenue teams, and future users.

The primary success metric is Paid Conversion Rate, as it directly contributes to subscription growth and revenue. However, the decision cannot be based on conversion alone. Guardrail metrics such as refund rate, support ticket rate, engagement score, and days to convert must also be evaluated to ensure the new experience does not create unintended negative effects.

A final recommendation will be based on statistical evidence showing whether the Treatment group significantly outperforms the Control group while maintaining acceptable levels of user experience and business performance.


## North Star Metric

The North Star Metric selected for this experiment is Paid Conversion Rate. This metric directly measures the percentage of users who become paying subscribers and is the strongest indicator of business growth for a subscription-based product.

Supporting metrics such as Trial Start Rate, Onboarding Completion Rate, Revenue Per User, and Engagement Score help explain user behavior but do not directly represent the company's primary business objective.

While improving Paid Conversion Rate is important, it must be evaluated alongside guardrail metrics such as Refund Rate, Support Ticket Rate, and Engagement Score to ensure that conversion gains do not come at the expense of user satisfaction or long-term value.


# Recommendation Memo

## Executive Summary

The purpose of this experiment was to evaluate whether a new onboarding and activation campaign improves user conversion and early engagement compared to the existing onboarding experience.

A controlled A/B experiment was conducted with users randomly assigned to either a Control group (existing onboarding) or a Treatment group (new onboarding experience). The primary objective was to increase the Paid Conversion Rate while ensuring that other important business metrics were not negatively affected.

The analysis shows that the Treatment group significantly outperformed the Control group in Paid Conversion Rate and Engagement Score. Statistical testing confirmed that the improvement in conversion rate is statistically significant. While some guardrail metrics indicate potential risks, the overall business impact of the Treatment experience is positive.

---

# North Star Metric

### Paid Conversion Rate

Paid Conversion Rate was selected as the North Star Metric because the primary business goal of the onboarding campaign is to increase the number of users who become paying customers.

Formula:

Paid Conversion Rate = Paid Conversions ÷ Total Users

This metric directly contributes to subscription growth and long-term revenue generation.

---

# KPI Tree Explanation

The KPI Tree was designed around Paid Conversion Rate as the North Star Metric.

### Primary KPI Drivers

#### 1. User Acquisition

* Landing Page Visit Rate
* Trial Start Rate

#### 2. User Activation

* Onboarding Completion Rate
* Days to Convert

#### 3. User Engagement

* Engagement Score
* Product Usage / Feature Adoption

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Revenue Quality
* Segment-Level Performance

These metrics ensure that conversion growth is achieved without creating negative customer or business outcomes.

---

# Experiment Result Summary

| Metric                   | Control | Treatment |
| ------------------------ | ------: | --------: |
| Users                    |     693 |       715 |
| Paid Conversion Rate     |   3.17% |     6.99% |
| Average Revenue Per User |   51.75 |     53.88 |
| Refund Rate              |   0.00% |     0.42% |
| Support Ticket Rate      |  14.72% |    24.76% |
| Average Engagement Score |   57.03 |     62.93 |
| Average Days to Convert  |    8.86 |      6.40 |

Key findings:

* Paid Conversion Rate more than doubled.
* Users converted faster in the Treatment group.
* Engagement improved significantly.
* Revenue per user increased slightly.
* Support tickets increased noticeably.

---

# Hypothesis Test Interpretation

A One-Tailed Two-Sample Statistical Test was performed to determine whether the Treatment group improved Paid Conversion Rate.

### Test Results

| Statistic                 |    Value |
| ------------------------- | -------: |
| Control Conversion Rate   |    3.17% |
| Treatment Conversion Rate |    6.99% |
| t Statistic               |  -3.2801 |
| One-Tailed P-Value        | 0.000533 |
| Significance Level        |     0.05 |

### Decision

Since:

P-Value = 0.000533 < 0.05

The Null Hypothesis was rejected.

### Interpretation

The increase in Paid Conversion Rate is statistically significant and unlikely to be caused by random variation. The new onboarding campaign demonstrates a meaningful improvement in conversion performance.

---

# Guardrail Analysis

### Refund Rate

The Treatment group showed a small increase in refund requests. Although higher than the Control group, the overall refund rate remains very low and does not currently represent a major business risk.

### Support Ticket Rate

Support Ticket Rate increased substantially in the Treatment group. This suggests that some users may be experiencing confusion or friction during onboarding. This is the most important risk identified in the experiment.

### Engagement Score

Engagement Score improved from 57.03 to 62.93. Higher engagement indicates that users are interacting more actively with the product after onboarding.

### Days to Convert

The Treatment group converted approximately 2.5 days faster than the Control group. Faster conversion accelerates revenue realization and indicates a more effective onboarding process.

### Revenue Quality

Revenue per user increased slightly; however, revenue per converted customer declined. This suggests that the campaign may be attracting a larger number of lower-value customers.

---

# Segment-Level Insights

Segment analysis was performed using business dimensions such as Region, Device Type, Traffic Source, and Plan Type.

Key observations:

* Most segments showed improved conversion performance under the Treatment experience.
* No major segment experienced a severe decline in conversion performance.
* Mobile users showed particularly strong engagement improvements.
* Traffic sources with higher onboarding completion rates also demonstrated stronger conversion gains.

Overall, the Treatment campaign produced positive results across the majority of analyzed segments.

---

# Final Recommendation

## Launch

Based on the experiment results, the Treatment onboarding experience should be launched.

### Supporting Evidence

* Paid Conversion Rate increased from 3.17% to 6.99%.
* Statistical testing confirmed significance (p-value = 0.000533).
* Engagement Score improved substantially.
* Users converted faster.
* Revenue per user increased slightly.

Although Support Ticket Rate increased, the overall business benefits outweigh the identified risks.

---

# Risks and Limitations

### Risks

* Increased support ticket volume may increase operational costs.
* Revenue per converted user declined.
* Refund rate increased slightly.

### Limitations

* The experiment measures short-term outcomes only.
* Long-term retention and customer lifetime value were not evaluated.
* Future user behavior may differ from the experiment sample.

---

# Next Steps

1. Launch the Treatment onboarding experience to all users.
2. Monitor Support Ticket Rate closely after launch.
3. Investigate onboarding steps generating the most support requests.
4. Track long-term retention and customer lifetime value.
5. Continue monitoring refund behavior and revenue quality.
6. Conduct follow-up experiments to further optimize onboarding performance.

---

# Conclusion

The Treatment onboarding campaign generated a statistically significant improvement in Paid Conversion Rate while also improving engagement and reducing time to conversion.

Although some operational risks were identified, particularly the increase in support tickets, the overall business impact is positive. Based on the available evidence, the Treatment experience should be launched while continuing to monitor guardrail metrics after deployment.

