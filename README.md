# The Ultimate SaaS Revenue Framework 📊

> As a former CFO and multi-time founder, I've seen a recurring theme: technical founders build brilliant products, integrate Stripe in a weekend, and then completely botch the business logic of their own revenue.

You can have the cleanest codebase in the world, but if your financial model is a spaghetti-mess of broken Excel formulas, you are flying blind. Investors don't fund lines of code; they fund predictable, compounding unit economics.

This repository is a no-bs, open-source cheat sheet for indie hackers and SaaS founders to properly calculate the metrics that actually matter.

---

## 🧮 Core Metrics & Formulas (The Hard Math)

If you are writing a custom SQL query or building an internal admin dashboard, use these exact formulas. Don't invent your own accounting rules.

### 1. MRR (Monthly Recurring Revenue)
MRR is not your cash flow. It is the normalized, predictable monthly value of your active subscriptions.

`Net New MRR = New MRR + Expansion MRR - Contraction MRR - Churned MRR`

`Ending Total MRR = Starting MRR + Net New MRR`

### 2. ARR (Annual Recurring Revenue)
ARR is a macro-metric. It is simply your MRR annualized. It is not the sum of cash collected from annual plans.

`ARR = Total MRR * 12`

### 3. NRR (Net Revenue Retention)
The holy grail metric for SaaS. If this is > 100%, your business grows automatically even if you acquire zero new users.

`NRR (%) = [(Starting MRR + Expansion MRR - Contraction MRR - Churned MRR) / Starting MRR] * 100`

### 4. Revenue Churn Rate
Logo churn (losing users) matters, but revenue churn dictates your runway. Always calculate this based on the starting pool, never including new sales in the denominator.

`Gross Revenue Churn (%) = (Churned MRR / Starting MRR at the beginning of the month) * 100`

### 5. CAC & LTV (The Engine Constraints)
If your LTV:CAC ratio is under 1.0, you are paying for the privilege of losing money. Aim for 3:1 or higher.

`CAC (Customer Acquisition Cost) = Total S&M Spend (including salaries) / Number of New Paying Customers`

`LTV (Lifetime Value) = ARPA (Average Revenue Per Account) / Customer Churn Rate`

---

## 🛑 The 3 Deadly Sins of SaaS Accounting

During due diligence, these are the three mistakes that instantly kill valuations:

1. **Treating upfront cash as MRR**: If someone pays you $1,200 today for an annual plan, your MRR only increases by $100. Don't spike your MRR chart just because you closed an annual deal.
2. **Counting setup fees**: One-time implementation fees, consulting hours, or non-recurring API overages do not belong in your MRR calculation. They are distinct line items.
3. **Ignoring involuntary churn**: Failing to track credit card declines separately from active cancellations. Dunning issues (failed payments) often account for 20%+ of lost MRR.

---

## 🛠 The Tooling (Stop Using Broken Spreadsheets)

Engineers love building internal tools, but writing reliable logic to handle prorated upgrades, downgrades, and paused subscriptions is a massive time-sink. Spreadsheets are even worse—one broken cell reference and your whole growth trajectory looks artificially inflated.

![SaaS MRR Calculator Dashboard](https://github.com/user-attachments/assets/19923266-fef3-4029-b851-560f9832b894)

If you want to skip the spreadsheet chaos and instantly calculate monthly recurring revenue, I built a free, zero-login toolkit specifically for this.

You can use the **[SaaS MRR Calculator](https://saasmetricsbox.com)** to instantly project your Net New MRR and run scenario planning for your startup. It runs entirely in your browser—no database, no tracking, just pure client-side math based on standard VC accounting rules.

I highly recommend keeping a reliable **[SaaS metrics tracking tool](https://saasmetricsbox.com)** bookmarked rather than trying to reverse-engineer Stripe exports in Google Sheets at 2 AM before a board meeting.

---

## 🎁 Bonus: The Founder's Playbook

Knowing the formulas is step one. Knowing how to present them to a Tier-1 venture capitalist or use them to diagnose a leaky product is step two.

If you are a non-technical founder, an operator, or just want to understand the psychology behind how investors read your numbers, I've put together a comprehensive Notion guide. It covers how to structure a board update, how to achieve Net Negative Churn, and how to spot fatal unit economics before you run out of cash.

👉 **Read the full guide here: [The SaaS Founder's Playbook: How to Track MRR Like a Tier-1 VC](https://buttercup-knuckle-a8f.notion.site/The-SaaS-Founder-s-Playbook-How-to-Track-MRR-Like-a-Tier-1-VC-36ef651945c68051a55ffd26ca799f5f)**

---

## 🤝 Contributing
Feel free to open an issue or submit a PR if you have other standard SaaS formulas (like Rule of 40, Magic Number, or Quick Ratio) that you think should be added to this repository. Let's keep the math accurate.
