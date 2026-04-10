# Mining Engine Overview

The Mining Engine is what separates BaseTrove from every other deflationary token. It is a fleet of physical ASIC miners powered by solar energy and battery storage, operating 24 hours a day, 7 days a week, generating real-world revenue that flows entirely back to $TROVE holders.

---

## The Problem With Most Deflationary Tokens

Most projects claim deflationary mechanics but rely on a single fuel source: **trading volume.** Swap taxes only flow into the vault when people are buying and selling. In a bear market or low-attention period, volume dries up, taxes stop, and the mechanism stalls.

BaseTrove's Mining Engine solves this with an external, self-sustaining revenue source that has nothing to do with crypto market sentiment.

---

## The Engine at a Glance

| Property | Detail |
|---|---|
| **Hardware** | ASIC miners (Bitcoin mining) |
| **Power Source** | Solar panels + battery storage |
| **Uptime** | 24/7/365 |
| **Revenue Asset** | Bitcoin (BTC) |
| **Deployment Asset** | ETH on Base |
| **Revenue Split** | 50% → Vault · 50% → Buyback & Burn |
| **Buyback Wallet** | Public, on-chain, verifiable |

---

## Revenue Flow

```
☀️  Sunlight → Solar Panels → Battery Storage
                    ↓
             ASIC Miners (BTC)
                    ↓
         Convert BTC → ETH on Base
                    ↓
         ┌──────────────────┐
         │                  │
        50%                50%
         ↓                  ↓
     🏦 Vault          🔥 Buyback
   (ETH deposited)   (Random LP → Burn)
```

---

## Why Solar + Battery?

Traditional mining operations depend on grid electricity — which is subject to price volatility, outages, and geographic constraints. Solar with battery backup changes the equation:

- **Near-zero marginal energy cost** — once panels and batteries are installed, sunlight is free
- **24/7 operation** — batteries store daytime energy for nighttime mining, ensuring continuous revenue
- **Location flexibility** — can be deployed in high-sun regions with low land costs
- **Predictable output** — solar irradiance data allows revenue forecasting with reasonable accuracy

This translates directly to **predictable, continuous Vault deposits** — a guarantee no trading-volume-dependent mechanism can match.

> Details: [Solar-Powered ASIC Miners](solar-asic-miners.md) · [Buyback & Burn Mechanism](buyback-mechanism.md) · [Transparency](transparency.md)
