# NovaPay Funnel Analysis

**Business question:** Where do NovaPay users drop off between signup and repeat usage, and which fix would recover the most users?

**Data:** Simulated dataset of 10,000 users modelled on a fintech onboarding flow.

**Tools:** SQL, Python, Power BI


## Key findings

1. **KYC is the biggest drop-off.** Android users from Paid Social complete KYC at only 42.7%, against roughly 70% for Android users from other channels, so the problem is specific to that segment and not Android in general.

2. **Older users stall before their first transaction.** Funded users aged 45+ make a first transaction at 69.4%, about 16 points below every other age band.

3. **Referral brings the best users.** Referral users fund their wallets more often (83.4%) and are far more likely to come back (65.5% repeat rate vs 48% to 52% for other channels).
