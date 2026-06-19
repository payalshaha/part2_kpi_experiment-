
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




# Hypothesis Test Notes

## Objective

To determine whether the new onboarding and activation campaign (Treatment) significantly improves the **Paid Conversion Rate** compared to the existing onboarding experience (Control).

---

# Metric Being Tested

## Primary Metric

**Paid Conversion Rate**

[
\text{Paid Conversion Rate}=\frac{\text{Number of Paid Conversions}}{\text{Total Users}}\times100
]

This is the **North Star Metric** for the experiment because it directly measures the primary business objective of increasing paid subscriptions.

---

# Business Question

Does the new onboarding and activation campaign significantly increase the Paid Conversion Rate compared to the existing onboarding experience?

The answer to this question will determine whether the Treatment experience should be rolled out to all users.

---

# Hypotheses

## Null Hypothesis (H₀)

The Paid Conversion Rate of the Treatment group is **less than or equal to** the Paid Conversion Rate of the Control group.

[
H_0 : p_T \le p_C
]

This implies that the new onboarding campaign does **not** provide a statistically significant improvement in paid conversions.

---

## Alternative Hypothesis (H₁)

The Paid Conversion Rate of the Treatment group is **greater than** the Paid Conversion Rate of the Control group.

[
H_1 : p_T > p_C
]

This implies that the new onboarding campaign results in a statistically significant improvement in paid conversions.

---

# Type of Test

**One-Tailed Two-Proportion Z-Test**

A one-tailed hypothesis test is appropriate because the business objective is specifically to determine whether the Treatment performs **better** than the Control. The company is interested in detecting improvement rather than any difference in either direction.

---

# Significance Level

[
\alpha = 0.05
]

Decision Rule:

* If **p-value < 0.05**, reject the null hypothesis.
* Otherwise, fail to reject the null hypothesis.

---

# Experiment Data

| Metric           | Control | Treatment |
| ---------------- | ------- | --------- |
| Total Users      | 693     | 715       |
| Paid Conversions | 22      | 50        |
| Conversion Rate  | 3.17%   | 6.99%     |

---

# Statistical Test

## Step 1: Sample Proportions

Control Conversion Rate

[
p_C=\frac{22}{693}=0.0317
]

Treatment Conversion Rate

[
p_T=\frac{50}{715}=0.0699
]

Difference

[
p_T-p_C=0.0382
]

---

## Step 2: Pooled Proportion

[
p=\frac{22+50}{693+715}
=\frac{72}{1408}
=0.0511
]

---

## Step 3: Standard Error

[
SE=
\sqrt{
p(1-p)
\left(
\frac1{693}
+
\frac1{715}
\right)
}
]

[
SE \approx 0.0118
]

---

## Step 4: Z-Statistic

[
Z=
\frac{0.0699-0.0317}
{0.0118}
\approx3.24
]

---

## Step 5: P-Value

For a one-tailed test,

[
p\text{-value}\approx0.0006
]

---

# Statistical Decision

Since

[
0.0006 < 0.05
]

Reject the Null Hypothesis.

There is strong statistical evidence that the Treatment onboarding experience significantly improves the Paid Conversion Rate compared with the Control experience.

---

# Practical Interpretation

The Treatment group achieved a Paid Conversion Rate of **6.99%**, compared with **3.17%** for the Control group.

This represents:

* **3.82 percentage point absolute increase**
* **Approximately 120% relative improvement** in paid conversions

The probability that this improvement occurred due to random chance is extremely low (approximately 0.06%).

Therefore, the observed increase is both statistically and practically significant.

---

# Business Recommendation

Based on the hypothesis test results:

* The Treatment significantly improves Paid Conversion Rate.
* The primary business objective has been achieved.
* The onboarding campaign demonstrates a meaningful increase in paid subscriptions.

However, a full rollout should only be recommended after verifying that guardrail metrics remain within acceptable limits.

These include:

* Refund Rate
* Support Ticket Rate
* User Engagement Score
* Average Days to Convert
* Customer Satisfaction
* Revenue per User (if available)

If these guardrail metrics do not show significant negative impacts, the Treatment should be recommended for production rollout.

---

# Conclusion

The statistical analysis provides strong evidence that the new onboarding campaign increases Paid Conversion Rate.

Because the p-value (0.0006) is well below the significance level of 0.05, the null hypothesis is rejected.

The Treatment group demonstrates a meaningful and statistically significant improvement in paid conversions, supporting a recommendation to launch the new onboarding experience, subject to satisfactory performance on all guardrail metrics.

If the Treatment group demonstrates a statistically significant improvement in Paid Conversion Rate without creating unacceptable risks in guardrail metrics, the campaign may be recommended for launch.
