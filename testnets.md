# 🦛 Testnets

## Westend

> The goal of Westend is to be a staging environment for Polkadot and Kusama.

Westend is mainly used as part of the release cycle for Parity. The release team deploys new runtimes and node binaries to Westend to test if everything is running as intended.

On top of this, developers at Parity test new functionality by deploying first to Westend as well (like nomination pools).

## Rococo

> The goal of Rococo is to be the parachain testnet environment.

Rococo is a network that was created to test the parachain code. Since the very beginning it was the place where all ecosystem parachains could deploy their code and test the parachain functionality. With XCM live, it is now also a place where teams test cross-chain messaging. As a community testing network, Rococo is being managed without it breaking.

Rococo has a pallet, `assigned_slots` pallet, which is responsible of distributing the duration of slots between teams. As long as a team has a paracahain on Polkadot and/or Kusama, they are entitled to have a parachain on Rococo; these are called `long-term slots`. For teams that don’t have a production parachain, they can get a `short-term slot`, which is 3 days long.

Although being a Parachain focused testnet, the onboarding of parachains is completely manual (issues on [GitHub - paritytech/subport: Parity Substrate(-based) chains usage and development support](http://github.com/paritytech/subport)), and there is no support for crowdloans and auctions (pallets are there, but not being used). Also, Rococo is a completely POA chain where staking and nominating can’t be tested.

**👉🏻 To get testnet tokens for Westend or Rococo please see**

[Polkadot Faucet](./tech-tools/polkadot-faucet.md)
