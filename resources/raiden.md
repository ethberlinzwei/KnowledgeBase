# [Raiden](https://developer.raiden.network/)

The [Raiden Network](https://raiden.network/) is an off-chain scaling solution, enabling low-fee and scalable payments. Raiden leverages payment channel technology, is complementary to Ethereum and works with any ERC20 token. 

A network of payment channels allows to securely transfer value off-chain, i.e without involving the blockchain for every transfer. Not involving the blockchain for every transfer helps avoiding the blockchain consensus bottleneck and makes transfers faster and cheaper.

A payment channel in Raiden is always backed by an on-chain deposit of tokens. When making a payment, the sender signs a balance proof to the respective receiver.

Raiden lets users pay anyone in the network by using a path of connected payment channels to mediate the payment.

## Resources 

- [Raiden Documentation](https://raiden-network.readthedocs.io/en/stable/index.html)
- [Developer Portal](https://developer.raiden.network/)
- [Raiden Code](https://github.com/raiden-network/raiden)
- [Raiden Network 101](https://raiden.network/101.html)
- [Raiden Blog](https://medium.com/raiden-network)
- [Awesome Raiden](https://github.com/raiden-network/awesome-raiden)

## Features

- Payment channel network for off-chain token transfers
- Token networks can be created for any ERC20 compliant token
- Direct transfers (with channel partners) 
- Mediated transfers via a path of connected nodes without the need of opening a channel with recipients directly

Supporting features/products:
- 🧙 **[Raiden Wizard](https://github.com/raiden-network/raiden-installer)**: On-boarding tool for quick installation and launch of Raiden (exclusively on Görli testnet)
- 🔮 **[Raiden Services](https://github.com/raiden-network/raiden-services)**: Pathfinding services (PFS) for better routing & monitoring services (MS) to allow nodes to go offline safely
- 🖥️ **[Raiden WebUI](https://github.com/raiden-network/webui)**: Web user-interface to interact with Raiden's API
- 📲 **[Raiden Light Client](https://github.com/raiden-network/light-client)**: A Raiden Network compatible client written in JavaScript/Typescript, capable of running in modern web3-enabled browsers, wallets and Node.js environments and  a first reference front-end implementation (both WIP!)


## Prizes Offered

- **👨‍💻 [Raiden User Experience Challenge](https://github.com/ethberlinzwei/Bounties/issues/9)**
- **💸 [Raiden Micropayments Challenge](https://github.com/ethberlinzwei/Bounties/issues/8)**
- **🤖 [Raiden IoT Challenge](https://github.com/ethberlinzwei/Bounties/issues/7)**

## Getting Started

If you want to hack on Raiden during ETHBerlinZwei, please use the latest testnet Raiden release: [v0.100.5a0 (Antifragile Crocodile)](https://github.com/raiden-network/raiden/releases/tag/v0.100.5a0).

Make sure you have read the [requirements for safe usage](https://raiden-network.readthedocs.io/en/stable/overview_and_guide.html#requirements-for-safe-usage) before proceeding. 

The easiest way to install and launch a Raiden node is using the [Raiden Wizard](https://medium.com/raiden-network/introducing-the-raiden-wizard-6c7c61c5b695). You can download the Raiden Wizard [here](https://github.com/raiden-network/raiden-installer/releases). 

Alternatively, you can manually install and launch Raiden:

0. Layer 1 required! You'll need a local (testnet) Ethereum node, either geth or parity, that is always synced and working reliably.
1. Download the Raiden Binaries for Linux or MacOS [here](https://github.com/raiden-network/raiden/releases/tag/v0.100.5a0).
2. Follow the [instructions](https://raiden-network.readthedocs.io/en/latest/overview_and_guide.html) to fire up Raiden. 
3. To start Raiden you need to provide a valid pathfinding service address. There are pathfinding services running on every testnet at the moment, some that charge fees and some that are for free. For Görli testnet the addresses are: PFS with fees --> https://pfs-goerli-with-fee.services-dev.raiden.network and PFS without fees --> https://pfs-goerli.services-dev.raiden.network

Here is an example:

```
raiden --keystore-path  ~/.ethereum/testnet/keystore --eth-rpc-endpoint "https://goerli.infura.io/v3/<yourToken>" --pathfinding-service-address "https://pfs-goerli.services-dev.raiden.network"
```

## Need Help?

For any technical questions or problems you can reach us via [Gitter](https://gitter.im/raiden-network/raiden) or on-site at the **ETHBerlin Layer 2 helpdesk**! 

To stay up to date about our bounties during the hackathon, follow our [updates on Twitter](https://twitter.com/raiden_network). 
