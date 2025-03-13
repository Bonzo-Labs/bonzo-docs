---
hidden: true
---

# 🥩 Single-Sided Staking

[Single-sided staking](https://app.bonzo.finance/stake) allows $BONZO token holders to earn yield without providing liquidity pairs or taking on impermanent loss risk. By staking $BONZO tokens, you receive $xBONZO tokens which automatically increase in value relative to $BONZO over time.

## How Staking Works

The staking mechanism is built around a conversion rate between $BONZO and $xBONZO that continuously improves, providing passive yield to stakers.

### The Staking Process

1. **Stake Your $BONZO Tokens**: Convert your $BONZO tokens to $xBONZO tokens at the current exchange rate
2. **Hold $xBONZO Tokens**: Your $xBONZO appreciates in value relative to $BONZO automatically
3. **Unstake When Ready**: Convert $xBONZO back to $BONZO at the improved conversion rate whenever you choose

## Key Features

### Token Locking

When you stake $BONZO, your tokens are securely locked in the staking smart contract. In return, you receive $xBONZO tokens at the current conversion rate. These $xBONZO tokens represent your stake in the protocol and your claim on the underlying $BONZO tokens.

```
Example:
- Current Conversion Rate: 1 $BONZO = 0.9 $xBONZO
- You stake 1,000 $BONZO
- You receive 900 $xBONZO tokens
- Your 1,000 $BONZO remains locked in the contract
```

### Automatic Yield Generation

Unlike traditional staking models that distribute rewards at fixed intervals, our system continuously increases the conversion rate between $BONZO and $xBONZO. This means:

* No manual claiming of rewards
* No tracking of reward distribution epochs
* Value accrues seamlessly in the background

The yield is reflected in the continuously improving conversion rate between $BONZO and $xBONZO. The longer you hold your $xBONZO tokens, the more $BONZO you'll receive when you eventually unstake.

### Variable APR

The Annual Percentage Rate (APR) for staking is not fixed and varies based on:

* The total number of $BONZO tokens currently staked in the protocol
* Current $BONZO allocations to the staking rewards contract
* Market conditions

You can check the current effective APR on the [staking dashboard](https://app.bonzo.finance/stake). This rate determines how quickly the conversion rate between $BONZO and $xBONZO improves over time.

### Unstaking Flexibility

One of the primary advantages of  staking is  flexibility — users can unstake $xBONZO tokens at any time with:

* No minimum lock-up period
* No unstaking fees (except standard Hedera network transaction fees)
* No vesting schedules

When unstaking,  $xBONZO tokens are burned, and the user receives $BONZO tokens at the current conversion rate, which will be higher than when initially staked.

```
CopyExample:
- Initial stake: 1,000 $BONZO → 900 $xBONZO (at 0.9 conversion rate)
- After 6 months: Conversion rate improves to 0.85
- Unstaking 900 $xBONZO would return 1,058.82 $BONZO (900 ÷ 0.85)
- Net gain: 58.82 $BONZO (5.88% return)
```

### Growth Effect

The improving conversion rate creates an effect similar to compound interest. The longer you hold your $xBONZO tokens, the more $BONZO you'll receive when you unstake. This incentivizes long-term holding and participation in the protocol ecosystem.

### Governance Rights (Coming Soon)

In 2025, $xBONZO tokens will grant holders governance rights proportional to their stake. This will allow $xBONZO holders to:

* Vote on protocol changes
* Participate in protocol upgrade decisions
* Influence DAO treasury fund allocations
* Shape the future development of the Bonzo Finance ecosystem
