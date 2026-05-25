---
title: Households
parent: English
nav_order: 12
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/hogares/)

# Households

A **household** is where a savr budget lives. The accounts, categories, transactions, recurring rules, reports — all of it sits inside a household. Up to five people can share access.

If you're the only person on the account, that's fine: you just have a household with one member. But if you've ever wanted a partner to see the grocery budget without bothering you, or two adults in the same family to record their own spending into one shared plan, this is what makes it work.

---

## The shape of it

| Thing | Where it lives | What that means |
|---|---|---|
| Accounts, categories, transactions, recurring, targets, reports, saved views, the budget itself | **The household** | Shared with every member. Edits by one are visible to everyone. |
| Plan & subscription, trial period | **The household** | The household pays for itself. Members don't get billed separately. |
| Your display name, email, password, MFA, trusted devices, active sessions | **Your user account** | Yours alone. Stays the same no matter which household you're in. |
| Theme, language, timezone, currency display preferences | **Your user account** | Personal. The household's data is rendered with your preferences. |

You can be a **member of multiple households** and switch between them. You can **own one household** at a time (the one whose subscription you pay for).

---

## Roles

Just two:

| Role | Can do |
|---|---|
| **Owner** | Everything: edit the budget, invite members, remove members, revoke pending invites, transfer ownership, delete the household. Pays the subscription. |
| **Member** | Edit the budget normally. Leave the household whenever they want. Cannot manage other members or billing. |

Exactly **one Owner** per household. The Owner can't leave — they have to either transfer ownership to another member or delete the household. Other members can come and go freely.

---

## Creating a household

If you've just signed up, you already have one — savr creates a household for you on your first sign-in, names it after you, and starts the 90-day trial. You're the Owner. You can rename it later.

If you're a user without any households (for example, you got removed from one and you don't own any), you'll see a welcome screen on sign-in with two options:

- **Create your household** — fresh 90-day trial, you're the Owner, you can invite up to four other people. Pick a name (e.g. "The Smiths' Budget"), confirm, done.
- **Wait for an invite** — if someone's planning to add you, the welcome screen tells you which email to expect the invitation at, and refreshes automatically when one arrives.

> **Heads up:** You can only **own** one household at a time. If you already own one and want to create a second, you'll need to either leave or delete the first. There's no limit on how many households you can be a **member** of, though.

---

## Inviting someone

Open **Profile → Households → [household name] → Invite a new member**.

1. Type the email address of the person you want to invite.
2. Click **Send invitation**.
3. savr emails them a link. The link is good for **7 days**.

The new pending invite shows up in the household's **Pending invitations** list. If they don't accept in time, the invite expires — just send a new one.

A few rules:

- **5-person cap.** Members + pending invites combined can't exceed 5. If you're full, you'll need to remove someone or revoke a pending invite before sending a new one.
- **One pending invite per email** at a time. You can't double-send.
- **Email-based, not username-based.** They don't need a savr account yet — the invite link guides them through sign-up if needed.

> **Worked example:** You're setting up a household with your partner. You create the household ("Casa Aguilar"), then click **Invite a new member**, type their email, and send. They get an email titled *"You're invited to Casa Aguilar."* They click the link, sign up for savr (or sign in if they already have an account), accept, and choose to switch to Casa Aguilar immediately. Now both of you see the same budget.

---

## Accepting an invite

When you click an invite link in your email, savr opens a preview page that shows:

- Which household you've been invited to
- Who invited you
- Which email address the invitation was sent to

If you're **not signed in**, you'll be prompted to sign in or create a savr account. You can use any email address — the one the invite was sent to is just a routing hint; your savr account can use a different email and that's fine.

If you're **signed in**, two buttons:

- **Accept invitation** — joins the household. You then choose **Switch to this household now** or **Stay where I am** (in which case the new household appears in your switcher and you can hop over later).
- **Maybe later** — closes the page without accepting. The invite stays valid for the rest of its 7-day window.

Expired or invalid links show a clean "this invitation can't be used" screen. Ask the inviter to send a fresh one.

---

## Switching households

If you're a member of more than one household, you'll see a **switcher** at the top of the navigation (web) or under the "…" overflow menu (mobile). Tap it for the list. Each entry shows:

- The household's name
- Your role (an **Owner** badge if you're the owner)
- The member count
- An **Active** badge on the one you're currently using

Tap any entry to switch. The budget, accounts, and activity refresh to show that household's data. Your profile, preferences, and security settings stay the same.

> **Common use:** a freelancer with a personal household and a "business" household for client expenses. They switch between them depending on whose money they're spending. Same login, two budgets, no cross-contamination.

---

## Managing members

Open **Profile → Households → [household name]** to see:

- The member list (with an Owner badge on whoever owns the household)
- Your pending invitations
- Forms to invite new people, transfer ownership, and (for owners) delete the household

### Remove a member (Owner only)

Click **Remove** next to the member you want to remove. Confirm. They lose access to this household's budget immediately.

Their savr account isn't affected — they keep their other households, their profile, their sessions, everything. Only this household disappears from their view.

The Owner can't remove themselves; for that, use Transfer ownership or Delete household below.

### Revoke a pending invite (Owner only)

In the **Pending invitations** list, click **Revoke** next to the invite. The token stops working immediately — if the invitee clicks the link after you revoke, they'll get the "this invitation can't be used" screen.

### Leave a household (Members)

Open the household's page, click **Leave household**, confirm. You lose access right away. The Owner gets the seat back to invite someone else if they want.

If you change your mind, the Owner can re-invite you.

### Transfer ownership (Owner only)

Open the household's page, scroll to **Transfer ownership**, pick a member from the dropdown, click **Transfer**. Confirm.

After the transfer:

- The new Owner inherits all owner powers (invite, remove, delete).
- You become a regular Member. You can still see and edit the budget; you just no longer manage membership or billing.

A member can only become Owner if they don't already own another household. If they do, they have to leave or delete that one first.

> **When this matters:** the person paying the subscription needs to be the Owner. If the bill needs to move from you to your partner, transfer ownership to them and then they can subscribe (or take over the active subscription, depending on your billing arrangement).

---

## Deleting a household

This is the destructive option. **It deletes everything in the household:** accounts, transactions, categories, recurring rules, reports, member access. It's irreversible.

Steps (Owner only):

1. Open **Profile → Households → [household name]**.
2. Scroll to **Delete household**.
3. Read the warning. Type the household's name to confirm.
4. Click **Delete permanently**.

A few preconditions:

- **No active subscription.** If the household is on a paid plan, cancel it from the billing portal first. savr refuses to delete a paying household to prevent surprise billing situations.
- **Owner only.** Members can't delete; they can only leave.

The other members of the household lose access immediately and won't be billed for anything.

---

## Delete household vs delete account

These are **different** operations:

| Action | What disappears | Where to find it |
|---|---|---|
| **Leave household** | Your access to this one household | Households page → Leave |
| **Delete household** | The household and everything in it. Your user account stays. | Households page → Delete (Owner only) |
| **Delete your savr account** | Your user account itself. You lose access to every household you're in. If you own a household, you have to transfer or delete it first. | Profile → Danger Zone → Delete my account |

---

## Households and billing

The subscription belongs to **the household**, not to you.

- A household has its own **90-day trial**.
- A household has its own **plan** (Monthly / Quarterly / Annual) and its own billing portal.
- The **Owner** pays for the household. Members don't get billed separately.
- If the Owner's subscription lapses or the trial ends without a plan, **the entire household goes read-only** until the Owner subscribes again. Members can't fix this — only the Owner has the billing controls.

A worked example:

> You and your partner share "Casa Aguilar" — you're the Owner. You also belong to "Mom & Dad" (your family household, where your mom is the Owner). You pay the Casa Aguilar subscription. Your mom pays Mom & Dad. When you switch to Mom & Dad, you see whatever plan your mom is on. When you switch back to Casa Aguilar, you see your own.
>
> If your mom forgets to renew Mom & Dad, that household goes read-only for everyone (you included) until she resolves it. Your Casa Aguilar subscription is unaffected.

See [Plans & Billing](../billing/) for the full subscription mechanics.

---

## Common scenarios

| Situation | How to handle it |
|---|---|
| **Sharing a budget with a partner** | One of you signs up first, creates the household, invites the other. Both edit the same budget. |
| **Personal + work budgets** | Create two households. Switch between them via the switcher. Each has its own subscription. |
| **Family budgeting with adult kids** | Parents create the family household and invite the kids. The kids can also have their own personal households if they want — no conflict. |
| **Bookkeeper managing client budgets** | Get invited into each client's household as a Member. Switch between them as you work. The client keeps Ownership and billing. |
| **Moving from solo to shared mid-budget** | Just invite the second person. They join the existing household with all its history. Nothing migrates or splits. |
| **Splitting after a shared budget no longer makes sense** | The Owner can transfer ownership to the other person if needed, or each person creates their own new household. The original household's data goes wherever the Owner takes it. |

---

## Tips

- **Pick a household name that's specific.** "Budget" works when you have one household; the moment you're in two, you'll want "Casa Aguilar" and "Aguilar Consulting" to tell them apart in the switcher.
- **Use Owner sparingly.** Most households only need one Owner. If you're in a couple, decide together who's the Owner; the other partner is a Member with full edit access. Same powers day-to-day, fewer "wait, who's responsible for billing?" moments.
- **The 5-member cap exists for a reason.** Households are designed for partners, families, and small bookkeeping setups — not for whole teams. If you're trying to budget across more than 5 people, you're probably looking for a different kind of tool.
- **Invitations are forwardable.** The link in the email contains a one-time token; anyone with the link can accept. Treat it like a password. Send it directly to the person, not in a public channel.
- **Keep your owned household healthy.** If you're an Owner, your subscription powers everyone in the household. Update your payment method when the card expires; renew before trial ends. Members can't rescue the household — only you can.
