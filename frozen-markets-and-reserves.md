# ❄️ Frozen Markets & Reserves

### **How is a Reserve or Market Frozen in Bonzo Finance?**

In the Bonzo Finance protocol, a reserve can be frozen by calling the `setReserveFreeze` function on the PoolConfigurator contract, which is deployed for each Bonzo Finance market. This function can only be called by addresses with the `RiskAdmin` or `PoolAdmin` role, which is owned by the Bonzo Finance Governance. These roles can also be granted to other addresses by the governance.

### **What Happens When a Reserve is Frozen?**

When a reserve is frozen, certain actions are restricted to protect the stability of the protocol and the interests of its users. In a frozen state, a reserve **does not allow**:

* New supply of assets
* New borrowing of assets
* Rate switching between variable and stable rates

However, a frozen reserve **still allows**:

* Repayment of borrowed assets
* Withdrawal of supplied assets
* Liquidations of undercollateralized positions
* Interest accrual (including stable rate rebalances)

### **Unfreezing a Reserve or Market**

Yes, a frozen reserve or market can be unfrozen using the same process and smart contract function (`setReserveFreeze`) if the conditions are deemed suitable for reinstating supply and borrow functionalities.

### **Paused Reserves: A Step Further**

In addition to freezing, a reserve can also be paused. A paused reserve is more restrictive than a frozen reserve, as it **does not allow** any protocol interactions, including:

* Supply
* Borrow
* Repay
* Rate switching (variable/stable)
* Liquidation
* bToken transfers

The same roles and processes used for freezing and unfreezing apply to pausing and unpausing reserves, via the `setReservePause` function.

### **Enabled Actions: Frozen vs. Paused Reserves**

The table below summarizes the actions that are permitted depending on the state of the reserve:

<table><thead><tr><th width="303">Function</th><th>Frozen</th><th>Paused</th></tr></thead><tbody><tr><td><code>Supply</code></td><td>No</td><td>No</td></tr><tr><td><code>Withdraw</code></td><td>Yes</td><td>No</td></tr><tr><td><code>Borrow</code></td><td>No</td><td>No</td></tr><tr><td><code>Repay</code></td><td>Yes</td><td>No</td></tr><tr><td><code>SwapRateMode</code></td><td>No</td><td>No</td></tr><tr><td><code>RebalanceStableBorrowRate</code></td><td>Yes</td><td>No</td></tr><tr><td><code>SetUseReserveAsCollateral</code></td><td>Yes</td><td>No</td></tr><tr><td><code>Flashloan</code></td><td>Yes</td><td>No</td></tr><tr><td><code>Liquidate</code></td><td>Yes</td><td>No</td></tr><tr><td><code>bToken Transfer</code></td><td>Yes</td><td>No</td></tr></tbody></table>

It's important to note that in the Aave V2 protocol, which Bonzo Finance is based on, it is not possible to pause a specific reserve; only the entire pool can be paused.
