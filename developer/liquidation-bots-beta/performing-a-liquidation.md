# Performing a Liquidation

Now, we'll execute the script to perform the liquidation.

### 1. Identify Liquidatable Accounts

The script contains a list of accounts that are eligible for liquidation. You can get these accounts through this API on the testnet:

* [Liquidatable Accounts API](https://bonzo-data-api-testnet-a3d6b2946b71.herokuapp.com/liquidatable)

{% hint style="info" %}
The "Liquidatable Accounts API" for the Hedera mainnet will be made available soon.
{% endhint %}

### 2. Configure the Liquidation Parameters

In the script, the `liquidate` function is set up to liquidate a specific user. Update the parameters accordingly.

```typescript
async function liquidate() {
  const user = liquidatables[2]; // Index of the user in the list
  const collateralReserve = "0xCollateralAssetAddress"; // Collateral asset address
  const debtReserve = "0xDebtAssetAddress"; // Debt asset address
  const borrowed = ethers.utils.parseUnits("100", 18); // Amount to cover

  // ... rest of the code
}
```

* **`user`**: The address of the user to liquidate.
* **`collateralReserve`**: The address of the collateral asset.
* **`debtReserve`**: The address of the debt asset.
* **`borrowed`**: The amount of debt to cover (in wei).

Replace the placeholders with the actual values based on the user's positions.

### 3. Execute the Script

Run the script using Hardhat:

```bash
npx hardhat run scripts/liquidationFlashLoan/liquidate.ts --network hedera_testnet
```

### 4. Monitor the Output

The script will output the progress of the liquidation:

```yaml
User: 0x78c3edaf3ae5dc69e688d7f41f85c4745ccd552c
Caller address: 0xYourWalletAddress
Collateral Reserve: 0xCollateralAssetAddress
Debt Reserve: 0xDebtAssetAddress
Borrowed: 100

Flash loan successful
```

If the liquidation is successful, you'll see a confirmation message. If there are errors, the script will output the error details.
