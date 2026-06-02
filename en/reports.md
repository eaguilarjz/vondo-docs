---
title: Reports
parent: English
nav_order: 8
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/reports/)

# Reports

The Reports page is where the budget stops being a chore and starts being interesting.

It's five charts, refreshed live as you record transactions, that answer the questions you've been quietly wondering for years:

- "Am I actually saving more than I spend?"
- "Where does most of my money go each month?"
- "Who am I giving the most money to?"
- "Are things getting better or worse?"
- "How much am I actually worth?"

Open **Reports** from the navigation. Pick a time range (This month, 3 months, 6 months, 12 months, or This year), optionally narrow the data with the Account and Category filters, and the five charts refresh together.

---

## What you'll see

| Report | Type | What it shows |
|---|---|---|
| **Income vs. Expenses** | Grouped bar chart | Each period's income (green) and expenses (red) side by side |
| **Net Savings** | Line chart | Income minus expenses for each period — the line you want to see going up |
| **Net Worth** | Line / area chart | Assets, Debts, and the resulting Net Worth across the selected range. Ignores the Account and Category filters (it's always whole-portfolio). |
| **Expenses by Category** | Donut chart | Top spending categories for the range, with everything else rolled into "Other ({{count}})" |
| **Top Payees** | Horizontal bar chart | Where your money actually went, ranked |

All five play well with light and dark mode, and stack vertically on mobile so you can read them on a phone.

Every chart that lists categories or payees has a **View transactions** action — click it and you land on the Activity page pre-filtered to that slice. Great for the "wait, *that* much at Amazon??" moment when you want to actually see the underlying receipts.

---

## Income vs. Expenses

This is the bird's-eye view. Each period in the selected range gets a pair of bars:

- **Income** (green) — total inflows
- **Expenses** (red) — total outflows

When green is taller than red, you saved money in that period. When red is taller, you spent more than you earned. Over time, the pattern tells a story.

> **What to look for:**
> - Two periods in a row where red is taller than green? Check what changed and address it. (One is noise. Two is a trend.)
> - One period where expenses spiked? Probably a known thing — taxes, a big trip, holidays. Use it as a reminder to budget for the next time.
> - The "is my income consistent?" question gets answered visually here. If you're a freelancer, this chart is gold.

X-axis labels show "Month Year" — the year is omitted for the current year, just to reduce clutter. Hover any bar for the exact amount.

---

## Net Savings

Same data as the bar chart, but presented as a single line: **net savings each period** (income − expenses).

Above zero = you saved. Below zero = you spent more than you earned. The trend matters more than any single point.

This chart is the cleanest way to answer "am I building up over time?" A handful of bars together can look noisy. The line cuts through it.

> **For example:** If your net savings line wanders between +$200 and -$150 month to month, you're roughly breaking even, with normal variance. If the line is consistently above zero and trending up, you're building. If it's consistently below zero, you're sliding — time to plan an intervention. The chart doesn't moralize; it just shows you the shape.

---

## Net Worth

The newest chart, and arguably the most important. Three lines across the selected range:

- **Assets** — sum of balances across all your Checking, Savings, Cash, and Investment accounts
- **Debts** — sum of what you owe across all your Credit Card and Loan accounts (shown as a positive number for readability)
- **Net Worth** — Assets minus Debts

Net Worth is the line you actually want to see going up. Income vs. Expenses tells you about the month; Net Worth tells you about the trajectory of your financial life.

> **What to look for:**
> - **The Net Worth line going up steadily** even when individual months are noisy. That's the goal.
> - **Debts coming down faster than assets are growing.** Paying off a loan moves Net Worth up the same as saving an equivalent amount; this chart shows both at once.
> - **A big one-time event** (paid off a car, bought a house, got a tax refund) shows as a step change. Useful for seeing what those events actually meant in context.

> **Heads up:** Net Worth always shows your whole portfolio. The **Account** and **Category** filters apply to the other four charts but **don't change Net Worth** — a filtered view of net worth doesn't really mean anything, so vondo just shows the full picture.

---

## Expenses by Category

A donut chart of where your money went over the selected range, broken down by category.

The top categories get their own slices. Everything else collapses into an "**Other**" bucket whose label shows the count — e.g. "Other (12)" means there are 12 additional small categories merged into that slice. Click "Other" or any individual slice and you get a **View transactions** action that drills into the Activity page with the matching filter applied.

Hover any slice for the exact amount and percentage. The legend on the side lists each one.

Splits are correctly attributed: a $87 grocery run that's split $54/$33 between Groceries and Household shows up as $54 in one slice and $33 in another. Transfers don't appear (they're not expenses). Opening balance transactions are excluded.

> **What to look for:**
> - Is the biggest slice what you'd expect? If "Subscriptions" is bigger than "Groceries," that's worth a second look.
> - Are there slices you don't recognize? "Other" growing past 5% is a sign you've got transactions that need a real category. Click into it to see what's piling up.
> - Compare to a longer range using the range selector. The shape of the donut should be roughly stable. Big shifts have a story.

---

## Top Payees

A horizontal bar chart ranking the payees you spent the most with over the selected range.

This is the chart that produces those "wait, *that* much at Amazon??" moments. It's a useful reality check. Click any bar and **View transactions** drops you into the Activity page filtered to that payee — instantly visible receipt-by-receipt.

Income transactions are excluded — this is about where your money went, not where it came from.

> **For example:** Whole Foods is your #1 payee at $487. Trader Joe's is #4 at $108. Total grocery spending across both is $595, which is $95 over your $500 grocery budget. The chart didn't budget for you, but it did show you the truth — fast. Click Whole Foods → View transactions and you can see exactly which receipts added up to that $487.

---

## Time range and filters

Three controls at the top of the Reports page shape what every chart shows:

### Time range

| Preset | What it covers |
|---|---|
| **This month** | The current calendar month from the 1st to today. |
| **3 months** | The last three complete months plus the current one. |
| **6 months** | The last six complete months plus the current one. |
| **12 months** | A rolling year of data. The default. |
| **This year** | January 1 of the current year through today. |

Pick a longer range when you want to see trends; pick "This month" when you want to see what's happening right now.

### Account filter

A multi-select chip — pick one account, several, or leave it on **All accounts** for the default. Useful when you want to see, say, just the activity on a single business credit card without the rest of your finances in the picture.

### Category filter

Same idea, for categories. Especially handy on the Top Payees chart: filter to "Restaurants" and the chart instantly becomes a ranking of which restaurants ate the most of your dining budget.

> **Heads up — Net Worth ignores both filters.** Account and Category filters narrow Income vs. Expenses, Net Savings, Expenses by Category, and Top Payees. They don't touch Net Worth, which always reflects your whole portfolio. (A filtered Net Worth would be misleading.) When a filter is active, the Net Worth chart shows a brief note reminding you.

### Drilling into the numbers

The Expenses by Category donut and the Top Payees bar chart both have a **View transactions** action on every slice/row. It opens the Activity page with the corresponding filter already applied — same time range, same account selection, plus the category or payee you clicked. Useful for "I want to see the actual receipts behind this number" moments.

---

## Reports vs. Budget

Quick distinction:

| Page | Question it answers |
|---|---|
| **Budget** | "Where am I going to spend my money this month?" — forward-looking |
| **Reports** | "Where did I actually spend my money?" — backward-looking |

You'll use Budget more often (probably daily). You'll use Reports less often but get more from it (probably weekly or monthly). They feed each other: this month's reports inform next month's budget targets.

---

## Tips

- **Don't open Reports during the first few days of a new month.** A two-day-old month is a sample of two days. Wait a week before drawing conclusions.
- **The "trend" line is more useful than any single month's number.** Variance is normal. Direction is meaningful.
- **Use the donut to clean up your categories.** If one slice is "Misc" with 30% of your spending, your category structure isn't doing its job. Add real categories and reassign.
- **Take a screenshot at the end of each month.** It's surprisingly motivating to look back at six months of these charts and see your trend line going up.
- **Don't moralize.** Reports show you what is, not what should be. Use them as data, not judgment.
