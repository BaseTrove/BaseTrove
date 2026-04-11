# ⚡ The Acceleration Effect

The floor price of $TROVE doesn't just rise — it rises **faster over time.** This page explains the math behind why, how market price affects the burn rate, and what that looks like across different scenarios.

---

## The Core Mechanic

The floor price formula is:

```
Floor = Vault ETH ÷ Circulating Supply
```

Two things happen simultaneously and continuously:
1. **ETH enters the Vault** (mining revenue + swap fees) — consistent, regardless of market price
2. **TROVE is burned** (from buybacks) — variable, depends on what the market is charging

Here's the key insight: **as supply shrinks, the same ETH deposit moves the floor further.**

At 1,000 supply, depositing 0.1 ETH moves the floor 10%.
At 500 supply, the same 0.1 ETH moves it 20%.
At 200 supply, that same 0.1 ETH moves it 50%.

The denominator shrinks. Every deposit hits harder. Every burn makes the next deposit more powerful.

---

## How Market Price Affects Burns

When buyback ETH is deployed to purchase TROVE from the DEX, the number of tokens burned depends on the **market price** — not the floor price.

```
TROVE burned = Buyback ETH ÷ DEX Market Price
```

This creates a natural relationship between market cap and burn rate:

| Market Price vs Floor | Example Buyback | TROVE Burned |
|---|---|---|
| 1× floor (at floor) | 0.25 ETH | Most — price is cheapest |
| 2× floor | 0.25 ETH | Half as many |
| 5× floor | 0.25 ETH | 5× fewer |
| 10× floor | 0.25 ETH | 10× fewer |

**When market cap is high, each buyback burns fewer tokens — but the Vault still fills at the same rate.**

This is not a flaw. It is a self-balancing mechanism:

- **High market cap:** Vault fills steadily. Burns are slow. Floor rises primarily from ETH accumulation.
- **Low market cap / near floor:** Burns are efficient — more TROVE removed per ETH. Supply compresses fast. Floor rises from both sides simultaneously.

In both cases, the floor goes up. The composition just differs.

---

## The Math in Action

Starting from 1 ETH in the Vault, the same cycle repeats four times — adding 0.5 ETH and burning 200 TROVE:

| Cycle | Vault ETH | Supply | Floor | Gain vs. Start |
|---|---|---|---|---|
| Start | 1.0 | 1,000 | 0.001 ETH | — |
| After 1 | 1.5 | 800 | 0.001875 ETH | +87.5% |
| After 2 | 2.0 | 600 | 0.003333 ETH | +233% |
| After 3 | 2.5 | 400 | 0.00625 ETH | +525% |
| After 4 | 3.0 | 200 | 0.015 ETH | +1,400% |

Same inputs. Exponentially larger output. Each burn permanently increases the leverage of every future ETH deposit.

---

## 12-Month Simulation

The table below models the floor price over 12 months. Two scenarios are shown side by side: one where TROVE trades **near floor** (low premium, efficient burns) and one where it trades at a **5× market premium** (high premium, fewer burns but vault still fills).

### Scenario A — Trading Near Floor (high burn efficiency)

| Month | ETH to Vault | TROVE Burned | Vault ETH | Supply | Floor |
|---|---|---|---|---|---|
| 0 — Launch | 0.50 seed | — | 0.50 | 1,000 | 0.000500 ETH |
| 1 | +0.25 | 55 | 0.75 | 945 | 0.000794 ETH |
| 2 | +0.25 | 48 | 1.00 | 897 | 0.001115 ETH |
| 3 | +0.30 | 42 | 1.30 | 855 | 0.001520 ETH |
| 4 | +0.35 | 36 | 1.65 | 819 | 0.002015 ETH |
| 5 | +0.35 | 30 | 2.00 | 789 | 0.002535 ETH |
| 6 | +0.40 | 25 | 2.40 | 764 | 0.003141 ETH |
| 7 | +0.45 | 22 | 2.85 | 742 | 0.003841 ETH |
| 8 | +0.50 | 20 | 3.35 | 722 | 0.004640 ETH |
| 9 | +0.55 | 18 | 3.90 | 704 | 0.005540 ETH |
| 10 | +0.60 | 16 | 4.50 | 688 | 0.006540 ETH |
| 11 | +0.65 | 14 | 5.15 | 674 | 0.007642 ETH |
| 12 | +0.70 | 12 | 5.85 | 662 | 0.008836 ETH |

**Floor after 12 months: 0.00884 ETH → +1,667% from launch**

---

### Scenario B — Trading at 5× Floor Premium (fewer burns, vault-led growth)

| Month | ETH to Vault | TROVE Burned | Vault ETH | Supply | Floor |
|---|---|---|---|---|---|
| 0 — Launch | 0.50 seed | — | 0.50 | 1,000 | 0.000500 ETH |
| 1 | +0.25 | 11 | 0.75 | 989 | 0.000758 ETH |
| 2 | +0.25 | 10 | 1.00 | 979 | 0.001021 ETH |
| 3 | +0.30 | 9 | 1.30 | 970 | 0.001340 ETH |
| 4 | +0.35 | 8 | 1.65 | 962 | 0.001715 ETH |
| 5 | +0.35 | 6 | 2.00 | 956 | 0.002092 ETH |
| 6 | +0.40 | 6 | 2.40 | 950 | 0.002526 ETH |
| 7 | +0.45 | 5 | 2.85 | 945 | 0.003016 ETH |
| 8 | +0.50 | 5 | 3.35 | 940 | 0.003564 ETH |
| 9 | +0.55 | 4 | 3.90 | 936 | 0.004167 ETH |
| 10 | +0.60 | 4 | 4.50 | 932 | 0.004828 ETH |
| 11 | +0.65 | 4 | 5.15 | 928 | 0.005550 ETH |
| 12 | +0.70 | 3 | 5.85 | 925 | 0.006324 ETH |

**Floor after 12 months: 0.00632 ETH → +1,165% from launch**

---

## What the Two Scenarios Tell You

Both scenarios result in a floor price that is **10–17× higher** than launch after 12 months — from mining revenue alone, before swap fees or arb activity.

The difference:
- **Near floor:** burns are powerful, supply compresses hard, floor accelerates more aggressively
- **High premium:** burns are smaller in token terms, but the Vault fills at the same ETH rate — the floor still rises substantially, just led more by ETH accumulation than supply compression

In practice, both forces operate together. When market price runs far above floor, the Vault quietly fills. When price retraces toward floor, burns become efficient again and supply compresses rapidly. The floor benefits either way.

---

## The Monthly Gain Acceleration

In Scenario A, the absolute monthly floor gain accelerates from **+0.000294 ETH** in month 1 to **+0.001194 ETH** in month 12 — **4× faster** in absolute terms, driven by the shrinking supply multiplying each ETH deposit.

This is the core compounding effect. The system does not plateau. It accelerates as it runs.

---

## Assumptions & Disclaimer

**Included:**
- 0.5 ETH Vault seed at launch
- Mining revenue: ~0.5 ETH/month growing to ~1.4 ETH/month as hardware expands (50% to Vault, 50% to buybacks)
- Scenario A burn rate: market price assumed at ~1.1–1.5× floor
- Scenario B burn rate: market price assumed at ~5× floor throughout

**Not included** (real results likely better):
- Swap fee revenue to Vault
- Arbitrage bot volume generating additional fees
- BTC/ZEC/ETC price appreciation
- Community-driven volume

This simulation illustrates the **mathematical structure** of the acceleration effect. It is not a promise of returns. Mining profitability varies with hardware, coin prices, network difficulty, and energy output.
