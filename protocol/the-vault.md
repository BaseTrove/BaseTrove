# 🏦 The Vault

The Vault is the backbone of BaseTrove. A smart contract that holds ETH and guarantees every $TROVE holder a minimum redemption price — at all times, unconditionally.

---

## The Price Floor Formula

```
Price Floor = Total ETH in Vault ÷ Circulating $TROVE Supply
```

This is the minimum price at which anyone can sell $TROVE directly to the Vault, at any time, with zero fees.

---

## The Compounding Acceleration Effect

This is the core mechanic that makes BaseTrove different from every other deflationary token.

Every burn reduces the number of tokens that need to divide the ETH in the Vault. So the floor price doesn't just rise — it **rises faster over time.**

**Example:**

| Event | Vault ETH | Supply | Floor |
|---|---|---|---|
| Start | 1 ETH | 1,000 | 0.001 ETH |
| +0.1 ETH deposited | 1.1 ETH | 1,000 | 0.0011 ETH (+10%) |
| 100 TROVE burned | 1.1 ETH | 900 | 0.00122 ETH (+11%) |
| +0.1 ETH deposited | 1.2 ETH | 900 | 0.00133 ETH (+9%) |
| 100 TROVE burned | 1.2 ETH | 800 | 0.0015 ETH (+12.7%) |
| +0.1 ETH deposited | 1.3 ETH | 800 | 0.001625 ETH (+8.3%) |

The same ETH deposit that moved the floor 10% at 1,000 supply moves it **further** at 800 supply — and further still at 500, 300, 100. As the supply compresses, every new ETH deposit hits harder. Every burn makes the next burn more powerful.

**The Vault loads up faster the more tokens get burned.**

---

## What Fills the Vault

| Source | Description |
|---|---|
| **Mining Revenue (50%)** | Half of all ASIC miner earnings, deposited on every cycle |
| **Swap Fee (50% of 2–5%)** | Half of every DEX trade fee, flowing in continuously |
| **Arb Bot Volume** | Every arbitrage trade between the two pools generates fees → Vault |

The Vault never pays salaries, operations, or marketing. It exists solely to back $TROVE holders.

---

## What Burns Supply

Every burn is a one-way door. Burned tokens are gone forever, and the ETH in the Vault now needs to be divided among fewer tokens.

| Event | Burns |
|---|---|
| Mining buyback | ETH buys TROVE from LP → burned |
| Vault sale (DApp) | Holder sells TROVE to Vault → burned, ETH paid out |

Both happen continuously. The total burned counter grows every day, and each new burn accelerates the floor price rise for everyone remaining.

---

## Selling to the Vault

Any holder can sell $TROVE to the Vault at the guaranteed floor price via the DApp:

1. Connect wallet on Base
2. Enter amount of TROVE to sell
3. Receive ETH at the current floor price — instantly, no slippage
4. Your TROVE is permanently burned

**Zero fees on Vault sales.** You receive the full floor price in ETH.

> The floor price is a *minimum*. $TROVE typically trades above floor on the open market. Selling to the Vault is most relevant when DEX price falls near or below floor — which is when the arb mechanism kicks in to correct it.

---

## Why the Floor Never Goes Down

The floor can only stay flat or rise. It stays flat only if:
- No ETH enters the Vault (mining stops AND no trading)
- No TROVE is burned

Both conditions simultaneously is effectively impossible while miners are running. In practice, **the floor rises every single day.**
