# NuCypher

A proxy re-encryption network to empower privacy in decentralized systems.

The NuCypher network facilitates end-to-end encrypted data sharing for distributed apps and protocols. Access permissions are baked into the underlying encryption, and access can only be explicitly granted by the data owner via sharing policies. Consequently, the data owner has ultimate control over access to their data. At no point is the data decrypted nor can the underlying private keys be determined by the NuCypher network.

Under the hood, the NuCypher network uses the [Umbral](https://github.com/nucypher/pyUmbral) threshold proxy re-encryption scheme to provide cryptographic access control.

## Features

-   Feature
-   Feature

## Prizes Offered

1.
2.

## Getting Started

### Ursula

#### Install Nucypher

```shell
pip3 install -U nucypher
```

#### Run a Federated-Only Development Ursula

```shell
nucypher ursula run --dev --federated-only
```

#### Configure a Persistent Ursula

```shell
nucypher ursula init --federated-only
```

#### Run a Persistent Ursula

```shell
nucypher ursula run --network <NETWORK_DOMAIN> --teacher-uri <SEEDNODE_URI> --federated-only
```

Replace `<NETWORK_DOMAIN>` with the network domain and `<SEEDNODE_URI>` with the URI of a node running on that network domain you want to connect to (for example 0.0.0.0:9151 or 0xdeadbeef@0.0.0.0:9151).

If you’re connecting to the `devnet`, you should use `--network devnet --teacher-uri 18.222.119.242:9151`.

#### Run a Geth-Connected Development Ursula

Run a local geth node in development mode:

```shell
geth --dev
```

Run a local development Ursula connected to the geth node

```shell
nucypher ursula run --dev --provider-uri ipc:///tmp/geth.ipc --checksum-address <GETH_DEV_ADDRESS>
```

Replace `<GETH_DEV_ADDRESS>` with the geth node’s public checksum address.

## Need Help?

-   [Full documentation](https://docs.nucypher.com/en/latest/guides/quickstart.html)
-   [Discord chat](https://discord.gg/7rmXa3S)
