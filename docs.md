Guide

This guide is for **people who use the Poly5M Telegram bot** — how to trade, manage your wallet, change settings, and stay safe. If you run the bot yourself, see **README.md** for setup.

---

## What is Poly5M?

**Poly5M** is a Telegram bot for **Polymarket 5-minute markets**. You can:

- **Paper trade** — Run the strategy with fake money (no real orders).
- **Real trade** — Run the strategy with real USDC (requires your wallet key and a trial).
- **Wallet** — See your balance, get deposit addresses, and withdraw to other chains.
- **Referrals** — Share your link and earn (if enabled by the operator).
- **Settings** — Choose markets (BTC, ETH, SOL, XRP), set buy threshold, amount, and risk.
- **Help** — Tutorial, community, and docs links.

The bot trades **5-minute prediction markets** (e.g. “Will BTC be above $X in 5 minutes?”). Strategy: buy when the best ask is above a threshold, with optional risk exit near the end of the round. **Redeem** (cashing out winning positions) runs automatically after resolution when you have it enabled in Settings.

---

## Getting started

1. Open the bot in Telegram (the operator will give you the bot link, e.g. `t.me/YourPoly5MBot`).
2. Send **`/start`**.
3. The bot replies with “Welcome to **Poly5M**. Choose an action:” and shows the **main menu**:

   | 📈 Paper Trading | 💵 Real Trading |
   |------------------|-----------------|
   | 👛 Wallet        | 🎁 Referrals    |
   | ⚙️ Settings      | 📖 Help         |

You can tap these buttons or type the same text. You can also use **commands** (see below).

---

## Paper Trading

- **What it does:** Runs one strategy cycle in **dry-run** — no real orders, no real money. You see live logs (e.g. best bid/ask) in the chat.
- **How to start:** Tap **📈 Paper Trading** or send **`/paper`**.
- **How to stop:** Tap **🛑 Stop** under the running message.
- **Requirements:** None. Your private key is not required for paper trading.

If you see *“A trading session is already running”*, stop the current run first. If you see *“Too many users are running Paper/Real right now”*, wait a few minutes and try again.

---

## Real Trading

- **What it does:** Runs the same strategy with **real USDC** — live orders on Polymarket.
- **Trial:** Real trading is limited to a **24-hour trial** per user. After that, you’ll see a message to upgrade (e.g. contact link). Use **`/upgrade`** for details. **Paper trading stays free.**
- **How to start:** Tap **💵 Real Trading** or send **`/real`**. You must have set your **private key** in **Settings** (see below); otherwise the bot cannot place real orders.
- **How to stop:** Tap **🛑 Stop** under the running message.

Before starting, the bot may check/approve tokens; then it streams logs like in Paper Trading. **Only use Real Trading with funds you can afford to lose.**

---

## Wallet

Tap **👛 Wallet** or send **`/wallet`**.

You’ll see:

- **Deposit addresses** — Where to send funds so they arrive in your Polymarket wallet:
  - **Polygon** (min $3)
  - **Solana** (min $3)
  - **ETH/BNB** (min $10)
  - **BTC** (min $10), if supported
- **Polymarket address** — Your proxy/Safe address (don’t send directly here for deposits; use the deposit addresses above).
- **Balance** — Your USDC balance (as shown by the bot).

**Buttons:**

- **📤 Withdraw** — Withdraw from your Polymarket balance to another chain:
  1. Choose **chain** (Polygon, Solana, Ethereum, BNB, Base, Arbitrum).
  2. Choose **token** (e.g. USDC, USDT, native gas token).
  3. Enter your **destination wallet address** (EVM: `0x` + 40 hex chars; Solana: 32–44 chars).
  4. Confirm. The bot sends your USDC.e from Polygon to the chosen chain/token. Withdrawals can be **gasless** if the operator enabled Builder API; otherwise you need POL for gas.
- **👤 Profile** — Opens your Polymarket profile in the browser.
- **📈 Portfolio** — (May show “not implemented yet” depending on version.)

---

## Referrals

Tap **🎁 Referrals** or send **`/referrals`**.

You’ll see your **referral code** and **invite link**. Buttons may include:

- **💸 Withdraw (Min $5)** — Withdraw referral earnings (if the operator wired this to a backend).
- **📋 Copy Link** — Copy your referral link.
- **🔄 Refresh** — Refresh the screen.

Minimum withdrawal for referral payouts is typically **$5 USDC**.

---

## Settings

Tap **⚙️ Settings** or send **`/settings`**.

Settings control **how** the bot trades (markets, entry, risk). Everything is **per user**.

### Buy Above (strategy)

- **Threshold** — Buy when best ask is above this (e.g. 0.95).
- **Amount ($)** — USDC amount per buy (e.g. 10).
- **Redeem Delay (s)** — Seconds to wait after market resolution before redeeming.
- **Risk Final (s)** — In the last N seconds of the round, risk rules apply.
- **Risk Drop** — If best ask drops by this much in the final seconds, the bot can sell and buy opposite.
- **Risk Opposite ($)** — USDC amount for the opposite side in that case.

Tap a row to **edit** that value; the bot will ask you to type the new value in chat.

### Risk Management

- **Stop Loss (%)** — Exit if the position drops by this percentage (e.g. 8).

### Markets

- **Assets** — Toggle **BTC**, **ETH**, **SOL**, **XRP** (✅ = enabled, ⬜ = off). Tap to toggle.
- **Intervals** — Usually **5m** only; tap to select.

### Wallet security

- **🔑 Export Private Key** — Shows a warning, then (if you confirm) displays your private key in chat. **Never share it.** Use this only if you need to import the same wallet elsewhere (e.g. Polymarket website). Delete the message after copying.
To get a copy of your config with secrets hidden, use **`/settings_export`** — the bot will send your YAML with private key and API secrets redacted.

---

## Help

Tap **📖 Help** or send **`/help`**.

You’ll see short text and links to:

- **📺 Tutorial Video**
- **👥 Community**
- **📄 Documentation**

Reminder: **Deposit only to your own wallet addresses. Never share your private key with anyone.** Legit admins won’t ask for your key or DM you first.

---

## Commands (quick list)

| Command | What it does |
|--------|----------------|
| `/start` | Start the bot and show the main menu |
| `/paper` | Start Paper Trading |
| `/real` | Start Real Trading |
| `/upgrade` | Show upgrade/premium contact (after trial ends) |
| `/wallet` | Open Wallet |
| `/referrals` | Open Referrals |
| `/settings` | Open Settings |
| `/help` | Open Help |
| `/settings_export` | Send your config file (secrets redacted) |

---

## Tips and safety

- **Paper first.** Use **Paper Trading** to see how the strategy behaves before using real funds.
- **Real trading needs your key.** To use **Real Trading**, you must add your Polymarket **private key** in **Settings** (or have it stored for your account). The same key controls the wallet shown in **Wallet**.
- **Trial is 24 hours.** After that, Real Trading is blocked until you upgrade; Paper stays available.
- **One session per user.** You can’t start a second Paper or Real run until you stop the current one.
- **Deposit minimums:** Polygon/Solana min $3; ETH/BNB/BTC min $10. Use the **deposit addresses** from Wallet, not the Polymarket proxy address, for deposits.
- **Withdrawals:** Confirm chain, token, and address before confirming. Withdrawals can be instant; mistakes can mean lost funds.
- **Never share your private key** with anyone. No legitimate support will ask for it or DM you first.

---

## What the strategy does (short)

- Subscribes to Polymarket 5m orderbooks (e.g. BTC, ETH, SOL, XRP).
- **Entry:** When best ask is above your **threshold**, the bot buys for your **amount** (in “buy above” mode).
- **Risk:** Near the end of the round (**Risk Final** seconds), if the ask **drops** by **Risk Drop**, it can sell and buy the opposite side for **Risk Opposite** amount. **Stop Loss %** can also close the position if it drops too much.
- **Redeem:** After the market resolves, the bot waits **Redeem Delay** seconds then redeems winning positions (gasless if the operator set up Builder API).

All of this is configurable in **Settings** and runs in one cycle when you start Paper or Real Trading; you stop it with **🛑 Stop**.

---

For **running and installing** the bot (operators), see **README.md** and the project’s setup instructions.
