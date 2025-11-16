---
icon: binary
---

# Lend Data API

Welcome to the Bonzo Data API Service documentation. This guide provides comprehensive information about the API endpoints, data structures, and usage examples to help you integrate with the Bonzo Liquidity Pools. Whether you're building custom liquidation services or integrating market statistics into your application, this documentation will assist you every step of the way.

## Introduction

### Overview

The **Bonzo Data API Service** provides current lending pool market statistics and individual account supply and borrow information for the [Bonzo.Finance](https://bonzo.finance) protocol. The service is publicly accessible and can be queried by third parties wishing to interact with the Bonzo Liquidity Pools, such as custom liquidation services or analytical tools.

### Key Features

* **Real-Time Market Data**: Access up-to-date information on supply and borrow pools for supported Hedera tokens.
* **Account Insights**: Retrieve detailed account information, including balances and solvency computations.
* **Public Endpoints**: Open API for developers to build custom solutions and integrations.
* **OpenAPI Specification**: Comprehensive API definitions for easy integration.

## Base URL

{% hint style="warning" %}
With the introduction of EVM ERC-20 assets on "Bonzo Lend" (e.g. $wETH LayerZero) — please utilize this temporary URL for live data, in place of the URL found below: [https://mainnet-data-staging.bonzo.finance/](https://mainnet-data-staging.bonzo.finance/) — notices will be provided via [𝕏](https://x.com/bonzo_finance) and [Discord](https://bonzo.finance/discord) for when the URL below will become active again, after this period of temporary monitoring. Thank you. &#x20;
{% endhint %}

All API requests are made to the following base URL:

```
https://data.bonzo.finance/
```

## Common Response Structure

### Balance Information Object

All token balances are returned in a standardized format:

```typescript
{
  "tiny_token": "0x1234...",     // Hex string of smallest denomination
  "token_display": "100.50",     // Human-readable token amount
  "hbar_tinybar": "0x5678...",   // Hex string of HBAR equivalent in tinybars
  "hbar_display": "50.25",       // Human-readable HBAR equivalent
  "usd_wad": "0x90ab...",       // Hex string of USD value in WAD
  "usd_display": "75.30"         // Human-readable USD value
}
```

## Endpoints

### 1. Account Dashboard

Get detailed information about an account's lending and borrowing positions.

```http
GET /dashboard/{accountId}
```

#### Parameters

<table><thead><tr><th width="154">Name</th><th width="89">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>accountId</code></td><td>string</td><td>Hedera account ID in format <code>shard.realm.num</code></td></tr></tbody></table>

#### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "hts_address": string, //The native hedera address for the account in question
  "evm_address": string, //The 20-byte EVM address for the account as seen by the network’s mirror node, this is the form of account address that must be used when interacting with Bonzo contracts.
  "reserves": [ //A list of reserve currencies and their statistics related to the account in question:
  "average_supply_apy": number, //The average return from supply of all holdings in the pool.
  "average_borrow_apy": number, //The average interest rate from all borrowed tokens from the pool.
  "average_net_apy": number //The average net APY on supplied assets minus the interest rate from borrowed tokens.
    {
      "id": number, //The ID of the reserve currency (typically the index of the currency in the pool’s internal list of reserve currencies.)
      "name": string, //Name of the reserve currency.
      "symbol": string, // The symbol for the reserve currency.
      "coingecko_id": string, //The CoinGecko ID associated with reserve token. Useful to 3rd party external wishing to lookup reserve prices without having to call the Supra Oracle.
      "hts_address": string, //The Native Hedera HTS address of the currency.
      "evm_address": string, //The EVM 20byte address for the currency.
      "atoken_address": string, //The EVM ERC20 address for the corresponding aToken for the reserve currency.
      "stable_debt_address": string, //The EVM ERC20 address for the corresponding stable debt for the reserve currency.
      "variable_debt_address": string, //The EVM ERC20 address for the corresponding variable debt for the reserve currency.
      "protocol_treasury_address": string, //The address of the treasury that receives the protocol's interest reserve payments.
      "decimals": number, //The native number of decimals of the currency.
      "ltv": number, //Loan-to-Value (LTV) of the reserve currency.
      "liquidation_threshold": number, //The liquidation Threshold for the reserve currency.
      "liquidation_bonus": number, //The liquidation bonus of the reserve currency.
      "active": boolean, //The active state of the reserve currency.
      "frozen": boolean, //The frozen state of the reserve currency.
      "variable_borrowing_enabled": boolean, //The variable borrowing state of the reserve currency.
      "stable_borrowing_enabled": boolean, //The stable rate borrowing state of the reserve currency.
      "reserve_factor": number, //The reserve factor.
      "token_balance": BalanceInfo, //The current balance information for the account’s holdings of the reserve token.
      "atoken_balance": BalanceInfo, //The amount of token this account supplied to the liquidity pool contract.
      "stable_debt_balance": BalanceInfo, //The amount of stable rate debt this account has accumulated.
      "variable_debt_balance": BalanceInfo, //The amount of variable rate debt this account has accumulated.
      "available_liquidity": BalanceInfo, //The total system wide liquidity available for this token.
      "total_stable_debt": BalanceInfo, //The total system wide stable debt for this token.
      "total_variable_debt": BalanceInfo, //The total system wide variable debt for this token.
      "total_supply": BalanceInfo, //The sum total of all supplied value of this token across all accounts.
      "borrow_cap": BalanceInfo, //The total system wide borrow limit for this token.
      "supply_cap": BalanceInfo, //The total system wide supply limit for this token.
      "utilization_rate": number, //The total system utilization of supplied token as a percentage.
      "supply_apy": number, //The current supply APY yield in percent.
      "variable_borrow_apy": number, //The current variable borrow APY cost in percent.
      "stable_borrow_apy": number, //The current stable borrow APY cost in percent.
      "use_as_collateral_enabled": boolean, //If true, the supplied balance of this token can be used by account as Collateral for borrowing purposes.
      "price_weibars": string, //The current market price in weibars (hex encoded binary integer)
      "price_usd_wad": string, //The equivalent USD price value in WAD (hex encoded binary integer)
      "price_usd_display": string //The equivalent USD price value for display purposes (string lossy representation).
    }
  ],
  "user_credit": { //Additional credit information attributed to the account in question.
    "hbar_balance": BalanceInfo, //The current account’s native crypto balance.
    "total_supply": BalanceInfo, //The total amount of value this account has supplied across reserve currencies, normalized to value in hbar.
    "total_collateral": BalanceInfo, //The sum total amount of supply that is enabled as collateral, normalized in hbar.
    "total_debt": BalanceInfo, //The sum total amount of account debt, normalized in hbar.
    "credit_limit": BalanceInfo, //The remaining value that this account may borrow, normalized in hbar.
    "liquidation_ltv": number, //Loan to Value threshold at which the borrower can be liquidated.
    "current_ltv": number, //The average loan to value position of this account.
    "max_ltv": number, //Loan-to-Value (LTV) allowed.
    "health_factor": number, //Acocunt’s health factor.
  },
  "timestamp": string //The consensus timestamp this information was generated.
}
```

#### Example Request

```bash
curl https://data.bonzo.finance/dashboard/0.0.1234
```

### 2. List of Debtors

Get a list of all accounts with outstanding debt.

<pre class="language-http"><code class="lang-http"><strong>GET /debtors
</strong></code></pre>

#### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "debtors": string[],  // Array of EVM addresses
  "timestamp": string //The consensus timestamp this information was generated.
}
```

#### Example Request

```bash
curl https://data.bonzo.finance/debtors
```

### 3. Market Information

Get current global state of all Bonzo liquidity pools.

```http
GET /market
```

#### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "reserves": [ //A list of reserve currencies and their global statistics:
    {
      "id": number, //The ID of the reserve currency (typically the index of the currency in the pool’s internal list of reserve currencies.)
      "name": string, //Name of the reserve currency.
      "symbol": string, //The symbol for the reserve currency.
      "coingecko_id": string, //The CoinGecko ID associated with reserve token. Useful to 3rd party external wishing to lookup reserve prices without having to call the Supra Oracle.
      "hts_address": string, //The Native Hedera HTS address of the currency.
      "evm_address": string, //The EVM 20byte address for the currency/
      // ... same as reserves object in dashboard endpoint
    }
  ],
  "timestamp": string //The consensus timestamp this information was generated.
}
```

### 4. Pool Statistics

Get 24-hour usage statistics for the protocol.

```http
GET /stats
```

#### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkit
  "total_supply_value": BalanceInfo, //The total amount of reserves supplied to the entire system, normalized in hBar value.
  "total_borrowed_value": BalanceInfo, //The total amount of reserves borrowed from the entire system, normalized in hBar value.
  "total_liquidity_value": BalanceInfo, //The total amount of supplied reserves minus borrowed, normalized in hBar value.
  "total_deposits_count": number, //Total number of deposits that occurred in the past 24-hour period.
  "total_withdraws_count": number, //Total number of withdrawals that occurred in the past 24-hour period.
  "total_borrows_count": number, //Total number of borrowings that occurred in the past 24-hour period.
  "total_repays_count": number, //Total number of repayments that occurred in the past 24-hour period.
  "total_enable_collateral_count": number, //Total number of times an account approved a deposit can be used as collateral in the past 24-hour period.
  "total_disable_collateral_count": number, //Total number of times an account removed a deposit as collateral in the past 24-hour period.
  "total_flash_loan_count": number, //Total count of flash loans executed in the past 24-hour period.
  "total_flash_loan_fees": BalanceInfo, //Total value of flash loan fees paid to the protocol in the past 24-hour period.
  "total_liquidations_count": number, //Total count of loan liquidations in the past 24-hour period.
  "total_liquidation_payoffs": BalanceInfo, //Total value of loans paid off via liquidations in the past 24-hour period.
  "total_liquidation_rewards": BalanceInfo, //Total value of collateral rewarded to liquidators in the past 24-hour period.
  "total_liquidation_bonuses": BalanceInfo, //Total value of the portion of collateral rewarded to liquidators that is considered the bonus value (value in excess of payoff value) in the past 24-hour  period.
  "total_protocol_fees": BalanceInfo, //Total value of fees collected by the protocol in the past 24-hour period.
  "total_intrest_earned": BalanceInfo, //Total value of interest earned by liquidity suppliers in the past 24-hour period.
  "total_gas_consumed": number, //Total value of gas consumed by the Hedera EVM all protocol activity in the past 24-hour period.
  "total_gas_charged": number, //Total value of gas charged by the Hedera Network to execute the protocol activities in the past 24-hour period, this value may exceed the total gas consumed due to the nature of how hedera manages EVM gas authorizations.
  "total_network_fees": number, //Total native hedera fees beyond gas fees charged to execute protocol activities in the past 24-hour period.
  "total_successful_transactions": number, //Count of all successful transactions submitted to the protocol in the past 24-hour period.
  "total_failed_transactions": number, //Count of transactions submitted to the protocol that failed to execute in the past 24-hour period.
  "active_users": string[], //A array list of accounts (EVM 20byte addresses) that have interacted with the protocol in the past 24-hour period.
  "reserves": [...],  // Same as market endpoint
  "timestamp_start": string, //The consensus timestamp at the beginning of this 24-hour period.
  "timestamp_end": string //The consensus timestamp at the end of this 24-hour period.
}
```

### 5. Protocol Information

Get server and protocol configuration information.

```http
GET /info
```

#### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "mirror_node": string, //The upstream mirror node this system relies upon to retrieve information from the hedera network.
  "lending_pool_address": string, //Address of the lending pool contract, the providing the lending and borrowing interfaces.
  "price_oracle_address": string, //Address of the price oracle contract, the contract the protocol relies upon for current market prices.
  "protocol_data_provider_address": string, //Address of the protocol data provider contract, this is the root contract upon which all other information regarding the protocol, pools, reserves and oracles can be obtained.
  "lending_pool_configurator_address": string, //The configuration module for the protocol.  Monitoring events from this contract can alert applications of changes in the protocol configuration.
  "whbar_hts_address": string, //The Native Hedera HTS address of the token wrapping native hbar crypto.
  "whbar_evm_address": string, //The EVM 20byte address for the address of the token wrapping native hbar crypto.
  "reserves": [...]  // Basic reserve configuration info
}
```

### 6. BONZO Token Information

Get circulation information for the BONZO token.

```http
GET /bonzo
```

### Response

```typescript
{
  "chain_id": string, //The EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //The name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "token_id": string, //The native hedera address for the BONZO token.
  "symbol": string, //The string symbol representing the token.
  "name": string, //The name of the token.
  "memo": string, //The memo record associated with the token.
  "total_supply": string, //The total minted supply of the token, in smallest denomination.
  "circulating_supply": string, //The circulating supply of the token, in smallest denomination.
  "decimals": number, //The number of decimals associated with the token.
  "treasuries": [ //A list of Hedera accounts that make up the various identified treasuries of $BONZO; the balances held by these accounts do not count towards circulating supply.
    {
      "address": string, //The native Hedera address of the treasury account.
      "name": string, //The name of the treasury.
      "balance": string //The balance of token held by the treasury, in smallest denomination.
    }
  ],
  "timestamp": string //The consensus timestamp this information was generated.
}
```

### 7. BONZO Circulation Supply

Get current circulating supply of BONZO token in decimal notation.

```http
GET /bonzo/circulation
```

#### Response

Plain text number representing circulating supply.

## Error Handling

The API uses standard HTTP status codes:

* 200: Success
* 404: Resource not found
* 503: Service unavailable (upstream mirror node error)

Error responses include a text explanation of the issue.

## Rate Limiting

* Current rate limits: None
* Please implement reasonable request throttling in your applications

## Best Practices

1. Cache responses when appropriate to minimize API calls
2. Use the dashboard endpoint instead of market when you have an account ID
3. Implement exponential backoff for retries
4. Monitor the health factor of positions if building liquidation bots

## Example Implementation

Here's a simple JavaScript example to fetch market data:

```javascript
async function getBonzoMarketData() {
  try {
    const response = await fetch('https://data.bonzo.finance/market');
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json();
    
    // Process reserves data
    data.reserves.forEach(reserve => {
      console.log(`${reserve.symbol}: ${reserve.utilization_rate}% utilization`);
      console.log(`Supply APY: ${reserve.supply_apy}%`);
      console.log(`Borrow APY: ${reserve.variable_borrow_apy}%`);
    });
  } catch (error) {
    console.error('Error fetching market data:', error);
  }
}
```

## Support

* Discord: [Join Bonzo Finance Discord](https://www.bonzo.finance/Discord/)





