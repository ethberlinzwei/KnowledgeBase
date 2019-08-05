# libp2p

[libp2p](https://libp2p.io) is a modular framework and protocol suite for
developing peer-to-peer applications. Originally part of the [IPFS
project](https://ipfs.io), libp2p has evolved to meet the needs of a growing
community of developers and users, and has recently been incorporated into the
[networking spec for Ethereum
2.0](https://github.com/ethereum/eth2.0-specs/blob/dev/specs/networking/p2p-interface.md).

There are many implementations of libp2p, with
[go-libp2p](https://github.com/libp2p/go-libp2p) being the oldest and most
"feature complete". Javascripters can use
[js-libp2p](https://github.com/libp2p/js-libp2p) in Node or browsers, and
rustaceans can dig into [rust-libp2p](https://github.com/libp2p/rust-libp2p).

Other language implementations are in developmement, but if your favorite
language isn't quite there yet, the [libp2p
daemon](https://github.com/libp2p/go-libp2p-daemon) allows you to run "libp2p as
a service" in an external process. Check out the supported [language
bindings](https://github.com/libp2p/go-libp2p-daemon#language-bindings) to see
if there's already a binding for your language.

## Features

-   Ensures secure, multiplexed streams between connected peers. Security and
    multiplexing protocols are modular, and peers can negotiate supported
    configurations.
-   Pluggable transport modules allow support for TCP, WebSockets, QUIC & WebRTC
    (if supported by the language / runtime). Nodes can support multiple
    transports for interop / network flexibility.
-   Kademlia-like DHT provides peer routing (to lookup network addresses by peer
    id), content routing (to look up content / service providers by hash key),
    and a public key lookup service.
-   Extensible PubSub protocol allows broadcast messaging to peers that are
    subscribed to a topic.
-   Can automatically traverse (some) consumer NATs using UPnP.
-   Local peer discovery using mDNS.
-   Circuit relay protocol allows peers behind NAT boundaries to communicate,
    using a relay node as intermediary.

## Prizes Offered

1\.
2\.

## Getting Started

Some background info that may be helpful:

- The Eth 2.0 [p2p networking
  spec](https://github.com/ethereum/eth2.0-specs/blob/dev/specs/networking/p2p-interface.md)
  details how Eth 2 will use libp2p for both testnet and mainnet configurations.

- Peer identity is [based on public keys](https://github.com/libp2p/specs/blob/master/peer-ids/peer-ids.md), so starting a node requires generating
  a keypair or loading one from disk. 
  - [secp256k1 keypairs are recommended](https://github.com/ethereum/eth2.0-specs/blob/dev/specs/networking/p2p-interface.md#interop-1)
    
- The core abstraction for communication between peers is the Stream - a
  reliable, ordered channel that's multiplexed over some transport connection.
  Streams are cheap to open once the initial connection is made, so it's okay to
  open a new stream for a quick request/reply sequence.
  - See [The Req/Resp
    Domain](https://github.com/ethereum/eth2.0-specs/blob/dev/specs/networking/p2p-interface.md#the-reqresp-domain)
    for protocol ids, framing logic, etc used in eth 2.0 request / response protocols.
  
- Network addresses are encoded as
  [multiaddrs](https://github.com/multiformats/multiaddr). There's a [draft spec
  in progress](https://github.com/libp2p/specs/pull/191) that has some detail
  about valid multiaddr constructions.

- The Eth 2 testnet and mainnet will use discv5 to advertise peers in each
  pubsub topic. For local development and testing, you'll need to use some other
  peer discovery mechanism.
  
- mDNS discovery will return _all_ nearby libp2p peers that are using mDNS, so
  if you use it at a hackathon, don't be surprised if you discover a bunch of
  peers that don't speak your custom protocol and error out when you try to dial
  them.


## Need Help

The [libp2p docs site](https://docs.libp2p.io) is a work in progress, but has
some useful info. The [concepts section](https://docs.libp2p.io/concepts/) is
especially helpful if you're new to libp2p. There are also quick tutorials for
[go-libp2](https://docs.libp2p.io/tutorials/getting-started/go/) and
[js-libp2p](https://docs.libp2p.io/tutorials/getting-started/javascript/).

Code examples:

- [go](https://github.com/libp2p/go-libp2p-examples)
- [js](https://github.com/libp2p/js-libp2p/tree/master/examples)
- [rust](https://github.com/libp2p/rust-libp2p/tree/master/examples)

Detailed specs are available in the [specs
repository](https://github.com/libp2p/specs) for most core libp2p wire
protocols and abstractions.

Check out the [libp2p discussion forums](https://discuss.libp2p.io) to ask
questions & find out about new developments in libp2p. Tagging Stack Overflow
questions with `libp2p` is also a good way to get them seen by people in the
community. The `#libp2p` IRC channel on freenode can also be a good venue for a
quick question.
