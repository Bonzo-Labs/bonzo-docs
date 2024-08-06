# Adding an Asset

Bonzo Finance enables users to deposit and borrow digital currencies through the pooling of funds. Depositors receive protocol-issued bTokens, which accumulate deposits and the interest generated. Each loan is secured by collateral acting as a risk mitigation tool against default. As the means of exchange, currencies are central in Bonzo Finance's non-custodial lending operations. More details on how the protocol works can be found in Bonzo Finance's [documentation](https://docs.bonzo.finance).

Given the specificities of Bonzo Finance's model the selection of currencies has been performed with the following constraints:

1. **Each additional currency will slightly increase the gas cost of the borrow and redeem actions permanently on the Hedera network.** The currency must be included in the smart contract, adding complexity and thus costs.
2. **Each currency added to the Bonzo Finance protocol as collateral increases the protocol risk of insolvency.** From a financial perspective, the assets of Bonzo Finance are the collaterals, while the liabilities are the loaned amounts. The underlying currencies of assets and liabilities often differ, with loans mostly taken in stablecoins and backed by volatile tokens. This means the protocol is heavily exposed to the failure of supported token systems as well as market fluctuations.
3. **A centralized currency accepted as collateral exposes the protocol to its centralization risk.** The single point of failure risks of underlying currencies flow into the Bonzo Finance protocol.
4. **Currencies only enabled for depositing and borrowing (not usable as collaterals) present lower risk for the protocol.** Collaterals are the assets of the protocol. To remain solvent, these assets must remain greater than the liabilities (loans). Currencies which can only be used for borrowing should always be excessively backed by other currencies as the collaterals.
5. **Having volume from different currencies in the lending pools reduces risks via diversification benefits.**

When adding a currency to the Bonzo Finance protocol, significant controls are required to ensure the currency will add more value than risk. Only currencies with a worthy product and significant community are considered. The currency risk assessment explores whether the currencies represent a reasonable amount of risk for the protocol, calibrating the currency parameters to mitigate those risks.

In the context of the Hedera ecosystem, Bonzo Finance must also consider the unique characteristics of the network and its native tokens. Hedera Token Service (HTS) tokens, which are native to the Hedera network, may have different risk profiles compared to EVM ERC-20 smart contract based tokens from other networks. Bonzo Finance carefully evaluates the risks associated with each HTS token before integrating it into the protocol.

Furthermore, the high throughput and low latency of the Hedera network may impact the way currency risks are assessed and managed. Bonzo Finance takes these factors into account when designing risk mitigation strategies and setting currency parameters.

By adhering to these constraints and conducting thorough risk assessments, Bonzo Finance aims to create a secure and reliable lending and borrowing environment for users within the Hedera ecosystem, while minimizing the protocol's exposure to various types of currency-related risks.
