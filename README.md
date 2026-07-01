# Hotel Bookings Analysis — Cancellations, Revenue & Channel Performance
------------------------------------------------------------------------
Exploratory analysis of 30,000 hotel bookings across 10 US cities (Apr 2024 – Apr 2025),
focused on answering a real business question: where is the platform losing bookings, and what should it do about it?

# Business Questions
--------------------
1) Where in the booking funnel is the most value being lost (cancellations)?
2) Which booking channel × room type combinations are the riskiest?
3) Is the coupon program actually growing booking value, or just discounting sales that would have happened anyway?
4) What should the business prioritize first?

# Key Findings
--------------
1) 20.2% of bookings cancel and 7.5% fail outright — over a quarter of demand never converts.
2) Travel Agent + Standard room bookings cancel at 31%, nearly 2.4x the safest combination (Web + Deluxe, 13%)
   — found by cross-tabulating channel and room type rather than looking at either alone.
3) Web is the best-performing channel on every dimension: highest booking value, highest profit, lowest cancellation rate.
4) Coupon usage is associated with statistically significantly lower booking value (p = 0.007, two-sample t-test), not higher
   — suggesting the coupon program mostly discounts demand that would have converted anyway.
5) February–March is peak demand, May is the seasonal trough — a ~20% swing in average booking value.
6) City and payment method were tested and ruled out as meaningful drivers of cancellation or revenue.

# Recommendations
-----------------
1) Apply a stricter cancellation policy specifically to Travel Agent + Standard room bookings rather than a blanket policy.
2) Shift acquisition spend toward the Web channel.
3) Audit the coupon program's ROI; test targeting it only at high-cancellation segments.
4) Front-load promotions ahead of the May demand dip instead of discounting during already-strong Feb/Mar demand.

# Tools
-------
· pandas · numpy · matplotlib · seaborn · scipy.stats

# Approach
----------
1) Data quality check — traced missing check-in/check-out dates to cancelled/failed bookings rather than treating them as errors requiring imputation.
2) Univariate and bivariate EDA on cancellation, revenue, and profit.
3) Cross-segment analysis (channel × room type) to find the highest-risk combination, not just single-variable effects.
4) Two-sample t-test to confirm the coupon effect was statistically significant rather than incidental.
5) Correlation analysis on pricing fields to validate internal data consistency.

# Files
-------
Source Dataset -- [Hotel_bookings_final.xlsx](https://github.com/user-attachments/files/29560114/Hotel_bookings_final.xlsx)



























