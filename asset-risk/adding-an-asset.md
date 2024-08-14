# Adding an Asset

Bonzo Finance enables users to deposit and borrow digital assets through the pooling of funds. Depositors receive protocol-issued aTokens, which accumulate deposits and the interest generated. Each loan is secured by collateral acting as a risk mitigation tool against default. As the means of exchange, assets are central in Bonzo Finance's non-custodial lending operations. More details on how the protocol works can be found in Bonzo Finance's [documentation](https://docs.bonzo.finance).

Given the specificities of Bonzo Finance's model, the selection of assets has been performed with the following constraints:

1. **Each additional asset will slightly increase the gas cost of the borrow and redeem actions permanently on the Hedera network.** The asset must be included in the smart contract, adding complexity and thus costs.
2. **Each asset added to the Bonzo Finance protocol as collateral increases the protocol risk of insolvency.** From a financial perspective, the assets of Bonzo Finance are collateral, while the liabilities are the loaned amounts. The underlying assets for collateral and loaned amounts often differ, with loans mostly taken in stablecoins and backed by volatile tokens. This means the protocol is heavily exposed to the failure of assets supported as collateral and their market fluctuations.
3. **A centralized asset accepted as collateral exposes the protocol to its centralization risk.** The single point of failure risks of underlying assets extend to the Bonzo Finance protocol.
4. **Assets only enabled for depositing and borrowing (not usable as collateral) present lower risk for the protocol.** Collateral are the assets of the protocol. To remain solvent, the value of these assets must remain greater than the value of the assets borrowed . Assets which can only be used for borrowing should always be excessively backed by other collateralized assets.
5. **Having volume from a wide range of supported assets in lending pools reduces risk via diversification benefits.**

When adding an asset to the Bonzo Finance protocol, significant controls are required to ensure the asset will add more value than risk. Only assets associated with long-term worthy projects, which have significant community support, are considered. The asset risk methodology framework explores whether an asset represents a reasonable amount of risk for the protocol, while calibrating the asset's risk parameters to mitigate those risks.

In the context of the Hedera ecosystem, Bonzo Finance must also consider the unique characteristics of the network and its tokens issued via the Hedera Token Service (HTS). These assets, native to the Hedera network, have different risk profiles compared to EVM ERC-20 smart contract based tokens typical of other networks. The asset risk methodology framework carefully evaluates risk associated with each HTS token prior to its integration into the protocol.

The high throughput and low latency of the Hedera network may impact the way currency risks are assessed and managed, relative to operations on alternative networks. Bonzo Finance took these factors into account when designing asset risk quantification criterion and configuring asset risk parameters.
