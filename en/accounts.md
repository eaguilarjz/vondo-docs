---
title: Accounts
parent: English
nav_order: 3
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/accounts/)

# Accounts

Accounts in savr mirror the real-world places your money lives: bank accounts, credit cards, the cash in your wallet, your investment portfolio, the loan that's slowly shrinking. Each transaction belongs to an account, and every account's balance updates the moment you record activity — so the totals you see in savr stay in sync with reality.

Set them up once. Maintain them with two minutes a week.

---

## Account types

savr supports six types. The type matters because it controls how the account is grouped on the page, how its balance is interpreted, and which features show up.

| Type | Use it for | Notes |
|---|---|---|
| **Checking** | Day-to-day spending | Where most transactions live |
| **Savings** | Money set aside | Treated like checking for budgeting purposes |
| **Credit Card** | Credit cards | Spending here doesn't reduce a cash account; record payments as Transfers. Optional **credit limit** field shown on the account detail page. |
| **Cash** | Physical cash on hand | Pocket money, that envelope in the drawer |
| **Investment** | Brokerage, retirement, crypto | Tracks the balance; not designed for trade-by-trade detail |
| **Loan** | Mortgages, auto loans, personal loans, student loans | Interest rate, monthly payment, linked payment category |

> Loans are special — see [Loan accounts](#loan-accounts) below for the full treatment.

---

## Add an account

1. Open **Accounts** and click **Add Account**.
2. Enter:
   - **Name** — how it shows up everywhere in savr (e.g. "Chase Checking")
   - **Type** — pick one of the six
   - **Opening balance** — what's in the account right now
3. For loans, fill in the loan-specific fields.
4. Click **Save**.

savr automatically creates an **Opening Balance** transaction equal to your starting amount. It marks this transaction specially: it sets the account balance but doesn't affect your budget or category spending.

> **For example:** You added a checking account with an opening balance of $2,847.13. savr creates a single transaction dated today, marked as Opening Balance, with that amount. Your account shows $2,847.13. Your budget is unaffected — that money just exists, ready to be allocated.

---

## Loan accounts

Loan accounts are where savr earns its keep. They give you a place to track the principal balance, the interest rate, and the payment so the math stays honest each month.

When creating or editing a loan, you can set:

| Field | Meaning |
|---|---|
| **Interest rate** | Annual percentage rate. Used in reports and recurring debt payments. |
| **Monthly payment** | The expected periodic payment — used as a default when you record payments. |
| **Linked payment category** | The category where loan interest and fees post when you record a payment. |

When you create a loan, you can either link to an **existing category** or have savr **create a new category** for it (and optionally place that category in a new group, like "Debt"). Either way, interest charges land in your budget like any other expense — visible, real, planned for.

For how to record loan payments with separate principal, interest, and fees amounts, see [Debt payments](../activity/#debt-payments). For monthly payments that fire on schedule, see [Recurring debt payments](../recurring/#recurring-debt-payments).

> **Pro tip:** When the loan is paid off, [close the account](#close-an-account) instead of deleting it. The history is part of your story — you'll want to look back and see the day that mortgage hit zero.

---

## Credit cards

Credit cards in savr work differently from most budgeting apps, and the difference is the whole point: **money sets itself aside to pay the card as you spend, so you're never surprised by the bill.**

This section explains exactly how that works.

### The payment category — savr's quiet superpower

When you create a credit-card account, savr automatically creates a **linked payment category** for it. By default it lives in a group called "Credit Card Payments" and is named `<your card's name> Payment` (e.g. "Chase Sapphire Payment"). You can override the group and name during account creation, or link to an existing category instead of making a new one.

That payment category is the trick. Whenever you charge a budgeted expense to the card, savr automatically moves that money into the payment category — so the funds to pay the card off are *already set aside* by the time the statement arrives.

### A worked example

You've budgeted **$500 to Groceries** for May. You also have a credit card with its linked **Chase Sapphire Payment** category.

May 5 — you buy groceries for **$80** on the card:

| Category | Before | After |
|---|---|---|
| Groceries (Spent) | $0 | $80 |
| Groceries (Available) | $500 | $420 |
| Chase Sapphire Payment (Available) | $0 | **$80** |
| Chase Sapphire (balance owed) | $0 | $80 |

May 28 — you pay the statement: a **$80 Transfer** from Checking → Chase Sapphire:

| Category | Before | After |
|---|---|---|
| Chase Sapphire Payment (Available) | $80 | **$0** |
| Chase Sapphire (balance owed) | $80 | $0 |
| Checking (balance) | … | dropped by $80 |

The payment category was filled automatically as you spent and drained as you paid. You never had to remember to budget "credit card payment" — it took care of itself.

### What happens when you overspend a category on a card

If you've budgeted $500 for Groceries and charge $600, **only the $500 that was actually budgeted moves into the payment category**. The remaining $100 stays as overspending on Groceries, which reduces next month's Ready to Assign — the same way overspending always works.

This keeps the math honest: the payment category only auto-funds money that was within your plan. Money you spent without budgeting for is something you have to actually deal with, not something the payment category quietly papers over.

### Refunds and credits

A **Credit** transaction on the card (a refund) reverses everything cleanly: the spending category's Spent goes down, the card balance goes down, and the payment category's Available goes down by the same amount. No matter the order of charges, refunds, and payments, the totals stay balanced.

### What if cash and card hit the same category?

savr walks transactions in chronological order and "covers" card spending only up to the point where the category's budget pool runs dry. If you've budgeted $200 for Groceries and spend $100 in cash on the 5th and then $150 on the card on the 10th, the first $100 of the card charge fits within what's left of the pool ($100) and flows to the payment category. The other $50 becomes overspending.

### Multi-card edge case

If you use *two* credit cards in the same category and one card's refund happens to bring net spending back inside the budget, the per-card payment-category amounts may not exactly match each card's actual debt — one card might end up "over-funded" in its payment category and the other "under-funded." The **total** is always right; only the per-card split can drift. If you want exact per-card matching, move money manually between the two payment categories.

### Recording payments

A credit-card payment is a [Transfer](../activity/#transfers) from your Checking (or wherever the money comes from) to the credit-card account. The card balance drops, your checking balance drops, your overall net worth doesn't change. **Don't enter the payment as an Expense on the credit card** — that would double-count.

For automated monthly payments, set up a [Recurring Transfer](../recurring/#create-a-recurring-transaction) so it fires the same day every month and the math takes care of itself forever.

### Credit limit (optional)

When you create or edit a credit-card account, you can set a **Credit Limit**. It's a reference value, not a hard cap — savr doesn't block transactions when you cross it — but the limit shows on the account detail page next to your current balance so you can see headroom at a glance.

Leave it blank if you don't want to bother. Add it later from the account editor whenever you decide to.

### Tips

- **Pay the statement balance every month.** The whole system assumes you do. The payment category will have exactly the right amount in it.
- **Treat the payment category as untouchable.** It's the money you've already committed to your card. Don't move it elsewhere unless you genuinely don't have a card balance to pay (which would be odd).
- **If you opened the account with an existing balance**, the opening-balance amount is debt that wasn't planned for in any budget month. It's not auto-covered. Manually assign money to the payment category to chip away at it.
- **When you close a credit card**, [close the account](#close-an-account) (don't delete). The payment-category history stays useful.

---

## Edit, close, reopen, delete

### Edit an account

Click the account row to open its editor. You can change:

- The name
- The type
- (For loans) the interest rate and monthly payment
- (For credit cards) the **credit limit** — see [Credit cards](#credit-cards) below

Opening balance is set at creation. To adjust historical balances, edit or add a transaction directly.

### Close an account

When you're done with an account but want to keep its history:

1. Open the account's detail view.
2. Click **Close**.

Closed accounts are hidden from the main accounts list and don't appear in transaction selectors, but every transaction stays put. This is the right move for paid-off credit cards, sold investments, and accounts at banks you no longer use.

### Reopen an account

In the closed accounts section of the Accounts page, click **Reopen**. Everything comes back exactly as you left it.

### Delete an account

You can permanently delete an account only if it has no transactions other than its opening balance. If you need to delete an account with activity, you've got two options:

1. Delete or reassign every transaction first, or
2. Close the account instead — closing preserves history.

Closing is almost always what you want. Deletion is for when you created an account by mistake.

---

## Reconciliation

Most accounts have a **Reconcile** button that walks you through matching savr to your bank's statement. This is the move that catches typos, missed transactions, and the occasional double-charge from your bank.

If your account balance in savr starts to drift from reality, run a reconciliation. It's the cleanest way to catch up.

> **Heads up:** Loan accounts don't have a Reconcile button. Lenders don't issue the kind of cleared/uncleared statement that the reconciliation flow assumes. For a loan, the right move is to keep the principal balance in sync via accurate [Debt Payment](../activity/#debt-payments) entries, and update the opening balance once a year if your lender's number drifts from yours.

→ Full guide: [Reconciliation](../reconcile/)

---

## CSV import

Got a year of transactions sitting in a CSV from your bank? Don't type them all in. savr has a three-step import wizard that handles the gnarly stuff (date formats, sign conventions, header mapping) for you.

→ Full guide: [Import & Export](../import-export/)

---

## Organizing the accounts page

### Grouping by type

Accounts are automatically grouped by type. Each group (Checking, Savings, Credit Card, etc.) has a header that shows the type's total balance — useful for "how much cash do I actually have right now?" at a glance.

### Collapse and expand

Click any group header to collapse it. Use this to focus on the accounts you're actively working with. The closed loans and the credit cards you barely touch don't need to clutter your view.

### Reorder accounts

savr supports drag-and-drop on two levels:

- **Within a group** — drag individual accounts to change their order
- **Across groups** — drag the group header to change the order of types

Your ordering saves automatically and persists across sessions.

> **For example:** You have three checking accounts and you always think of "Chase Checking" first. Drag it to the top of the Checking group. Now it's always first when you record a transaction.

---

## Account detail view

Click an account's name to open its detail page. You'll see:

- The current balance and account metadata (type, opening balance, created date)
- All transactions for this account, with the same filters as the main Transactions page
- A **New Transaction** button to record activity directly against this account
- A **Reconcile** button to match against a statement
- An **Import CSV** option to bulk-add transactions

This is the fastest way to reconcile against a paper or online statement, or to add a streak of transactions for one account in a row.

---

## Account balances explained

Balances are stored to two decimal places. Every time you create, update, or delete a transaction, the affected account's balance recalculates atomically — so the number on the Accounts page always matches the sum of its activity. No drift, no "let me close and reopen the app to refresh."

Transfers between two accounts post a paired entry: one debit, one credit. Both accounts update together.

For credit card accounts, the balance reflects what you owe. A positive balance means you have an outstanding amount to pay. When you record a payment, transfer money from a checking account to the credit card account — the credit card balance goes down, the checking balance goes down, and your overall net worth is unchanged.

> **Common scenario:** Your Chase Sapphire shows a balance of $843.21. You pay it off by transferring $843.21 from Checking. Now Sapphire shows $0 and Checking shows $843.21 less. The transfer is one savr action, two linked transactions, zero math on your end.
