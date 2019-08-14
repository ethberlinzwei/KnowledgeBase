# [go-ethereum](https://geth.ethereum.org)

Go-ethereum (or Geth for short) is one of the most widely used client implementations of the Ethereum protocol, it's written in Go.

## Features

- Dev mode. Run a private network with an account already having a practically infinite amount of ether. 
- GraphQL to query a local node.  Start geth with `geth --graphql`, then point your browser to http://localhost:8547 where you can enter and execute GraphQL queries.
- Puppeth to manage a private network. See `puppeth -h` after you installed Geth.
- [Clef](https://geth.ethereum.org/clef/Overview) to sign transactions in a secure way, independently from the cllient's account management.
- [Tracing](https://geth.ethereum.org/developers/Tracing_Introduction)

## Getting Started

[Install Geth](https://geth.ethereum.org/install-and-build/Installing-Geth). Then you have two easy options

1. Sync with a testnet running `geth --goerli --syncmode "light"`
2. Or run your private network `geth --dev`. It will create a new account (if none exists), and put a lot of ether on it.

You can interact with Geth in a number of ways:

- [JavaScript console](https://geth.ethereum.org/interface/JavaScript-Console) if you run `geth attach` in another terminal.
- Using a graphql client at the http://localhost:8547/graphql endpoint if you started geth with `geth --graphql`.
- With the standard [JSON RPC AP](https://github.com/ethereum/wiki/wiki/JSON-RPC) if you started geth with `geth --rpc`.


## Need Help

- [Public Discord channel](https://discord.gg/nthXNEv)
- [Read the docs](https://geth.ethereum.org/docs/)
- [Use the source, Luke](https://github.com/ethereum/go-ethereum)

