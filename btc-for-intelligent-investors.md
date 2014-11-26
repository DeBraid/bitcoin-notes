*********************************************
Bitcoin White Paper for Intelligent Investors
*********************************************

Much of this is taken from the paper, it is highly opinionated.  Consider this an annotated version of the white paper. 

## Abstract 

Electronic cash for online payments is possible without financial institutions.  

Digital signatures combined with a peer-to-peer network provides a novel solution to a 40+ year old problem in computer science. A network of transactions forms chain --  the *blockchain* -- which is maintained such that the longest chain with the most consensus (CPU power) is the de facto account balance, or in bitcoin language the *ledger*. 

> The longest chain not only serves as proof of the sequence of events witnessed, 
> but proof that it came from the largest pool of CPU power.

The network is incentives to work hard to earn BTC (and thus invest CPU power), since the quality and security of the distributed ledger is directly proprotional to their particpation in the mining (provision of marginal CPU power);


#### 51% Attack 

>As long as a majority of CPU power is controlled by nodes that are not cooperating to attack the network, they'll generate the longest chain and outpace attackers.

First, this is the major assumption in the abstract!  So a vital point for bitcoin.  Second, what an awful sentence!  The downside of secrecy is that the editing process is absent.  How about: 

If the network is sufficiently diverse, then it is safe from malicious attackers.  The cost to hi-jack the network would in theory exceed the value of the coins.  CPU power remains distributed 

>The network itself requires minimal structure. Messages are broadcast on a best effort basis, and nodes can leave and rejoin the network at will, accepting the longest proof-of-work chain as proof of what happened while they were gone.

The trust, is that is you aren't actively mining (and thus making some marginal attempt at verifying the blockchain independently), then you can re-join and take the blockchain provided as gospel. 


## Introduction 

Banks and FI's are the pillars of modern financial system.  The element of trust required to transact in the modern economy is a major drawback of the current system.

This trust is costly in many ways.  The entirety of credit card, AML and fraud prevention for banks is $50-100 billion per year conservatively.  This is the 'vig'
 upon which FI's collect or acting as trusted third-party to financial transactions. 

However, with the advent of bitcoin, the requirement for third parties can be wholly, or at worst significantly, eliminated. 

Financial institutions mediate disputes between transacting parties, the result is that transactions are reversible.  The possibility of reversing a transaction necessitates trust, where merchants and customers battle to provide as little info as possible while still quickly completing a digital transaction, and fraud is accepted as being unavoidable. 

### Bitcoin is an electronic payment system based on cryptographic proof *instead of* trust.   

The major premise of the paper:

> We propose a solution to the double-spending problem using a peer-to-peer distributed timestamp server to generate computational proof of the chronological order of transactions. 

Transactions are too costly to reverse (protecting sellers from fraud) and buyers can be protected by 'routine escrow mechanisms'.

> The system is secure as long as honest nodes collectively control more CPU power than any cooperating group of attacker nodes.

## Transactions

#### An electronic coin is a chain of digital signatures. 

A block hash is combined with a public key (wallet of recipient) and private key (proof of ownership of coins by payee).

The private key 'signs' the transaction, while the public keys (wallet and block hash) verify that coins exist, and have not been double-spent.

> To accomplish this without a trusted party, transactions must be publicly announced, and we need a system for participants to agree on a single history of the order in which they were received. 

## Timestamp server

Solution: take a hash of a block of items to be timestamped and widely publish them.  The timestamp proves the existence of a transaction, with each transaction chained to next, reinforcing ones before it.

## Proof-of-Work

To implement a distributed timestamp server on P2P basis, we use proof of work (like Adam Backs Hash Cash).  

> The proof-of-work involves scanning for a value that when hashed, such as with SHA-256, the hash begins with a number of zero bits. The average work required is exponential in the number of zero bits required and can be verified by executing a single hash.

Like interpreting that, mining bitcoins is very diffcult (finding the solution to the problem).  However, verifying the existence of a valid solution is very easy.  

Once the CPU effort has been put forth to make it satisfy the proof of work, the block cannot be changed without re-doing the work.  As the chain grows, so expands the amount of work required to solve each block.

### Proof of work is essentially one CPU one vote.

The blockchain is the majority decision repsenting the longest chain, which by design has the most proof of work effort in it.

To modify the past, or hack the blockchain, a hacker would need to re-do all the previous work, and keep up with on-going work, in order to beat the combined effort fo the honest CPU nodes.

Hence the desire for those involved in bitcoin to stay away from alt coins.  They fragment the CPU power and diminish the adoption efforts of cryptocurrencies broadly by drawing resources that would otherwise be allocated to the prime mover -- bitcoin. 

> To compensate for increasing hardware speed and varying interest in running nodes over time, the proof-of-work difficulty is determined by a moving average targeting an average number of blocks per hour. If they're generated too fast, the difficulty increases.

## Network

Run the network as follows: 

### Transact - broadcast - collect -- proof of work - acceptance

1.  New transactions are broadcast to all nodes.
2.  Each node collects new transactions into a block
3.  Each node works on finding a difficult proof-of-work for its block. 
4.  When a node finds a proof-of-work, it broadcasts the block to all nodes.
5.  Nodes accept the block only if all transactions in it are valid and not already spent.
6.  Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.


The longest chain is considered to the be the correct one.  Nodes work to extend the longest chain, by mining and accepting the transactions, then adding them as a new block to the chain.

In case of a tie, two blocks are held, the winner is whichever chain finished the next block first, thus creating a new longest chain. 

## Incentive 

The first transaction in a block is special, this is by design, since a new coin is owned by the creator of the block.  This is done for two reasons: 

1.  no central authority to *issue* coins, rather they get distributed on the basis of allocation of resources: CPU time and electricity.
2.  creates direct incentive for nodes to support the network (mining = earning bitcoin)

"If the output value of a transaction is less than its input value, the difference is a transaction fee that is added to the incentive value of the block containing the transaction."

if [ Output ( bitcoin value ) ] < [ input ( CPU + electricity ) ] , then transaction fees compensate. 

output - input = fees (*check this*)

Transaction fees can be implemented to create incentive to support the network but generating a spread between market value and capex for coin production.

These incentives are explicitly designed encourage honest behaviour amongst nodes.

A greedy attacker -- assuming the CPU power to overtake the network -- would have to choose between stealing back his payments, or using it generate new coins.

"He ought to find it more profitable to play by the rules" since such rules make it obvious to choose new coins, rather than directly undermine the value that which is attempting to be stolen.

It's like the man who runs a wildly-popular local brewery.  Everyone around agrees the beer is delicious and he has a line of paying customers 24/7.  He could keep all his delicious beer for himself, but in the process he would devolve into a drunkard, directly harming the quality of the beer, and hurting the overall community surrounding his product!

Much like BTC protocol that kind of mutually assured destruction is by design.  Like the drunken brewer, the attacking miner ought to find it in his interest to play by the rules.

This is another example of the genius of Satoshi, and bitcoin.  There are several clever, ingenious and outright brilliant logical, mathematical and scientific elements to bitcoin, not a single feature that makes it suitable for digital money.

## Reclaiming Disk Space

"Once the latest transaction in a coin is buried under enough blocks, the spent transactions before it can be discarded to save disk space."

Anticipating that the size of the chain would outgrow the CPU power of lesser machines, Satoshi contrived a method for storing old transactions ("hashed in a Merkle Tree" where roots are kept and branches discarded). 

(Image)
A block contains the following: 

1.  block header (which contains previous Hash, nonce, and a root hash)
2.  transaction records/hashes (when combined for the root hash w/in block header)

"A block header with no transactions would be about 80 bytes. If we suppose blocks are generated every 10 minutes, 80 bytes * 6 * 24 * 365 = 4.2MB per year. With computer systems typically selling with 2GB of RAM as of 2008, and Moore's Law predicting current growth of 1.2GB per year, storage should not be a problem even if the block headers must be kept in memory.

## Simplified Payment Verification 

First mention of payments!  Satoshi diligently laid out the architecture of bitcoin prior to getting to the juiciest part, the mark of a true scientist! 

Payments can be verified by users simple by querying the network to obtain the longest proof-of-work chain.  A user needn't run a full network node to verify payments,  since the network has accepted this chain. 

The downside of this approach is that a user lacking full transaction record and cannot recreate it independently.  This creates a vulnerability that is avoided by alerts being broadcast whenever suspcious activity (invalid or fraudlent block), is found in place of a previous hashed/pruned block.

Once alerted, the user would then be prompted to download the FULL transaction record and can "confirm the inconsistency".  

"Businesses that receive frequent payments will probably still want to run their own nodes for more independent security and quicker verification."

Interesting to note that trustless money may require some extra work from those who are most heavily invested in the system.  This alignment of incentive structures is a master stroke.  In theory systemic risk that global financial markets are fraught with can be mitigated by the underlying features of bitcoin.   

## Combining and Splitting Value

Transactions contain multiple inputs and outputs.  There are at most two outputs: one for the payment, another returning the change.  Inputs can take various forms, normally a large sum is presented as a single input or multiple inputs of smaller amounts are combined.

## Privacy 

Financial institutions are responsible for privacy in modern banking.  We have seen countless attacks result in the publication of sensitive personal information, sufficient to assume that (my words, not Satoshi): EVERYTHING DITIGAL IS PUBLIC!

Motivated attackers can obtain 99.999% of information stored as bits and bytes regardless of the efforts put in place to stop it.  Computer security is like building the perfect Ebola suit to wear for your kissing competition.  If you keep everybody out, you can't participate, but as soon as you open up a crack, you've already lost the game!

If you think bitcoin is paradoxical, we agree.  How can a network that must broadcast every transaction possibly be anonymous? Despite this feature, bitcoin does provide improved privacy vs. trusted third parties by using private keys.

"Privacy can still be maintained by breaking the flow of information in another place: by keeping public keys anonymous.  The public can see that someone is sending an amount to someone else, but without information linking the transaction to anyone."

Like a stock exchange, the time and size of a transaction is widely known, via the tape, but parties to the transaction are kept secret. 

Privacy Models ( where | is private, -> is shared )

Traditional: ID -> Transactions -> Trusted 3rd party -> Counterparty | Public
Bitcoin: ID | Transactions -> Public

Recommended that a new key pair should be used for each transaction.  It is possible to link transactions to a common owner with multi-input transactions.  If the owner of the key is revealed, it can be deduced that they own all other coins linking to a given transaction. 

## Calculations 



















