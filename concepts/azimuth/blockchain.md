+++
title = "Why Urbit Uses a Blockchain"
weight = 1
template = "doc.html"
+++
The Arvo network is composed of personal servers: instances of the Arvo operating system, called ships,
that communicate as peers.

Every ship has an associated secure identity, called a point, that it needs
to connect to the network. Your point is your name and your network address.
Each point has associated authentication and encryption keys for networking.
Think of a point as an IP address, a domain name, and a PGP key-pair.

There are a limited number of points and, as you might expect, scarcity gives
points value. This means that bad actors – spammers, scammers, and malware-spreaders – can be made economically unviable. Points being
immutable allows for reputation systems to be built on top,
keeping the network friendly and giving users information to help them decide
who to treat as a trusted peer.

At the user level, having one identity for your digital life means that all the
services that you trust recognize you. You no longer need to worry about
managing dozens of different logins. When you're using Arvo, everything you do
is "verified" in the sense that it links back to your point.

But wait! We need some way to secure these identities. To that end, we have
built a public-key infrastructure (PKI) called _Azimuth_ on the Ethereum
blockchain. Azimuth acts as a decentralized ledger for points: it determines
which Ethereum addresses own which points. It's separate from and parallel to
the Arvo network.

In theory, our ecosystem doesn't need a blockchain, because Urbit identities are
more like real estate than currency: they change hands slowly. A low-friction,
zero-trust solution to the double-spend problem isn't an economic necessity for
transactions such as ours. So we could have the Arvo network run its own
key-signing system. But, since Azimuth identities are valuable, you don't want
to put them in an self-hosted PKI that isn't generally recognized as secure.
Arvo is still young, we'd prefer to use an existing system for people to secure
their property.

Moving the Urbit land registry to Ethereum is an easy and obvious solution to
this problem. We chose Ethereum over Bitcoin because the former is built for
computation Landscape the latter is not. We need a computational blockchain to
enforce the specific rules of the Urbit identity registry.

For more background on the decision to use the Ethereum blockchain, check out
[these](https://urbit.org/posts/essays/urbit-and-the-blockchain/)
[two](https://urbit.org/posts/essays/bootstrapping-urbit-from-ethereum/) posts.
