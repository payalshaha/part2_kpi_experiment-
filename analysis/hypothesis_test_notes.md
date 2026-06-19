# Hypothesis Test Notes

## Metric Being Tested

### Paid Conversion Rate

Formula:

Paid Conversion Rate = (Number of Users Converted to Paid / Total Users) × 100

This metric was selected because it is the North Star Metric of the experiment and directly measures the company's primary objective of increasing paid subscriptions.

---

## Business Question

Does the new onboarding and activation campaign significantly improve the Paid Conversion Rate compared to the existing onboarding experience?

The answer to this question will help determine whether the Treatment experience should be launched to all users.

---

## Null Hypothesis (H₀)

The Paid Conversion Rate of the Treatment group is less than or equal to the Paid Conversion Rate of the Control group.

H₀: p(Treatment) ≤ p(Control)

This implies that the new onboarding campaign does not generate a meaningful improvement in paid conversions.

---

## Alternative Hypothesis (H₁)

The Paid Conversion Rate of the Treatment group is greater than the Paid Conversion Rate of the Control group.

H₁: p(Treatment) > p(Control)

This implies that the new onboarding campaign increases paid user conversions.

---

## Type of Test

### One-Tailed Two-Proportion Z-Test

A one-tailed test was selected because the business objective is specifically to determine whether the Treatment group performs better than the Control group. The company is interested in detecting improvement rather than simply identifying any difference.

---

## Significance Level

α = 0.05

A significance level of 5% was used.

Decision Rule:

* If p-value < 0.05 → Reject H₀
* If p-value ≥ 0.05 → Fail to Reject H₀

---

## Test Inputs

| Group     | Total Users | Paid Conversions | Conversion Rate |
| --------- | ----------: | ---------------: | --------------: |
| Control   |         693 |               22 |           3.17% |
| Treatment |         715 |               50 |           6.99% |

---

## Test Output

### Pooled Conversion Rate

72 / 1408 = 5.11%

### Standard Error

0.0116

### Z Statistic

3.25

### P-Value

0.00058

---

## Statistical Decision

Since:

P-Value = 0.00058

and

α = 0.05

Therefore:

0.00058 < 0.05

The Null Hypothesis (H₀) is rejected.

---

## Business Interpretation

The Treatment group achieved a Paid Conversion Rate of 6.99%, compared to 3.17% for the Control group.

The observed improvement is statistically significant and is highly unlikely to be caused by random chance.

This result provides strong evidence that the new onboarding and activation campaign increases paid user conversions.

---

## Connection to Business Decision

The hypothesis test supports the conclusion that the Treatment experience performs significantly better than the existing onboarding process in terms of converting users into paying customers.

However, the final launch decision should not rely solely on conversion improvement. Additional guardrail metrics including Refund Rate, Support Ticket Rate, Engagement Score, Revenue Quality, and Days to Convert should also be reviewed to ensure the campaign does not introduce negative business impacts.

---

## Conclusion

Result: Reject H₀

The Treatment group demonstrates a statistically significant improvement in Paid Conversion Rate.

The experiment provides strong evidence that the new onboarding campaign improves user conversion performance and should be considered for launch, subject to guardrail metric evaluation.
