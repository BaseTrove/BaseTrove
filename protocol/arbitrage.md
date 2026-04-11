# ⚖️ Arbitrage

BaseTrove has a built-in arbitrage mechanism that works in holders' favour — powered by the gap between the DEX market price and the Vault's guaranteed floor price.

---

## The Floor Arbitrage

$TROVE trades on the open market at whatever price buyers and sellers agree on. The Vault simultaneously offers a **guaranteed redemption price** — the floor.

When the DEX price drops toward or below the Vault floor, a textbook arbitrage opportunity opens:

```
DEX price < Vault floor
        ↓
Rational traders buy TROVE cheaply on DEX
        ↓
Sell to Vault at guaranteed floor price
        ↓
Pocket the ETH difference
        ↓
TROVE sold to Vault is permanently burned
        ↓
Supply shrinks → floor rises
```

This is a **hard floor** enforced not by promises but by rational self-interest. Anyone can execute it. No team involvement needed. The market corrects itself.

---

## Why It Benefits Holders

Every trader who exploits this arbitrage is:
1. Buying TROVE from the market (buy pressure)
2. Burning it through the Vault (permanent supply reduction)
3. Raising the floor price for everyone remaining

The arb trader profits. The remaining holders benefit. This is one of the few mechanisms in DeFi where arbitrageurs and long-term holders are fully aligned.

---

## The Self-Reinforcing Loop

```
Market dips near floor
        ↓
Arb traders buy + burn via Vault
        ↓
Supply shrinks
        ↓
Floor rises above where it was before the dip
        ↓
Market recovers — now chasing a higher floor
```

Every dip that triggers floor arbitrage leaves $TROVE with a higher floor than before the dip occurred. The floor is not just a safety net — it's a ratchet.

---

## All Market Participants Help the Vault

| Actor | Motivation | Effect on $TROVE |
|---|---|---|
| Floor arbitrageur | Buy DEX cheap, sell to Vault | Burns supply, floor rises |
| Regular buyer | Speculate on price appreciation | Swap fees → Vault |
| Regular seller | Take profit | Swap fees → Vault |
| Miner | Generate mining yield | Buybacks + Vault deposits |

Everyone who interacts with $TROVE contributes to the Vault — whether they intend to or not.
