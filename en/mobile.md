---
title: Mobile App
parent: English
nav_order: 13
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/movil/)

# Mobile App

vondo ships on iOS and Android as a native cross-platform app. Same account, same data, same budget — just optimized for a phone in your pocket while you're standing in line at the grocery store deciding whether the $7 bag of granola is "Groceries" or "Dining Out."

This page covers everything that's specific to the mobile app: how it's organized, how it stays in sync with the web app, and the small handful of things the mobile app doesn't do (yet).

---

## Install

Search for **Vondo** in the App Store (iOS) or Play Store (Android), install, and sign in with the same account you use on the web. Everything you've already set up — accounts, categories, budgets, recurring rules, saved views, the lot — appears on the phone immediately.

If you haven't signed up yet, you can also create your account from the mobile sign-in screen. See [Getting Started → Create your account](../getting-started/#create-your-account-and-start-your-free-trial) for the flow (the steps are the same on mobile).

---

## Tabs

The bottom of the screen has five tabs:

| Tab | What's there |
|---|---|
| **Home** | A digest of the current month — Ready to Assign at the top, overspent categories that need your attention, recent activity. |
| **Budget** | The full budget for the current month: groups, categories, Assigned / Spent / Available per category. Tap a category for the detail sheet (assign money, set a target, see history). |
| **Transactions** | Every transaction across every account, with filter pills and search. (The web calls this tab **Activity**.) |
| **Accounts** | All your accounts grouped by type. Tap one to see its detail screen with transactions and the reconcile button. |
| **Reports** | The same five reports as the web — Income vs Expenses, Net Savings, Net Worth, Expenses by Category, Top Payees. |

Adding something is always one tap away: a green **+** button sits at the top-right of the main screens. It creates the obvious thing for where you are — a transaction on Home or Transactions, a category on Budget, an account on Accounts.

### The "…" overflow menu

Things that don't live in a tab — Categories, Payees, Recurring, Profile, Households, Security, Plan & Billing, Active Sessions, Pending Changes — open from an overflow **…** button on the Home, Budget, and Transactions screens. Tap it and you get a sheet with all the secondary destinations grouped by topic. **Undo** and **Redo** live at the top of this menu too.

We took this approach because the bottom tab bar gets crowded fast, and Apple's HIG advises keeping it at five or fewer. The result: the five things you do every day are one tap away; everything else is two taps away.

### Household switcher

If you're a member of more than one [household](../households/), the overflow menu also surfaces a **household switcher**. Tap it and you get a sheet listing each household you belong to, with your role badge, member count, and an **Active** marker next to the one you're currently using. Tap any entry to switch — the budget, accounts, and activity reload to show that household's data. Your sign-in, theme, and language preferences stay the same.

---

## Offline-first: how mobile stays usable on a bad connection

The single biggest difference from the web is that **the mobile app keeps working when your connection drops**. You can record transactions, assign money, move money between categories, and edit just about anything while you're on the subway, on a plane, or in the back of that one café with terrible Wi-Fi.

### What happens when you're offline

1. **The app shows a banner at the top** — *You're offline — changes will sync when you reconnect*.
2. **Reads come from local storage.** Your accounts, categories, budget, and recent activity are cached on the device, so the app loads instantly even with no signal.
3. **Writes go into a queue.** When you create a transaction, edit a category, or move money, the change applies locally right away — you see the new numbers immediately — and gets added to a **pending writes** queue.
4. **When you reconnect**, the queue replays automatically. No button to press. The banner disappears once everything is in sync.

> **Worked example — a flight from SFO to JFK:**
>
> 1. You take off. The phone flips to airplane mode. vondo's offline banner appears at the top.
> 2. Mid-flight, you remember you owe your roommate $40 for utilities. You record it as a Transfer from your Checking to "Roommate IOUs" — it shows up in your Activity right away, and **Pending Changes** ticks to "1 unsynced change."
> 3. Boarding the connecting flight, you grab a sandwich and a coffee. Two more transactions go in. Now "3 unsynced changes."
> 4. You land at JFK and turn off airplane mode. Within a few seconds the offline banner disappears, the Pending Changes count drops to zero, and all three transactions are now on the server. Open the web app in the cab and they're already there.
>
> You did nothing special. No "sync now" button to press, no retries, no rerunning anything. The app just caught up.

### The Pending Changes screen

Open **… → Pending Changes** to see exactly what's queued up. Each row shows:

- A description of the change ("Add transaction at Whole Foods", "Edit Rent category", etc.)
- Its current state — **Waiting to sync**, **Sending…**, or **Failed**
- A timestamp

If a change fails (typically because the server rejects it — e.g. you edited a category on web that you'd already deleted on phone), you'll see a **Retry** or **Discard** button on the failed row. Retry sends it again; Discard drops the change and removes it from the queue.

> **Heads up:** If a write fails repeatedly, that's a sign the local copy has diverged from the server. The safest fix is to discard the failed write, pull-to-refresh on the affected screen to get a fresh copy from the server, and re-do the change with the updated data in front of you.

---

## Sign-in and security on mobile

The mobile app uses the same authentication system as the web: email + password (including sign-up, with the same 6-digit email verification), Continue with Google, Continue with Microsoft, and Continue with Apple. After sign-in, the same [two-factor authentication](../security/#two-factor-authentication-mfa) and [trusted-device](../security/#trusted-devices) flow apply.

A couple of mobile-specific notes:

- **Apple sign-in works on Android too.** On iPhone it uses the native Apple sheet; on Android it opens a quick in-app browser to Apple's sign-in page and drops you back in the app when you're done. Either way you land on the same account.
- **Logout wipes local data.** Signing out on a phone clears the device's local cache, the pending-writes queue, and the sync cursor — so the next person to sign in (you or someone else) starts clean. The web sign-out only clears tokens; mobile sign-out clears tokens *and* the on-device database.
- **Active sessions show your phones.** Your mobile devices appear in **Security → Active sessions** alongside web browsers. Revoke a phone session from the web if a device is lost.

## When the trial ends (or the subscription lapses)

If your trial ends or the subscription lapses without an active plan, the household goes **read-only** — all your data is still there and you can browse it freely, but you can't make changes until someone subscribes.

Rather than a blocking screen, the app shows a **read-only banner** pinned at the top:

- **If you're the Owner,** tap the banner to open the in-app **paywall**, pick a plan, and pay through the **App Store / Google Play** (see [Plans & Billing → Subscribe](../billing/#subscribe)). You can also reach it from **Profile → Subscribe**. Already subscribed on this store? Tap **Restore Purchases** on the paywall.
- **If you're a member** (not the Owner), the banner tells you to ask the household's Owner to resubscribe — only the Owner has billing controls.

Your data is completely safe. Once a plan is active, the banner clears and full editing returns — nothing to re-import or set up again.

---

## What's the same

Nearly everything. To save you reading the rest of the help pages a second time, here's what works identically:

- The four transaction types (Income, Expense, Transfer, Credit) plus Debt Payment, with splits
- All six [Quick-fill strategies](../budget/#quick-fill-strategies)
- [Recent Moves](../budget/#recent-moves) modal
- [Move Money](../budget/#moving-money-between-categories) between categories
- All four [target types](../budget/#targets-a-k-a-goals) (Monthly, Weekly, Yearly, Custom) with rollover
- All five [recurring frequencies](../recurring/#frequencies), the apply-due preview modal, and recurring debt payments
- All six [account types](../accounts/#account-types) including credit cards with optional credit limit and the linked payment category that auto-funds as you spend
- [Reconciliation](../reconcile/)
- [Reports](../reports/) — all five charts (Income vs Expenses, Net Savings, Net Worth, Expenses by Category, Top Payees) with the same time-range presets, account, and category filters as web
- Undo / Redo (from the **…** overflow menu — the first two rows)
- All your [saved views](../activity/#saved-views), filters, and the search box
- **System / Light / Dark theme** and language

### Mobile niceties

A handful of small flourishes that mobile gets in addition to parity:

- **Inline create on the transaction form.** When you're entering a transaction and need a category or payee that doesn't exist yet, type a name that doesn't match anything and a **"Create *<name>*"** option appears at the bottom of the suggestions. Tap it and the entity is created in place — no need to leave the form, go to the Categories or Payees screen, and come back.
- **Inline create on the recurring form too.** Same affordance when you're setting up a recurring bill.
- **Pull-to-refresh** on any list screen forces a fresh sync from the server.

---

## What's web-only (for now)

A few things live on the web app only. None are blockers for day-to-day use; they're either edge-case admin tasks or workflows that need a bigger screen:

- **CSV import.** Importing a year of bank transactions from a CSV is a desktop task — file pickers and column mapping work much better on a laptop. Use the web's [Import & Export](../import-export/) page.
- **Power-user search tokens.** Mobile search supports the search box and filter pills, but the `category:Food`, `>100`, `since:YYYY-MM-DD` shorthand syntax is web-only.
- **Drag-to-reorder categories.** On mobile, you reorder categories from the edit screen with up/down controls. Web has true drag-and-drop.
- **Onboarding wizard.** Web has the full setup wizard; mobile shows a brief welcome screen and assumes you'll do initial setup from a laptop.

---

## Push notifications, biometric unlock, background sync

Not in this version:

- **No push notifications.** The mobile app doesn't ping you about anything — no daily summaries, no reminders, no balance alerts. We may add some opt-in ones later.
- **No FaceID / TouchID unlock.** Sign-in is the standard email/password (or OAuth) flow plus MFA. The trusted-device cookie keeps you signed in for 30 days, so in practice you rarely re-authenticate.
- **No background sync.** The queue syncs when the app is open and connected (immediately on reconnect, and on screen focus). Closing the app doesn't drain pending changes — they wait for the next time you open it.

---

## Tips

- **Use the phone for capture, the laptop for setup.** Most people end up using the mobile app to record transactions throughout the day and the web app on Sunday nights for the monthly review.
- **Pull to refresh on any list screen.** If you think the server has newer data, swipe down — vondo fetches a fresh snapshot and reconciles it with whatever's in your pending queue.
- **Don't worry about the offline banner.** It's not an error; it's a status. The app keeps working. Your changes are safe locally and will sync when you're back online.
- **Sign out before lending a device.** If someone borrows your phone for a flight, sign out first. Signing back in is fast (one tap with a Google, Microsoft, or Apple account, or your password + an MFA code if you've set that up).
