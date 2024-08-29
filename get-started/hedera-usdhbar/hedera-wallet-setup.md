---
description: Setting up a Hedera wallet that's compatible with the Bonzo Finance protocol.
---

# Hedera Wallet Setup

### HashPack <a href="#hashpack" id="hashpack"></a>

[HashPack](https://www.hashpack.app/) is the leading wallet on the Hedera network. For detailed, step-by-step instructions on setting up your HashPack wallet, visit [How to Create Your First Account with HashPack](https://www.hashpack.app/post/how-to-create-your-first-account-with-hashpack).

* For desktop users, install the HashPack extension from the [Chrome Web Store](https://chrome.google.com/webstore/detail/hashpack/gjagmgiddbbciopjhllkdnddhcglnemk).
* For iOS users, download HashPack from the[ Apple App Store](https://apps.apple.com/us/app/hashpack/id6444389849).
* For Android users, you can find HashPack on the[ Google Play Store](https://play.google.com/store/apps/details?id=app.hashpack.wallet.twa).

### MetaMask <a href="#metamask" id="metamask"></a>

{% hint style="warning" %}
Currently in development. The Bonzo Finance testnet application today only works with the HashPack wallet.
{% endhint %}

[MetaMask](https://metamask.io/) is the most widely-used wallet, allowing users to store ERC-20 tokens on Ethereum-based blockchains, as well as HTS tokens on the Hedera network. For detailed, step-by-step instructions on setting up your MetaMask wallet, visit [Getting started with MetaMask](https://support.metamask.io/hc/en-us/articles/360015489531-Getting-started-with-MetaMask).

* For desktop users, install the MetaMask extension directly from [metamask.io](https://metamask.io/).
* For iOS users, download MetaMask from the[ Apple App Store](https://apps.apple.com/us/app/metamask-blockchain-wallet/id1438144202?\_branch\_match\_id=1235424007731302813&\_branch\_referrer=H4sIAAAAAAAAA8soKSkottLXz00tScxNLM7WSywo0MvJzMvWL8529DB2SnSztAQA5G46IyQAAAA%3D).
* For Android users, you can find MetaMask on the [Google Play Store](https://play.google.com/store/apps/details?id=io.metamask\&hl=en\_US\&ref=producthunt&\_branch\_match\_id=1235424007731302813&\_branch\_referrer=H4sIAAAAAAAAA8soKSkottLXz00tScxNLM7WSywo0MvJzMvWT6ooz3a1yHeztAQA%2FOIqTSQAAAA%3D).

### JSON-RPC

{% hint style="info" %}
When first connecting your MetaMask account to Hedera, you will need to add a JSON-RPC relay to enable communication between MetaMask and Hedera.
{% endhint %}

1. Use [ChainList](https://chainlist.org/chain/295) to add the "Hashio" RPC, operated and maintained as a "community service" by [Hashgraph](https://www.hashgraph.com/).
2. Manually add a network by including the following JSON-RPC information:
   * **Network Name:** Hedera Mainnet
   * **RPC URL:** [https://mainnet.hashio.io/api](https://mainnet.hashio.io/api)
   * **Chain ID:** 295
   * **Currency Symbol:** HBAR
   * **Block Explorer URL:** [https://hashscan.io/mainnet/](https://hashscan.io/mainnet/)
