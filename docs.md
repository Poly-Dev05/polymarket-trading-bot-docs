# Poly5M Bot — User Guide
# 🚀 Polymarket Telegram Bots

This guide is for **people who use the Poly5M Telegram bot** — how to trade, manage your wallet, change settings, and stay safe. If you run the bot yourself, see **README.md** for setup.
A complete suite of **Telegram trading bots for Polymarket**, supporting multiple advanced strategies with a **unified interface**, built-in wallet system, and both **paper** and **real trading** modes.

---

## What is Poly5M?
## 📌 Overview

**Poly5M** is a Telegram bot for **Polymarket 5-minute markets**. You can:
This repository provides automated trading bots designed primarily for **short-duration Polymarket markets** (e.g. 5-minute rounds).

- **Paper trade** — Run the strategy with fake money (no real orders).
- **Real trade** — Run the strategy with real USDC (requires your wallet key and a trial).
- **Wallet** — See your balance, get deposit addresses, and withdraw to other chains.
- **Referrals** — Share your link and earn (if enabled by the operator).
- **Settings** — Choose markets (BTC, ETH, SOL, XRP), set buy threshold, amount, and risk.
- **Help** — Tutorial, community, and docs links.

The bot trades **5-minute prediction markets** (e.g. “Will BTC be above $X in 5 minutes?”). Strategy: buy when the best ask is above a threshold, with optional risk exit near the end of the round. **Redeem** (cashing out winning positions) runs automatically after resolution when you have it enabled in Settings.
Each bot uses a different strategy, but all share the **same UI, commands, and features** inside Telegram.

---

## Getting started

1. Open the bot in Telegram (the operator will give you the bot link, e.g. `t.me/YourPoly5MBot`).
2. Send **`/start`**.
3. The bot replies with “Welcome to **Poly5M**. Choose an action:” and shows the **main menu**:
## 🧠 Available Bots & Strategies

   | 📈 Paper Trading | 💵 Real Trading |
   |------------------|-----------------|
   | 👛 Wallet        | 🎁 Referrals    |
   | ⚙️ Settings      | 📖 Help         |
- **Market Maker Bot**  
  Provides liquidity and profits from bid/ask spread

You can tap these buttons or type the same text. You can also use **commands** (see below).
- **HFT (High-Frequency Trading) Bot**  
  Executes rapid trades based on micro price movements

---
- **Arbitrage Bot**  
  Exploits price inefficiencies across markets

## Paper Trading
- **End-Cycle Bot**  
  Trades based on late-stage (end-of-round) behavior

- **What it does:** Runs one strategy cycle in **dry-run** — no real orders, no real money. You see live logs (e.g. best bid/ask) in the chat.
- **How to start:** Tap **📈 Paper Trading** or send **`/paper`**.
- **How to stop:** Tap **🛑 Stop** under the running message.
- **Requirements:** None. Your private key is not required for paper trading.
- **Momentum / Threshold Bot**  
  Buys based on price thresholds and trends

If you see *“A trading session is already running”*, stop the current run first. If you see *“Too many users are running Paper/Real right now”*, wait a few minutes and try again.
> ⚠️ Strategy differs per bot — everything else (wallet, UI, commands) is identical.

---

## Real Trading
## ✨ Core Features

- **What it does:** Runs the same strategy with **real USDC** — live orders on Polymarket.
- **Trial:** Real trading is limited to a **24-hour trial** per user. After that, you’ll see a message to upgrade (e.g. contact link). Use **`/upgrade`** for details. **Paper trading stays free.**
- **How to start:** Tap **💵 Real Trading** or send **`/real`**. You must have set your **private key** in **Settings** (see below); otherwise the bot cannot place real orders.
- **How to stop:** Tap **🛑 Stop** under the running message.

Before starting, the bot may check/approve tokens; then it streams logs like in Paper Trading. **Only use Real Trading with funds you can afford to lose.**
### 📈 Paper Trading
- Simulate trading with **no real funds**
- No private key required
- Real-time logs and signals
- Best way to test strategies safely

---

## Wallet
### 💵 Real Trading
- Trade with **real USDC**
- Requires wallet private key
- Includes **24-hour free trial**
- Upgrade required after trial

Tap **👛 Wallet** or send **`/wallet`**.
> ⚠️ Use only funds you can afford to lose.

You’ll see:
---

- **Deposit addresses** — Where to send funds so they arrive in your Polymarket wallet:
  - **Polygon** (min $3)
  - **Solana** (min $3)
  - **ETH/BNB** (min $10)
  - **BTC** (min $10), if supported
- **Polymarket address** — Your proxy/Safe address (don’t send directly here for deposits; use the deposit addresses above).
- **Balance** — Your USDC balance (as shown by the bot).
### 👛 Wallet System
- Multi-chain deposits:
  - Polygon (min $3)
  - Solana (min $3)
  - Ethereum / BNB (min $10)
  - BTC (if supported)

**Buttons:**
- Withdraw to:
  - Polygon, Solana, Ethereum, BNB, Base, Arbitrum

- **📤 Withdraw** — Withdraw from your Polymarket balance to another chain:
  1. Choose **chain** (Polyg
