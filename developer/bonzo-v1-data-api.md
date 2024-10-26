# 📊 Bonzo v1 Data API

Welcome to the Bonzo Data API Service documentation. This guide provides comprehensive information about the API endpoints, data structures, and usage examples to help you integrate with the Bonzo Liquidity Pools. Whether you're building custom liquidation services or integrating market statistics into your application, this documentation will assist you every step of the way.

## Introduction

### Overview

The **Bonzo Data API Service** provides current lending pool market statistics and individual account supply and borrow information for the [Bonzo.Finance](https://bonzo.finance) protocol. The service is publicly accessible and can be queried by third parties wishing to interact with the Bonzo Liquidity Pools, such as custom liquidation services or analytical tools.

### Key Features

* **Real-Time Market Data**: Access up-to-date information on supply and borrow pools for supported Hedera tokens.
* **Account Insights**: Retrieve detailed account information, including balances and solvency computations.
* **Public Endpoints**: Open API for developers to build custom solutions and integrations.
* **Swagger Interface**: User-friendly interface for exploring and testing API endpoints.
* **OpenAPI Specification**: Comprehensive API definitions for easy integration.

## Base URL

All API requests are made to the following base URL:

```
https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/
```

## Swagger Interface

For interactive API exploration and testing, visit the Swagger UI:

<pre><code><strong>https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/swagger/index.html
</strong></code></pre>

## OpenAPI Specification

The OpenAPI 3.0 specification for the API is available at:

```
https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/swagger/v1/swagger.json
```

{% hint style="info" %}
You can use this specification with tools like Postman or Swagger Codegen to generate client libraries.
{% endhint %}

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
  "chain_id": string, //the EIP155 identifier of the hedera network used to create Ethereum transactions.
  "network_name": string, //the name identifier of the hedera network compatible with forNetwork and other native SDK toolkits.
  "hts_address": string, //the native hedera address for the account in question
  "evm_address": string, //the 20-byte EVM address for the account as seen by the network’s mirror node, this is the form of account address that must be used when interacting with Bonzo contracts.
  "reserves": [ //A list of reserve currencies and their statistics related to the account in question:
    {
      "id": number, //The ID of the reserve currency (typically the index of the currency in the pool’s internal list of reserve currencies.)
      "name": string,
      "symbol": string,
      "coingecko_id": string,
      "hts_address": string,
      "evm_address": string,
      "atoken_address": string,
      "stable_debt_address": string,
      "variable_debt_address": string,
      "protocol_treasury_address": string,
      "decimals": number,
      "ltv": number,
      "liquidation_threshold": number,
      "liquidation_bonus": number,
      "active": boolean,
      "frozen": boolean,
      "variable_borrowing_enabled": boolean,
      "stable_borrowing_enabled": boolean,
      "reserve_factor": number,
      "token_balance": BalanceInfo,
      "atoken_balance": BalanceInfo,
      "stable_debt_balance": BalanceInfo,
      "variable_debt_balance": BalanceInfo,
      "available_liquidity": BalanceInfo,
      "total_stable_debt": BalanceInfo,
      "total_variable_debt": BalanceInfo,
      "total_supply": BalanceInfo,
      "borrow_cap": BalanceInfo,
      "supply_cap": BalanceInfo,
      "utilization_rate": number,
      "supply_apy": number,
      "variable_borrow_apy": number,
      "stable_borrow_apy": number,
      "use_as_collateral_enabled": boolean,
      "price_weibars": string,
      "price_usd_wad": string,
      "price_usd_display": string
    }
  ],
  "user_credit": {
    "hbar_balance": BalanceInfo,
    "total_supply": BalanceInfo,
    "total_collateral": BalanceInfo,
    "total_debt": BalanceInfo,
    "credit_limit": BalanceInfo,
    "liquidation_ltv": number,
    "current_ltv": number,
    "max_ltv": number,
    "health_factor": number,
    "average_supply_apy": number,
    "average_borrow_apy": number,
    "average_net_apy": number
  },
  "timestamp": string
}
```

#### Example Request

```bash
curl https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/dashboard/0.0.1234
```

### 2. List of Debtors

Get a list of all accounts with outstanding debt.

<pre class="language-http"><code class="lang-http"><strong>GET /debtors
</strong></code></pre>

#### Response

```typescript
{
  "chain_id": string,
  "network_name": string,
  "debtors": string[],  // Array of EVM addresses
  "timestamp": string
}
```

#### Example Request

```bash
curl https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/debtors
```

### 3. Market Information

Get current global state of all Bonzo liquidity pools.

```http
GET /market
```

#### Response

```typescript
{
  "chain_id": string,
  "network_name": string,
  "reserves": [
    {
      "id": number,
      "name": string,
      "symbol": string,
      "coingecko_id": string,
      "hts_address": string,
      "evm_address": string,
      // ... same as reserves object in dashboard endpoint
    }
  ],
  "timestamp": string
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
  "chain_id": string,
  "network_name": string,
  "total_supply_value": BalanceInfo,
  "total_borrowed_value": BalanceInfo,
  "total_liquidity_value": BalanceInfo,
  "total_deposits_count": number,
  "total_withdraws_count": number,
  "total_borrows_count": number,
  "total_repays_count": number,
  "total_enable_collateral_count": number,
  "total_disable_collateral_count": number,
  "total_flash_loan_count": number,
  "total_flash_loan_fees": BalanceInfo,
  "total_liquidations_count": number,
  "total_liquidation_payoffs": BalanceInfo,
  "total_liquidation_rewards": BalanceInfo,
  "total_liquidation_bonuses": BalanceInfo,
  "total_protocol_fees": BalanceInfo,
  "total_interest_earned": BalanceInfo,
  "total_gas_consumed": number,
  "total_gas_charged": number,
  "total_network_fees": number,
  "total_successful_transactions": number,
  "total_failed_transactions": number,
  "active_users": string[],
  "reserves": [...],  // Same as market endpoint
  "timestamp_start": string,
  "timestamp_end": string
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
  "chain_id": string,
  "network_name": string,
  "mirror_node": string,
  "lending_pool_address": string,
  "price_oracle_address": string,
  "protocol_data_provider_address": string,
  "lending_pool_configurator_address": string,
  "whbar_hts_address": string,
  "whbar_evm_address": string,
  "reserves": [...]  // Basic reserve configuration info
}
```

### 6. BONZO Token Information

Get circulation information for the BONZO token.

{% hint style="info" %}
Note: Before the Token Generation Event (TGE), this endpoint returns placeholder data.
{% endhint %}

```http
GET /bonzo
```

### Response

```typescript
{
  "chain_id": string,
  "network_name": string,
  "token_id": string,
  "symbol": string,
  "name": string,
  "memo": string,
  "total_supply": string,
  "circulating_supply": string,
  "decimals": number,
  "treasuries": [
    {
      "address": string,
      "name": string,
      "balance": string
    }
  ],
  "timestamp": string
}
```

### 7. BONZO Circulation Supply

{% hint style="info" %}
Note: Before the Token Generation Event (TGE), this endpoint returns placeholder data.
{% endhint %}

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
    const response = await fetch('https://bonzo-data-api-eceac9d8a2aa.herokuapp.com/market');
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

* GitHub Issues: [Bonzo-Labs/bonzo-finance](https://github.com/bonzo-labs)
* Discord: [Join Bonzo Finance Discord](https://www.bonzo.finance/Discord/)
