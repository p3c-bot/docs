+++
title = "Azimuth"
weight = 6
sort_by = "weight"
template = "sections/docs/chapters.html"
+++
Azimuth is a general-purpose public-key infrastructure (PKI) on the Ethereum blockchain, used as a platform for Urbit identities that we call _points_. You need a point to use the Arvo network.

The primary way to interact with Azimuth is through our [Bridge](https://github.com/urbit/bridge) application and the node libraries that it depends on, azimuth-js and keygen-js. Take a look at the source and play around or see [Getting Started](/docs/getting-started).

## Arvo vs. Azimuth

Urbit is a project, not a single computer system. It has three components: Arvo, the operating system; Azimuth, the identity system; and Aegean, the pattern for creating software experiences for individual Urbit communities. Let's compare the first two.

**Arvo** is an operating system that provides the software for a personal server. These personal servers together constitute the peer-to-peer Arvo network. To make this network work on the social level, Arvo is built to work with a system of scarce and immutable identities.

**Azimuth** is the public-key infrastructure built to be such a system. A suite of smart-contracts on the Ethereum blockchain, Azimuth determines which Ethereum addresses own which Azimuth identities, called _points_. All point-related operations, such as transfers, are governed at this layer. But Azimuth isn't built strictly for Arvo -- it could be used as a generalized identity system for other projects.

These otherwise-parallel systems meet when you want to connect to the Arvo network. Your Arvo personal server, called your _ship_, needs to be able to prove cryptographically that it is who it says it is. This proof comes in the form of a keyfile, derived from your point, that you use to start your ship.

A metaphor might help illustrate the relationship between these two systems: the Arvo network is the neighborhood that you live in; Azimuth is the bank vault that stores the deed to your house.
