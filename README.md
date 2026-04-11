# 🚀 Polymarket Telegram Bots

A complete suite of **Telegram trading bots for Polymarket**, supporting multiple advanced strategies with a **unified interface**, built-in wallet system, and both **paper** and **real trading** modes.

---

## 📌 Overview

This repository provides automated trading bots designed primarily for **short-duration Polymarket markets** (e.g. 5-minute rounds).

Each bot uses a different strategy, but all share the **same UI, commands, and features** inside Telegram.

---

## 🧠 Available Bots & Strategies

- **Market Maker Bot**  
  Provides liquidity and profits from bid/ask spread

- **HFT (High-Frequency Trading) Bot**  
  Executes rapid trades based on micro price movements

- **Arbitrage Bot**  
  Exploits price inefficiencies across markets

- **End-Cycle Bot**  
  Trades based on late-stage (end-of-round) behavior

- **Momentum / Threshold Bot**  
  Buys based on price thresholds and trends

> ⚠️ Strategy differs per bot — everything else (wallet, UI, commands) is identical.

---

## ✨ Core Features

### 📈 Paper Trading
- Simulate trading with **no real funds**
- No private key required
- Real-time logs and signals
- Best way to test strategies safely

---

### 💵 Real Trading
- Trade with **real USDC**
- Requires wallet private key
- Includes **24-hour free trial**
- Upgrade required after trial

> ⚠️ Use only funds you can afford to lose.

---

### 👛 Wallet System
- Multi-chain deposits:
  - Polygon (min $3)
  - Solana (min $3)
  - Ethereum / BNB (min $10)
  - BTC (if supported)

- Withdraw to:
  - Polygon, Solana, Ethereum, BNB, Base, Arbitrum

- View:
  - Balance
  - Polymarket wallet address

- Gasless withdrawals supported (if enabled)

---

### 🎁 Referrals
- Get your referral link/code
- Invite users and earn rewards
- Withdraw earnings (min $5)

---

### ⚙️ Settings
Full control over trading behavior:

- Entry threshold / trigger
- Trade amount (USDC)
- Redeem delay
- Risk final window
- Risk drop logic
- Opposite position size
- Stop loss (%)

Markets:
- BTC ✅
- ETH ✅
- SOL ✅
- XRP ✅

Security:
- Export private key (⚠️ sensitive)
- Export config (secrets hidden)

---

### 📖 Help
- Tutorials
- Documentation
- Community links

---

## ▶️ Getting Started

1. Open your Telegram bot  
2. Send:

3. Choose from the main menu:

---

## ⌨️ Commands

| Command | Description |
|--------|-------------|
| `/start` | Open main menu |
| `/paper` | Start paper trading |
| `/real` | Start real trading |
| `/upgrade` | Upgrade after trial |
| `/wallet` | Open wallet |
| `/referrals` | Referral system |
| `/settings` | Configure bot |
| `/help` | Help & resources |
| `/settings_export` | Export config |

---

## ⚙️ How It Works

All bots follow the same lifecycle:

### 1. Market Monitoring
- Subscribe to Polymarket orderbooks

### 2. Signal Generation
- Based on strategy (HFT, arbitrage, threshold, etc.)

### 3. Execution
- Paper Trading → simulated orders  
- Real Trading → live orders  

### 4. Risk Management
- Stop loss
- Late-cycle adjustments
- Opposite hedging

### 5. Settlement
- Automatic redeem after resolution

---

## ⚠️ Important Notes

- One active trading session per user
- Real Trading requires private key
- Trial applies only to Real Trading
- Paper Trading is always free
- All bots share identical interface

---

## 🔐 Security & Safety

- **Never share your private key**
- Always verify withdrawal addresses
- Use Paper Trading before Real Trading
- Beware of impersonators — admins never DM first

---

## 🧾 Summary

This project delivers a **professional multi-strategy Polymarket trading system** via Telegram:

- Multiple trading strategies (MM, HFT, Arbitrage, etc.)
- Unified and simple UI
- Built-in wallet and withdrawals
- Advanced risk management tools

---

## 🛠 Setup (For Operators)

To run the bot yourself:

1. Clone the repository
2. Install dependencies
3. Configure environment variables
4. Run the bot

> Full setup instructions are provided in the project documentation.

---

## 📄 License

This project is provided for educational and research purposes. Use at your own risk.

---
