# Step-by-Step Guide

### Prerequisites

* A Hedera wallet (for example, HashPack) or an EVM wallet (for example, MetaMask) connected to the Bonzo Finance application.
* Native gas on the source chain to initiate the bridge transaction.
* A small amount of native gas on the destination chain for any follow-up transactions (destination delivery gas itself is included in the bridging fee).

### Step-by-Step Instructions

1. Navigate to [app.bonzo.finance/bridge](https://app.bonzo.finance/bridge).
2. Connect wallet (MetaMask or ecosystem wallet via WalletConnect) to the Bonzo Finance application.
3.  Click the **`+Destination`** button to manually input a destination EVM address to receive the bridged asset on your destination chain.

    <div data-gb-custom-block data-tag="hint" data-style="warning" class="hint hint-warning"><p><strong>Please make sure the destination EVM address (whether manually inputted or the same EVM address of the connected account) on the destination chain is valid and accessible.</strong></p></div>
4. Select the source chain and asset you’d like to bridge in the **`From`** section.
5. Select the destination chain and asset you’d like to receive in the **`To`** section.
6. Enter an amount, or use the **`25%`** / **`50%`** / **`MAX`** quick-select buttons.
7. Review the displayed exchange rate and fee details.
8. Click the **`Confirm Bridge Transaction`** button and approve the transaction(s) in your wallet.
9. Track progress in the on-screen modal, including all links to network explorers and LayerZero Scan once bridging completes.
10. Review all previous bridge transactions for your connected account in the **`Recent Transactions`** box, below the bridging box, if applicable.

### Fees and Timing

Bridge fees include a LayerZero / Stargate protocol fee. Source-chain gas is paid by the user as a normal transaction fee.

Typical delivery times are a few minutes. Transfers involving Ethereum mainnet may take slightly longer due to block confirmation times. Exact timing depends on network congestion and the chains involved.

### Safety and Failed Transactions

If a bridge transaction fails, user funds remain safe on the source chain. LayerZero's messaging protocol is designed so that assets are not lost in transit. If an issue occurs, users can:

* Check the transaction status on [LayerZero Scan](https://layerzeroscan.com).
* Open a ticket in the [official Bonzo Finance Discord](https://bonzo.finance/discord) for support.
