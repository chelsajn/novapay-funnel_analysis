# NovaPay Funnel Analysis

**Business question:** Where do NovaPay users drop off between signup and repeat usage, and which fix would recover the most users?

**Data:** Simulated dataset of 10,000 users modelled on a fintech onboarding flow.

**Tools:** SQL, Python, Power BI


## Key findings

1. **KYC is the biggest drop-off.** Android users from Paid Social complete KYC at only 42.7%, against roughly 70% for Android users from other channels, so the problem is specific to that segment and not Android in general.

2. **Older users stall before their first transaction.** Funded users aged 45+ make a first transaction at 69.4%, about 16 points below every other age band.

3. **Referral brings the best users.** Referral users fund their wallets more often (83.4%) and are far more likely to come back (65.5% repeat rate vs 48% to 52% for other channels).

## Recommendations

1. **Fix the KYC flow for Android users from Paid Social (priority 1).** This segment completes KYC at 42.7% against about 70% for other Android users. Closing the gap would add about **563 verified users** and **348 first transactions**, an **8.2% uplift** in first-transaction volume. Next step: review the Android KYC journey for this campaign (document upload, camera permissions, landing page handoff) and A/B test a simplified flow, tracking KYC completion rate as the success metric.

2. **Add an activation nudge for funded users aged 45+ (priority 2).** They make a first transaction at 69.4% against about 85% for other age bands. Closing the gap would add about **83 first transactions** (**2.0% uplift**). Next step: test a guided first-payment prompt or a small first-transaction incentive for this group, tracking funded to first transaction rate.

3. **Shift acquisition spend toward Referral (to validate).** Referral users fund more often (83.4%) and repeat more (65.5% vs 48% to 52%). Next step: test a referral incentive increase and compare cost per repeat user against Paid Social.

Impact estimates assume each segment can reach the benchmark rate of its comparison group, so they are best-case figures. The two fixes overlap slightly, so the combined uplift is a little under 10%.

## Method

1. **Data validation:** checked for duplicate users, nulls, duplicate events, events out of order, and users reaching a stage without completing the previous one. All checks returned zero issues.
2. **Segmentation:** compared conversion by device, channel, city and age band using SQL.
3. **Significance testing:** chi-square tests confirmed all three gaps are statistically significant (p < 0.001).
4. **Impact sizing:** estimated extra first transactions from closing each gap.
