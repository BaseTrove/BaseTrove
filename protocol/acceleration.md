# ⚡ The Acceleration Effect

The floor price of $TROVE doesn't just rise — it rises **faster over time.** This page explains the math behind why, and shows a 12-month simulation of what that looks like in practice.

---

## The Core Mechanic

The floor price formula is:

```
Floor = Vault ETH ÷ Circulating Supply
```

Two things happen simultaneously and continuously:
1. **ETH enters the Vault** (from mining revenue + swap fees)
2. **TROVE is burned** (from buybacks)

Here's the key insight: **as supply shrinks, the same ETH deposit moves the floor further.**

At 1,000 supply, depositing 0.1 ETH moves the floor by 10%.
At 500 supply, the same 0.1 ETH deposit moves it by 20%.
At 200 supply, that same 0.1 ETH moves it by 50%.

The denominator shrinks. Every deposit hits harder. Every burn makes the next deposit more powerful.

---

## The Math in Action

Starting from 1 ETH in the Vault, watch what happens when the same cycle repeats four times — adding 0.5 ETH and burning 200 TROVE each time:

| Cycle | Vault ETH | Supply | Floor | Gain vs. Start |
|---|---|---|---|---|
| Start | 1.0 | 1,000 | 0.001 ETH | — |
| After 1 | 1.5 | 800 | 0.001875 ETH | +87.5% |
| After 2 | 2.0 | 600 | 0.003333 ETH | +233% |
| After 3 | 2.5 | 400 | 0.00625 ETH | +525% |
| After 4 | 3.0 | 200 | 0.015 ETH | +1,400% |

Same inputs. Exponentially larger output. The system accelerates because each burn permanently increases the leverage of every future ETH deposit.

---

## 12-Month Floor Simulation

The table below models BaseTrove's floor price over 12 months under **conservative assumptions** (listed below the table).

| Month | ETH Added | TROVE Burned | Vault ETH | Supply | Floor Price | vs. Launch | Monthly Gain |
|---|---|---|---|---|---|---|---|
| 0 — Launch | 0.50 seed | — | 0.50 | 1,000 | 0.000500 ETH | — | — |
| 1 | +0.25 | 8 | 0.75 | 992 | 0.000756 ETH | +51% | +0.000256 |
| 2 | +0.25 | 8 | 1.00 | 984 | 0.001016 ETH | +103% | +0.000260 |
| 3 | +0.30 | 10 | 1.30 | 974 | 0.001335 ETH | +167% | +0.000319 |
| 4 | +0.35 | 12 | 1.65 | 962 | 0.001715 ETH | +243% | +0.000380 |
| 5 | +0.35 | 12 | 2.00 | 950 | 0.002105 ETH | +321% | +0.000390 |
| 6 | +0.40 | 15 | 2.40 | 935 | 0.002567 ETH | +413% | +0.000462 |
| 7 | +0.45 | 18 | 2.85 | 917 | 0.003108 ETH | +522% | +0.000541 |
| 8 | +0.50 | 20 | 3.35 | 897 | 0.003735 ETH | +647% | +0.000627 |
| 9 | +0.55 | 22 | 3.90 | 875 | 0.004457 ETH | +791% | +0.000722 |
| 10 | +0.60 | 25 | 4.50 | 850 | 0.005294 ETH | +959% | +0.000837 |
| 11 | +0.65 | 28 | 5.15 | 822 | 0.006265 ETH | +1,153% | +0.000971 |
| 12 | +0.70 | 30 | 5.85 | 792 | 0.007386 ETH | +1,377% | +0.001121 |

**The floor price floor grows from 0.0005 ETH to 0.0074 ETH in 12 months — a 14.7× increase — under conservative assumptions.**

---

## The Acceleration Is in the Monthly Gain Column

Look at the rightmost column. The absolute floor increase per month grows from **0.000256 ETH** in month 1 to **0.001121 ETH** in month 12 — **4.4× faster** by the end of year one, despite only modest growth in ETH additions.

This is the acceleration in action. As supply compresses, the same ETH does more work. By month 12, each 0.70 ETH addition moves the floor almost as much as the first 1.5 ETH did at launch.

As mining hardware expands further into year two and three, and supply continues shrinking, this effect becomes increasingly powerful.

---

## Conservative Assumptions Used

These numbers are deliberately conservative. The simulation **does not include:**

- Swap fee revenue to the Vault (every trade adds ETH on top)
- Arbitrage bot volume (free additional fees from dual-pool activity)
- BTC/ZEC/ETC price appreciation (higher coin prices = more ETH per mining cycle)
- Increased trading volume over time

**What it does include:**
- 0.5 ETH Vault seed at launch
- Mining revenue starting at ~0.3 ETH/month (proof-of-concept single miner)
- Mining revenue growing to ~0.7 ETH/month by month 12 as fee revenue funds hardware expansion
- 50% of mining revenue to Vault, 50% to buybacks
- Conservative burn rate: 8–30 TROVE/month depending on buyback budget and market price

Real-world results will vary. Mining profitability depends on hardware, coin prices, energy output, and network difficulty. This simulation exists to illustrate the **mathematical structure** of the acceleration effect — not to promise specific returns.

---

## What This Means for Holders

The longer you hold, the harder each new ETH deposit works for you. The fewer tokens remain in circulation, the more ETH backs each one.

Early holders experience the full duration of supply compression. A holder who buys at launch and holds through month 12 owns a larger and larger share of an Vault that is filling faster and faster.

This is not dependent on new buyers. It is not dependent on hype. It is math — powered by sun, hardware, and a Vault that never stops filling.
