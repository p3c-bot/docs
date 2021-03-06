+++
title = "The Urbit HD Wallet"
weight = 2
template = "doc.html"
+++
Owners of Azimuth _points_ need safeguards that allow for the use of Urbit
without jeopardizing cryptographic ownership of their assets. Toward this end,
we created the **Urbit Hierarchical Deterministic (HD) Wallet** for the storage of
points. The Urbit HD Wallet is not one key-pair, but a system of related
key-pairs that each have distinct powers, from setting networking keys for
communicating in the Arvo network to transferring ownership of points.

The Urbit HD Wallet's derivation paths have a hierarchical structure, so
that keys with different powers can be physically separated. A \"master ticket"
can re-derive the entire wallet in case of loss. The encryption and
authentication keys that points ships use to sign messages within the network
are also derived from the wallet.

Urbit HD wallets are composed of the following items, which are each assigned to
their own individual Ethereum key-pairs.

#### Master Ticket

Think of your master ticket like a very high-value password. The master ticket
is the secret code from which all of your other keys are derived. Technically,
your master ticket is seed entropy. You should never share it with anyone, and
store it very securely. This ticket can derive all of your other keys: your
ownership key and all of the related proxies.

#### Ownership Address

An ownership address has all rights over the assets deeded to it. These rights
are on-chain actions described and implemented in the Ecliptic, Azimuth's suite
of governing smart-contracts.

#### Proxies

Proxy addresses allow you to execute non-ownership related actions like spawning
child points, voting, and setting networking keys without jeopardizing the keys
you've designated with ownership rights. Setting proxy rights is optional, but
it is recommended for on-chain actions you will execute more frequently.

- **Management Proxy**

  Can configure or set Arvo networking keys and conduct sponsorship related
  operations.

- **Voting Proxy**

  Galaxies only. Galaxies are the part of the galactic senate, and this means
  they can cast votes on new proposals including changes to the Ecliptic.

- **Spawn Proxy**

  For stars and galaxies only. Can create new child points.

![](https://media.urbit.org/fora/proposals/UP-8.jpg)


Most Ethereum tokens use the ERC-20 standard for smart contracts. Azimuth points
are, however, essentially different from most Ethereum tokens, due to points not
being fungible. Since any two stars will handle social-networking realities in a
different way, they will carry a different reputation. Points are to houses as
tokens are to gold.

The ERC-721 standard, having been made specifically to provide a smart-contract
interface for non-fungible assets, serves our needs well. This is the standard
that we use for deeding Azimuth points.

Points, and all of their blockchain operations, are governed by the Ecliptic.
The Ecliptic is an Ethereum smart-contract that governs point state and the
ownership, spawn, management, and voting rights affiliated with your points.

For the technical implementation details Azimuth, take a look at the
[Github repo](https://github.com/urbit/azimuth).
