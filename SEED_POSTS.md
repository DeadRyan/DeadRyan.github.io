# KROTAL — Seed Posts (ready to paste)

Copy each fenced block below into its matching GitHub Discussions category.
The title is on the first line; paste it into the "Title" field, then the body.

---

## 📣 Announcements

### Post 1 — Welcome to the KROTAL community

**Title:** Welcome to the KROTAL community

**Body:**

```markdown
// SYS.BOOT_OK · COMMUNITY ONLINE

Welcome aboard. This is the official community hub for **KROTAL — autonomous FX
trading systems**, engineered to pass FTMO prop-firm challenges and run live
capital.

## What KROTAL is

KROTAL deploys **self-operating trading agents** onto dedicated VPS
infrastructure. A central LLM decision engine — **CentCom** — ingests live market
data, produces ranked trade ideas with sized risk, and routes orders to your
broker 24/7. Every deployment enforces FTMO challenge rules at the protocol
level: max daily loss, max overall loss, weekend and news lockouts, and
trade-frequency throttles.

## The three ways to deploy

- 🎖️ **KROTAL Centurion (PKG_A)** — the full autonomous stack on a dedicated
  Contabo Windows VPS, FTMO 200K · 3-Step optimized.
- 🔁 **KROTAL Kopier (PKG_B)** — a trade copier that mirrors CentCom master
  signals to your own account. Proportional lot sizing, SL/TP and timing. No
  LLM keys required.
- 👥 **KROTAL Krowd (PKG_C)** — group crowdsourced trading. Pool resources with
  other traders, keep your own FTMO account. Up to 12 seats per pool.

## Billing

KROTAL is **crypto-native** — we accept **BTC, ETH, SOL and USDT (ERC20)**.
Subscriptions activate on first on-chain confirmation. No cards. No chargebacks.

## House rules

- Search before posting — your question may already be answered.
- Keep prop-firm and account specifics in mind; share results, not keys.
- Be respectful. No financial advice — KROTAL is a tool, deploy responsibly.

Read the docs, browse the categories, and when you're ready — pick a package at
[krotal.systems](https://krotal.systems).
```

---

### Post 2 — v3.7.2 · Release notes

**Title:** v3.7.2 · SYS.BOOT_OK — release notes

**Body:**

```markdown
// RELEASE_NOTES · v3.7.2 · CENTCOM ONLINE

Latest release is live. Highlights:

- ✅ Improved DD-guard responsiveness (server-side daily drawdown ceiling).
- ✅ Refined news blackout windows from the economic calendar feed.
- ✅ Faster kill-switch routing from the dashboard.
- ✅ Correlation filter tuned for XAUUSD + major FX overlaps.

Full changelog and upgrade notes in the docs. Existing deployments roll forward
automatically on the managed tier.
```

---

### Post 3 — How to read the CentCom live feed

**Title:** How to read the CentCom live feed

**Body:**

```markdown
// CENTCOM_LIVE_FEED · RFC

The live feed streams trade events and system telemetry. Here's how to read it.

## Trade lines

> EURUSD BUY 0.42 @ 1.07241 tp:1.07390 sl:1.07180

- **pair** / **direction** / **lots** / **entry** / **take-profit** / **stop-loss**

## Telemetry lines

> CENTCOM dd_used=1.42% cap=4.50% status=OK

- **dd_used** — drawdown currently consumed vs. your challenge cap.
- **status=OK** — within limits. Anything else is flagged.

> RISK guard=ARMED news_window=CLEAR
> CENTCOM heartbeat ok · node=01 · lat=24ms

- **guard=ARMED** — daily DD guard active.
- **news_window=CLEAR** — no economic blackout in effect.
- **lat** — node round-trip latency in ms.

If `status` ever leaves `OK` or `guard` drops to `DISARMED`, that's the kill-switch
or DD guard stepping in — check the Troubleshooting category.
```

---

## 🙏 General Support (Q&A)

### Post 4 — Centurion vs Kopier vs Krowd

**Title:** Which should I choose — Centurion, Kopier or Krowd?

**Body:**

```markdown
Quick decision guide:

- **Want the full autonomous system, hands-off?** → 🎖️ Centurion (PKG_A).
  Dedicated VPS, full stack, managed updates, FTMO 200K · 3-Step optimized.
- **Already have a system or prefer to mirror our master?** → 🔁 Kopier (PKG_B).
  Follows CentCom master signals with proportional lot sizing. No LLM keys.
- **Want to split the cost with others?** → 👥 Krowd (PKG_C).
  Share infrastructure, keep your own FTMO account, up to 12 seats per pool.

Still unsure? Drop your goal + budget below and the community will help you pick.
```

---

### Post 5 — What do I need before subscribing?

**Title:** What do I need before subscribing?

**Body:**

```markdown
Checklist before you subscribe:

1. An **FTMO account** (or a compatible clone) — KROTAL is tuned for the
   **200K · 3-Step** challenge.
2. A **crypto wallet** funded with BTC, ETH, SOL or USDT (ERC20).
3. A basic understanding of your prop firm's rules — KROTAL enforces them, but
   you should know them.

Subscriptions activate on first on-chain confirmation; provisioning starts once
funds confirm.
```

---

## 🎖️ Centurion · PKG_A

### Post 6 — Centurion onboarding checklist

**Title:** Centurion onboarding checklist

**Body:**

```markdown
After your subscription confirms on-chain:

1. Check your email/Telegram for the **VPS credentials**.
2. Log in to your dedicated Contabo Windows VPS.
3. Confirm the **KROTAL stack** is running (`SYS.BOOT_OK` in the feed).
4. Link your FTMO account to the routing bridge.
5. Verify the **DD-guard**, **news lock** and **kill-switch** are armed.

Provisioning is typically under 30 minutes after first confirmation.
```

---

### Post 7 — Understanding CentCom (the LLM engine)

**Title:** Understanding CentCom — the LLM decision engine

**Body:**

```markdown
CentCom is the central decision engine. It runs in four stages:

1. **INGEST** — market data streamed in.
2. **DECIDE** — produces ranked trade ideas with sized risk.
3. **EXECUTE** — routes orders to your broker via the VPS.
4. **GUARD** — DD-guard, news lock and kill-switch enforce challenge rules.

Every trade carries an audit log entry with the model's rationale. That's your
per-trade explanation — check it in the dashboard.
```

---

## 🔁 Kopier · PKG_B

### Post 8 — Setting up Kopier on MT4/MT5

**Title:** Setting up Kopier on MT4/MT5

**Body:**

```markdown
Kopier is plug-and-play:

1. Install Kopier on your MT4/MT5 terminal.
2. Point it at the **CentCom master** (credentials provided on deploy).
3. Set your **lot-scaling factor** (proportional to your account size).
4. Confirm SL/TP and timing replication is on.

No LLM keys or API setup needed — Kopier mirrors the master and scales
positions to your balance.
```

---

### Post 9 — Proportional lot sizing explained

**Title:** How proportional lot sizing works in Kopier

**Body:**

```markdown
Kopier scales the master's position size to your account. If the master opens
0.42 lots on a 200K account and your account is 50K, you trade at a 0.105 ratio.
SL/TP and entry timing copy 1:1 — only the lot size scales.

This keeps your risk proportional to your balance, not the master's.
```

---

## 👥 Krowd · PKG_C

### Post 10 — Starting or joining a KROTAL pool

**Title:** Starting or joining a KROTAL pool

**Body:**

```markdown
Krowd lets you pool resources with up to **12 traders**. Each member keeps their
own FTMO account and picks a Centurion or Kopier base.

To start a pool: pick the PKG_C package, set the seat count, and share your invite
link. Billing is **auto pro-rata** per seat.

To join: click a pool's invite link and confirm your seat in crypto.
```

---

### Post 11 — Pool admin controls and audit log

**Title:** Krowd pool admin controls + audit log

**Body:**

```markdown
Pool admins get:

- A shared **group dashboard**.
- An **audit log** of every trade and system event.
- Seat management (up to 12 per pool).
- Auto pro-rata billing per seat.

Each pool also has a private **Discord channel** for member coordination.
```

---

## 🧭 Challenge Strategy

### Post 12 — FTMO 3-step survival guide

**Title:** FTMO 3-step survival guide

**Body:**

```markdown
KROTAL is tuned for the **FTMO 200K · 3-Step** challenge. The core rules it
enforces:

- **Max daily loss** — hard ceiling, enforced server-side.
- **Max overall loss** — never breached by the DD-guard.
- **Weekend lockout** — no positions held into the weekend.
- **News blackout** — no entries during high-impact calendar windows.

Surviving the challenge is about *not* breaching these — KROTAL's guardrail is
the whole point. Let it run the protocol; don't fight the risk caps.
```

---

### Post 13 — Why the news blackout blocks trades

**Title:** Why the news blackout blocks trades

**Body:**

```markdown
High-impact news events (NFP, CPI, central-bank decisions) cause unpredictable
spreads and slippage. KROTAL reads the economic calendar and locks entries during
these windows.

If your dashboard shows `news_window=BLOCKED`, the guard is deliberately holding
positions. That's normal and by design — it protects your daily drawdown limit.
```

---

## ⚠️ Troubleshooting

### Post 14 — Kill-switch didn't trigger

**Title:** Kill-switch didn't trigger — what to check

**Body:**

```markdown
If the kill-switch didn't fire:

1. Confirm the switch is **ARMED** in the dashboard.
2. Check the **audit log** for the event that should have triggered it.
3. Verify your VPS and broker connection are healthy.
4. Report the timestamp + pair in this thread.
```

---

### Post 15 — Billing / on-chain activation not confirmed

**Title:** Billing — on-chain activation not confirmed

**Body:**

```markdown
Subscriptions activate on **first on-chain confirmation**. If it's stuck:

- Confirm the correct chain/wallet was used (BTC, ETH, SOL, USDT-ERC20).
- Check the transaction has enough confirmations.
- Share the tx hash (never your private key) in this thread.

We'll verify and provision once the payment is confirmed.
```

---

## 💡 Ideas & Feedback

### Post 16 — Feature request template

**Title:** Request a feature for the dashboard

**Body:**

```markdown
When requesting a feature, include:

- **What** you want.
- **Why** it helps your trading / challenge.
- **Where** it belongs (dashboard, feed, guard, billing).

Upvote 👍 the ideas you want the team to prioritise.
```
