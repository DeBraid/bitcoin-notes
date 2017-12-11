# Lightning Network

via https://lightning.network/lightning-network-paper.pdf

# Abstract

> The bitcoin protocol can encompass the global financial transaction volume in all electronic payment systems today, without a single custodial third party holding funds or requiring participants to have anything more than a computer using a broadband connection.

Posit: Lightning can make bitcoin scale using existing modern technology.

## micropayment channels

Off-blockchain, decentralized, payment channels can be used to transfer value.  This requires a new _sighash type_.

> A decentralized system is proposed whereby transactions are sent over a network of micropayment channels (a.k.a. payment channels or transaction channels) whose transfer of value occurs off-blockchain. If Bitcoin transactions can be signed with a new sighash type that addresses malleability, these transfers may occur between untrusted parties along the transfer route by contracts which, in the event of uncooperative or hostile participants, are enforceable via broadcast over the bitcoin blockchain in the event of uncooperative or hostile participants, through a series of decrementing timelocks.

* Sounds like a first-class transaction type.  Is this a new UTXO set (a new coin? or a modification to the existing UTXO?)
* a series of decrementing timelocks (callbacks to the main chain) ensure security of the micropayment channels

# The Bitcoin Blockchain Scalability Problem

Bitcoin cannot support the current transaction volume of the global eCommerce system because it broadcasts the current state of the ledger to ALL participant.  This security feature present scaling challenges.

### Visa Case Study

Visa has done ~47k transactions per second (tps) at peak load.  Given 1MB blocks, bitcoin can do ~7 tps at in 2016.

To reach par with VISA, bitcoin would need 8GB blocks and process 400 terabytes per year!

### Who cares?

If only the most powerful machines can process all this data, then centralization is likely to occur.

> Having fewer validators due to larger blocks not only implies fewer
individuals ensuring ledger accuracy, but also results in fewer entities that
would be able to validate the blockchain as part of the mining process,
which results in encouraging miner centralization.

Decentralized systems can avoid use of custodians and significantly reduce counterparty risk.  Off-chain transactions are required to allow bitcoin to scale.

# A Network of Micropayment Channels Can Solve Scalability

> It is preferable to only have the bare minimum of information on the blockchain.

Payment channels can reduce the overall volume of transaction data by time-locking and bundling transaction between two trusting parties.

> By deferring telling the entire world about every transaction, doing net settlement
of their relationship at a later date enables Bitcoin users to conduct many
transactions without bloating up the blockchain or creating trust in a centralized
counterparty.

* this sure sounds like trust to me... "net settlement of their relationship at a later date"

> These channels are not a separate trusted network on top of bitcoin. They are real bitcoin transactions.

This scheme sounds much like what "smart contracts" are described as.  A more complex agreement then buy/sell, in the case of payment channels, the introduction of time/escrow(?).

> Micropayment channels[3][4] create a relationship between two parties to perpetually update balances, deferring what is broadcast to the blockchain in a single transaction netting out the total balance between those two parties.


# Micropayment Channels Do Not Require Trust

Both parties can commit to signing a transaction and not broadcasting this transaction.  Using mutli-sig address that requires consent from both parties balances can be updated at will on a later date.  This is known by tracking current correct balance and previous deprecated balances.

> The balance is reflected on the blockchain only when a single party disagrees.

If both parties agree, then the payment channel can continue to defer broadcasting.  Dispute among transacting parties in a channel will spawn a callback transaction.

> Conceptually, this system is not an independent overlay network; it is more a deferral of state on the current system, as the enforcement is still occurring on the blockchain itself (albeit deferred to future dates and transactions).












