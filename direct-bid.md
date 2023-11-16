# How to direct bid for a Parachain slot

Assuming you have followed the steps in:

[Setup your chain ](setup-your-chain.md)

A Parathread can be transformed to parachain by winning a parachain slot auction. This guarantees the now parachain will always have their block data hashed and included in the relay chain block (called Proof of Validation, or short for PoV), during the slot duration they are alloted.

Only fully-onboarded parathreads are eligible to bid in a parachain slot auction.

## Relevant Settings

_Some critical setting in the network dependant! These affect timing behavior on some parachain operations, and are subject to change!_

- Session length
- Lease Period Length
- Ending Period
- Current Lease Period Index = Current Block Number / 14400

Note that transitions of a parachain/Parathread into a different state will take at least 2 sessions, including on-boarding, off-boarding, upgrading, downgrading, etc.

Find these settings on the [Polkadot wiki](https://wiki.polkadot.network/docs/learn-crowdloans#starting-a-crowdloan-campaign) and the [source of the runtime](https://github.com/paritytech/polkadot/tree/master/runtime) presently running on your target relay chain. It is _absolutely essential_ that you understand these parameters before you commit to them.

## Direct Bidding

Anyone with a fully onboarded parathread can make a bid to win a parachain slot for their ParaID. They need to out-bid all others participating in the slot auction.

You can do so in Polkadot-JS App [Network -> Parachains -> Auctions](https://polkadot.js.org/apps/#/parachains/auctions) page (make sure you are on the right network).

Pick your ParaID, how much you want to bid, and the slots you want to bid for:
