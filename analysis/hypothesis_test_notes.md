
# Hypothesis Test Notes

## Metric Being Tested

Paid Conversion Rate

Formula:

Paid Conversion Rate = (Number of Users Converted to Paid / Total Users) × 100

This metric was selected because it is the North Star Metric for the experiment and directly measures the primary business objective of increasing paid subscriptions.

---

## Business Question

Does the new onboarding and activation campaign significantly increase the Paid Conversion Rate compared to the existing onboarding experience?

The answer to this question will help determine whether the Treatment experience should be launched to all users.

---

## Null Hypothesis (H₀)

The Paid Conversion Rate of the Treatment group is less than or equal to the Paid Conversion Rate of the Control group.

H₀: p(Treatment) ≤ p(Control)

This means the new onboarding campaign does not provide a meaningful improvement in conversions.

---

## Alternative Hypothesis (H₁)

The Paid Conversion Rate of the Treatment group is greater than the Paid Conversion Rate of the Control group.

H₁: p(Treatment) > p(Control)

This means the new onboarding campaign improves paid user conversions.

---

## Type of Test

One-Tailed Test

A one-tailed test is appropriate because the business objective is specifically to determine whether the Treatment group performs better than the Control group. The company is interested in detecting improvement rather than any difference in either direction.

---

## Significance Level

α = 0.05

A significance level of 5% is used. If the p-value is less than 0.05, the null hypothesis will be rejected.

---

## Test Inputs

Control Group:

* Total Users = 693
* Paid Conversions = 22
* Conversion Rate = 3.17%

Treatment Group:

* Total Users = 715
* Paid Conversions = 50
* Conversion Rate = 6.99%

---

## Decision Rule

If p-value < 0.05:

* Reject H₀
* Conclude that the Treatment group significantly improves Paid Conversion Rate

If p-value ≥ 0.05:

* Fail to reject H₀
* Conclude that there is insufficient evidence to show improvement

---

## Interpretation Logic

The hypothesis test evaluates whether the observed increase in Paid Conversion Rate is statistically significant or could have occurred due to random variation.

A statistically significant result provides evidence that the new onboarding campaign is more effective than the existing onboarding experience.

However, the final business recommendation will not be based solely on conversion improvements. Guardrail metrics such as Refund Rate, Support Ticket Rate, Engagement Score, and Days to Convert will also be evaluated to ensure the Treatment experience does not introduce negative business impacts.

---

## Connection to Business Decision

The outcome of this hypothesis test directly supports the decision of whether to launch the new onboarding campaign to all users.




