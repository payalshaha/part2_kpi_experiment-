## Business Problem Statement

The company has introduced a new onboarding and activation campaign designed to improve user conversion and early engagement for its subscription-based digital product. To evaluate the effectiveness of the new experience, users were randomly assigned to either a Control group (existing onboarding experience) or a Treatment group (new onboarding campaign).

The key business decision is whether the new onboarding experience should be rolled out to all users. This decision impacts multiple stakeholders, including the Product Team, Marketing Team, Customer Success Team, Revenue Team, company leadership, and future users of the platform.

The primary metric expected to improve is the **Paid Conversion Rate**, which measures the percentage of users who become paying subscribers after onboarding. Improvements in engagement, onboarding completion, and revenue generation are also important supporting outcomes.

Before making a launch decision, several risks must be monitored. These include increased refund requests, higher support ticket volumes, lower user engagement quality, slower conversion times, and poor performance within specific user segments. An improvement in conversion alone may not justify a full rollout if it negatively affects the overall user experience or business performance.

A recommendation will only be made after analyzing experiment results, comparing Control and Treatment performance, evaluating guardrail metrics, and conducting statistical hypothesis testing. The evidence must demonstrate that the Treatment group delivers a meaningful and statistically significant improvement in the primary success metric without creating unacceptable business risks.

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
