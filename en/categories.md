---
title: Categories
parent: English
nav_order: 5
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/categories/)

# Categories

Categories are the buckets you put your money in. Groceries. Rent. The Vacation Fund. The "I bought a fancy coffee setup, please don't judge me" fund.

Every Expense and Credit transaction lives in a category, and every category lives inside a category group. Picking the right level of detail is one of those quiet skills that turns a mediocre budget into a useful one.

---

## Why categories matter

Categories are the unit you assign money to on the Budget page, and the unit your spending gets summed against. Picking the right level of granularity is a balance:

- **Too few categories** → you can't see where money is actually going. "Misc: $1,247" is not insight.
- **Too many** → maintenance becomes a chore, you stop using vondo, you go back to wondering where your money went.

A solid starting point: one category per recurring bill (rent, utilities, phone), one for each major variable expense (groceries, transportation, dining), and a few for goals and quality of life. About 15–25 total. Adjust over time.

You can rename, reorder, hide, or delete categories at any time, so don't fret over getting the structure perfect upfront.

---

## Category templates

If you're starting fresh and want a head start, the [onboarding wizard](../getting-started/#the-onboarding-wizard) offers three pre-built templates:

- **Simple** — 8 categories across 8 groups. The minimum viable budget.
- **Standard** — 21 categories across 8 groups. Probably what you want.
- **Detailed** — 40 categories across 8 groups. For people who like granular tracking.

You can edit, rename, or delete anything the template creates. The template just saves you from staring at an empty Categories page on day one.

If you missed the wizard or want to start over, you can always create groups and categories manually.

---

## Category groups

Groups are how categories are organized visually. Examples:

- **Bills** — Rent, Utilities, Phone, Internet
- **Variable** — Groceries, Transportation, Dining Out
- **Goals** — Emergency Fund, Vacation, New Car
- **Quality of Life** — Entertainment, Subscriptions, Hobbies

Groups are purely organizational. They don't affect math. They just keep your Budget and Categories pages from looking like a long unsorted list.

### Create a group

1. Open **Categories**.
2. Click **New group**.
3. Type a name and save.

### Edit a group

Click the group name to rename it. You can also hide a group from the **edit** menu — see [Hiding](#hiding-categories-and-groups) below.

### Reorder groups

Drag a group's header up or down. The order applies everywhere groups are shown (Budget, Categories, transaction selectors).

### Delete a group

To delete a group, every category inside it has to be deleted or moved out first. vondo will warn you if a group still has categories in it.

---

## The Credit Card Payments group

There's one group vondo manages for you: the **Credit Card Payments** group (or **Pagos de tarjeta de crédito** in Spanish — the default name follows the language you're using when you add your first credit card).

It's created automatically the first time you add a credit-card account, and every CC payment category you ever create lives inside it. This is what powers vondo's [credit-card auto-flow](../accounts/#credit-cards): when you charge a budgeted expense to a card, vondo moves the matching amount into the card's payment category — which always lives in this group.

Because vondo depends on this group being a clean, predictable home for payment categories, it carries a few rules other groups don't:

| Rule | What it means |
|---|---|
| **One per household** | The group is created once. Adding a second, third, or fifth credit card reuses it — every card's payment category lands in the same place. |
| **Can't be deleted while CC accounts exist** | You'd orphan the linked payment categories. To delete the group, first delete every credit card on the household; once the group is empty you can delete it. (vondo will mint a fresh one if you add a CC later.) |
| **Can't add regular categories to it** | If you try to drop "Groceries" or "Vacation" into it from the Categories page, vondo refuses. The group is reserved for the auto-created payment categories. |
| **Can't move CC payment categories out** | The card's payment category has to stay in this group — moving it elsewhere would break the auto-flow that fills it. |
| **Renaming is allowed** | You can rename the group itself (e.g. from "Credit Card Payments" to "Pay Off My Cards"). The system identity is independent of the visible name, so the rules above still apply after a rename. |

You can rename or reorder the categories *inside* the group exactly as you would in any other group. Hiding a CC payment category is allowed but unusual — if you're not going to use a card anymore, [close the card](../accounts/#close-an-account) and the related categories naturally fade from active use.

> **Heads up:** CC payment categories don't appear in the **category picker on a transaction or recurring rule** — they're not a place you spend money directly. They show up where they should: as targets on the **Budget page** (so you can see and adjust their Available balance), and as the auto-flow destination when you charge spending to a card.

---

## Categories

### Create a category

1. Open **Categories**.
2. Pick the group it belongs in.
3. Click **New category** in that group.
4. Type the name and save.

> **Pro tip:** Category names support emoji. A leading 🛒 or 🏠 turns a long list into something you can scan at a glance. Use sparingly — emoji on every category is more chaotic than charming.

### Edit a category

Click any category name to rename it inline. Press Enter to save, Escape to cancel.

To move a category to a different group, drag it across to the destination group's section.

### Reorder categories

Drag categories within a group to change their order. The order persists across sessions and is reflected on the Budget page.

### Delete a category

If the category has no transactions, you can delete it directly.

If the category **has transactions**, vondo opens a **reassign** modal:

1. Pick another category to receive all the existing transactions.
2. Confirm.

vondo moves every transaction to the new category and then deletes the old one. Your history stays intact — no spending data is lost, it just moves homes.

> **Common scenario:** You have separate categories for "Coffee" and "Dining Out" and realize you don't actually want to track them separately. Delete "Coffee" and reassign its 47 transactions to "Dining Out." Done. The Coffee category is gone but the spending is preserved.

---

## Hiding categories and groups

Sometimes a category isn't relevant anymore (a one-time goal you finished, a service you canceled), but you want to keep its history. Hide it instead of deleting:

1. Open the category's actions and toggle **Hide**.

Hidden categories don't appear on the Budget page, in transaction selectors, or in Quick-fill strategies. The data is preserved. Show them again any time you want.

The same goes for entire groups.

This is the cleanest way to retire a category that's served its purpose without losing the history.

> **For example:** You ran a 6-month Wedding Fund and now you're married. Hide the category — the spending stays in your records, but it's not cluttering this month's Budget page.

---

## How spending and budgeting interact

A few things worth knowing about how categories behave:

- **Spending** in a category is the sum of Expense transactions less any Credit (refund) transactions for the selected month.
- **Assigned** is what you've allocated this month — independent of spending.
- **Available** = Assigned − Spent. When negative, the category is overspent.
- **Targets** can be set on any category to indicate what you want to budget. They power Quick-fill and the Fill by Targets shortcut. See [Budget → Targets](../budget/#targets-a-k-a-goals).

Hidden categories don't appear in the budget, but they still receive any transactions already assigned to them. To stop posting new transactions to a category, simply don't pick it when creating new ones — or delete it (with reassignment).

---

## Tips

- **Start broad.** Add detail later if you find yourself wanting to track something specific. A "Personal Care" category that aggregates haircuts, soap, and skincare is fine — until the day you actually want to know how much you spent on haircuts. Then you split it.
- **Use groups for hierarchy, not categories.** It's tempting to make sub-categories like "Dining Out → Lunch" and "Dining Out → Dinner." Don't. Use a single Dining Out category with notes on each transaction. Way easier to maintain.
- **One category per real-world commitment.** If you have a fixed monthly bill, give it its own category. A clean target on Rent works because rent is one thing. A target on "Bills" muddies it.
- **Hide before delete.** Hiding is reversible. Deletion (with reassignment) merges history into another category permanently. When in doubt, hide.
- **Review your category list every six months.** Some will feel obvious to remove. Others will feel obvious to add. Your spending changes — your categories should keep up.
