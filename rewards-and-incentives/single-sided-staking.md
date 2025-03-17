# 🥩 Single-Sided Staking

[Single-sided staking](https://app.bonzo.finance/stake) allows $BONZO token holders to earn yield without providing liquidity or incurring impermanent loss. By staking $BONZO tokens, users receive $xBONZO tokens as a receipt that represents their share of the staking pool. Over time, as rewards are continuously compounded into the pool, the conversion rate between $BONZO and $xBONZO improves, resulting in higher returns when unstaking.

## How Staking Works

The staking mechanism is designed around a continuously improving conversion rate between $BONZO and $xBONZO. This dynamic rate reflects both user contributions and ongoing reward emissions:

### **Staking Process**

1. **Stake $BONZO Tokens:** When staking $BONZO tokens, receive $xBONZO receipt tokens at the current exchange rate.  For example, if the rate is 1 $BONZO = 0.9 $xBONZO, staking 1,000 $BONZO will mint 900 $xBONZO.
2. **Hold $xBONZO Tokens:** The $xBONZO tokens appreciate in value over time as the staking pool grows via continuous reward emissions.
3. **Unstake When Ready: C**onvert  $xBONZO tokens back to $BONZO at any time at the improved conversion rate, without a mandatory lock-up period or unstaking fees (aside from Hedera network fees).

## Key Features

### Token Locking

When staking $BONZO,  tokens are securely locked in the staking smart contract. In return, users receive $xBONZO tokens at the current conversion rate. These $xBONZO tokens represent the user's stake in the protocol and their claim on the underlying $BONZO tokens.

```
Example:
- Current Conversion Rate: 1 $BONZO = 0.9 $xBONZO
- User stakes 1,000 $BONZO
- User receives 900 $xBONZO tokens
- 1,000 $BONZO remains locked in the contract
```

### Automatic Yield Generation

Unlike traditional staking models that distribute rewards at fixed intervals, our system continuously increases the conversion rate between $BONZO and $xBONZO. This means:

* No manual claiming of rewards
* No tracking of reward distribution epochs
* Value accrues seamlessly in the background

The yield is reflected in the continuously improving conversion rate between $BONZO and $xBONZO. The longer user hold their $xBONZO tokens, the more $BONZO they'll receive when they eventually unstake.

### Variable APR

The Annual Percentage Rate (APR) for staking is not fixed and varies based on:

* The total number of $BONZO tokens currently staked in the protocol
* Current $BONZO allocations to the staking rewards contract

Users can check the current effective APR on the [staking dashboard](https://app.bonzo.finance/stake). This rate determines how quickly the conversion rate between $BONZO and $xBONZO improves over time.

<table><thead><tr><th width="334.68487548828125">Monthly Schedule</th><th>$BONZO Token Rewards</th></tr></thead><tbody><tr><td>March 17, 2025 - April 17, 2025</td><td>100,000</td></tr><tr><td>April 17, 2025 - May 17, 2025</td><td>Coming Soon</td></tr></tbody></table>

### Unstaking Flexibility

One of the primary advantages of  staking is  flexibility — users can unstake $xBONZO staking receipt tokens at any time with:

* No minimum lock-up period
* No unstaking fees (except standard Hedera network transaction fees)
* No vesting schedules

When unstaking,  $xBONZO tokens are burned, and the user receives $BONZO tokens at the current conversion rate, which should be higher than when initially staked.

```
CopyExample:
- Initial stake: 1,000 $BONZO → 900 $xBONZO (at 0.9 conversion rate)
- After 6 months: Conversion rate improves to 0.85
- Unstaking 900 $xBONZO would return 1,058.82 $BONZO (900 ÷ 0.85)
- Net gain: 58.82 $BONZO (5.88% return)
```

### Growth Effect

The improving conversion rate creates an effect similar to compound interest. The longer $xBONZO tokens are held, the more $BONZO will be received when unstaked. This incentivizes long-term participation in the protocol's ecosystem.

### Governance Rights (Coming Soon)

In 2025, $xBONZO tokens will grant holders governance rights proportional to their stake. This will allow $xBONZO holders to:

* Vote on protocol changes
* Participate in protocol upgrade decisions
* Influence DAO treasury fund allocations
* Shape the future development of the Bonzo Finance ecosystem
