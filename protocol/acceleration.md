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

At 100,000 supply, depositing 0.1 ETH moves the floor 10%.
At 50,000 supply, the same 0.1 ETH moves it 20%.
At 20,000 supply, that same 0.1 ETH moves it 50%.

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

As daily buybacks gradually burn TROVE over many months, the supply shrinks. Here's what that does to the power of each new ETH deposit — the same 0.25 ETH mining deposit hitting the Vault at different stages of supply compression:

| Stage | Supply Remaining | Vault ETH | Same 0.25 ETH deposit raises floor by... |
|---|---|---|---|
| Launch | 100,000 | 0.50 | **+0.0000025 ETH** per TROVE |
| A few months in | 80,000 | 2.00 | **+0.0000031 ETH** per TROVE |
| Mid way | 60,000 | 3.50 | **+0.0000042 ETH** per TROVE |
| Later | 40,000 | 5.50 | **+0.0000063 ETH** per TROVE |
| Deep compression | 20,000 | 7.50 | **+0.0000125 ETH** per TROVE |

The same 0.25 ETH deposit is **5× more powerful** at 20,000 supply than at launch. The miners keep putting in the same revenue — it just hits harder every time a token gets burned.

This is the acceleration. Not some overnight event — but the slow, compounding result of daily buybacks gradually shrinking the supply until every single deposit lands with significantly more force.

Supply doesn't drop to 20,000 overnight. It gets there over months or years of continuous buybacks. The table just shows what each future deposit is worth once you arrive at that stage — and the floor level it's moving from is already much higher by then too.

---

## 12-Month Simulation

The table below models the floor price over 12 months. Two scenarios are shown side by side: one where TROVE trades **near floor** (low premium, efficient burns) and one where it trades at a **5× market premium** (high premium, fewer burns but vault still fills).

### Scenario A — Trading Near Floor (high burn efficiency)

| Month | ETH to Vault | TROVE Burned | Vault ETH | Supply | Floor |
|---|---|---|---|---|---|
| 0 — Launch | 0.50 seed | — | 0.50 | 100,000 | 0.0000050 ETH |
| 1 | +0.25 | 5,500 | 0.75 | 94,500 | 0.0000079 ETH |
| 2 | +0.25 | 4,800 | 1.00 | 89,700 | 0.0000112 ETH |
| 3 | +0.30 | 4,200 | 1.30 | 85,500 | 0.0000152 ETH |
| 4 | +0.35 | 3,600 | 1.65 | 81,900 | 0.0000201 ETH |
| 5 | +0.35 | 3,000 | 2.00 | 78,900 | 0.0000254 ETH |
| 6 | +0.40 | 2,500 | 2.40 | 76,400 | 0.0000314 ETH |
| 7 | +0.45 | 2,200 | 2.85 | 74,200 | 0.0000384 ETH |
| 8 | +0.50 | 2,000 | 3.35 | 72,200 | 0.0000464 ETH |
| 9 | +0.55 | 1,800 | 3.90 | 70,400 | 0.0000554 ETH |
| 10 | +0.60 | 1,600 | 4.50 | 68,800 | 0.0000654 ETH |
| 11 | +0.65 | 1,400 | 5.15 | 67,400 | 0.0000764 ETH |
| 12 | +0.70 | 1,200 | 5.85 | 66,200 | 0.0000884 ETH |

**Floor after 12 months: 0.0000884 ETH → +1,667% from launch**

---

### Scenario B — Trading at 5× Floor Premium (fewer burns, vault-led growth)

| Month | ETH to Vault | TROVE Burned | Vault ETH | Supply | Floor |
|---|---|---|---|---|---|
| 0 — Launch | 0.50 seed | — | 0.50 | 100,000 | 0.0000050 ETH |
| 1 | +0.25 | 1,100 | 0.75 | 98,900 | 0.0000076 ETH |
| 2 | +0.25 | 1,000 | 1.00 | 97,900 | 0.0000102 ETH |
| 3 | +0.30 | 900 | 1.30 | 97,000 | 0.0000134 ETH |
| 4 | +0.35 | 800 | 1.65 | 96,200 | 0.0000172 ETH |
| 5 | +0.35 | 600 | 2.00 | 95,600 | 0.0000209 ETH |
| 6 | +0.40 | 600 | 2.40 | 95,000 | 0.0000253 ETH |
| 7 | +0.45 | 500 | 2.85 | 94,500 | 0.0000302 ETH |
| 8 | +0.50 | 500 | 3.35 | 94,000 | 0.0000356 ETH |
| 9 | +0.55 | 400 | 3.90 | 93,600 | 0.0000417 ETH |
| 10 | +0.60 | 400 | 4.50 | 93,200 | 0.0000483 ETH |
| 11 | +0.65 | 400 | 5.15 | 92,800 | 0.0000555 ETH |
| 12 | +0.70 | 300 | 5.85 | 92,500 | 0.0000632 ETH |

**Floor after 12 months: 0.0000632 ETH → +1,165% from launch**

---

## What the Two Scenarios Tell You

Both scenarios result in a floor price that is **10–17× higher** than launch after 12 months — from mining revenue alone, before swap fees or arb activity.

The difference:
- **Near floor:** burns are powerful, supply compresses hard, floor accelerates more aggressively
- **High premium:** burns are smaller in token terms, but the Vault fills at the same ETH rate — the floor still rises substantially, just led more by ETH accumulation than supply compression

In practice, both forces operate together. When market price runs far above floor, the Vault quietly fills. When price retraces toward floor, burns become efficient again and supply compresses rapidly. The floor benefits either way.

---

## The Monthly Gain Acceleration

In Scenario A, the absolute monthly floor gain accelerates from **+0.0000029 ETH** in month 1 to **+0.0000120 ETH** in month 12 — **4× faster** in absolute terms, driven by the shrinking supply multiplying each ETH deposit.

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
- Floor arbitrage volume (traders buying DEX dips to sell to Vault)
- BTC/ZEC/ETC price appreciation
- Community-driven volume

This simulation illustrates the **mathematical structure** of the acceleration effect. It is not a promise of returns. Mining profitability varies with hardware, coin prices, network difficulty, and energy output.
