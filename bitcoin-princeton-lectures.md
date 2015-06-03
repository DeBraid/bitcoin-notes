# Money and Payment System 
by David Andolfatto VP Research, FRB St. Louis 
### May 01, 2015 - [Video Link][1]

Think of bitcoin as solving a money and payments problem.  Not credit: don't confuse bitcoins with credit systems associated with typical sovereign currencies.  It combines:

#### Monetary Tokens
- record keeping device

#### Ledgers 
- ledgers (aka accounts to keep money secure)

#### Payment System 
- finance needs a set of payment protocols to transfer value from one party to another

#### Monetary policy 
- description of management of the quantity

Bitcoin is a revolution that is a throwback to the past.  Anthropologists noted money doesn't exist in small communities, but memes (memories of actions -- specifically contributions to the tribe -- would form abstract payment systems.  Virtual data on shared or distributed ledger (brains) and communicated through network (gossip).  Tally sticks, etc.) 

Key innovation of bitcoin is to extend our brains to think in computer terms.  Bitcoin is money for the internet (ad @pmarca notes if you could go back in time pre-internet Bitcoin would have been in the design spec for payments since day 1).



Text from Slides: 

Bitcoin
A Decentralized, Public Ledger Digital Asset Transfer Mechanism
David Andolfatto


## Money and Payments System
1. Monetary tokens: record-keeping devices.
2. Ledgers: accounts containing monetary objects.
3. Payment protocols: value transfer mechanisms.
4. Monetary policy: protocol to manage money supply.



Money and Payments System
1. Monetary tokens.

Money and Payments System
2. Secure ledger.

Money and Payments System
3. Payment protocols.

Money and Payments System
4. Monetary policy: managing the supply of marbles.

## Early money and payment systems: Gift-giving economies, social credit systems.

Virtual data (memories) recorded on shared and distributed ledger (communal brains) updated via consensus algorithm (gossip).  Physical coin tokenized this ancient form of social of currency. Invention of coined tokens and precious metals (specie) which may have became required as communities expanding beyond capacity of memory (magic 149 people in a group?).

### Then:
- In 17th C. goldsmith banks issue paper money (receipts)
- 19th C. banknotes redeemable for specie, backed by assets

### Now:
Monetary objects consist of liabilities issued by central and chartered private banks: **physical (cash) and digital objects**.

Much like the old days bank liabilities legally a digital version of 19th C. banknotes.  Cash payment: P2P debit/credit of personal wallets.

## Important distinction on permission
Cash is a permissionless accounts held in invisible ledger (personal wallets), with few KYC restrictions and is nearly fully anonymous (paper leaves no trail).

In contract, digital payment are intermediated debit/credit of bank accounts.  They are permissioned accounts, held in private bank ledgers, KYC restrictions, identifiable payment history (digital trail).

Complaints w/ status quo: 
1: Inflation
2: Payments System
3: Lack of direct communication between banks.
4: Correspondent banking system for international payments.
5: Banks and MSBs charge too much.
6: Too much personal information presently at risk.

## Bitcoin is a money & payments system

Digital money supply (**bitcoin**) managed by open-source computer algorithm (**Bitcoin**). [ 21M unit cap ].

BTC exist on a publicly visible, distributed ledger: **block chain**. Blockchain = history of all transactions.

BTC “account” = public + private key pairs (crypto. secure).  Public-address transparent P.O. box + private key.  Permissionless, pseudonymous.

Payment requests processed via consensus protocol called proof of work (POW). No banks!

## Bitcoin: deliverables

Capped money supply (hopefully) means long-run price-level stability.  Free ourselves of central banks (alas, not governments).  Ability to transfer value (bitcoin) between any two points in the world (connected to the Internet) at trivial cost.  Free ourselves of all banks (except from their lending arms).

## What’s the bitcoin innovation?

### No:  
* Virtual currency? Open-source algorithm? No.
* Public/private key cryptography? Pseudonymous accounts? No.
* Transparent online database? No.
* Algorithmically determined money supply? Not really.

### Yes:
* Innovation: **block chain** and **proof-of-work consensus protocol**.
* Packaged together with aforementioned innovations.

Bitcoin solved the double-spend problem of P2P digital asset transfer (and monetary supply) without use of “trusted” intermediaries.  

> As close as one can get to unintermediated digital cash.

## POW: Dynamic Membership Multisig

P2P payment requests broadcast to network are validated and added to the block chain by pseudonymous “miner nodes.”  Miners must collectively “sign off” on requests. 

How? Simple voting procedure will not work: Sybil attacks (spam).

POW makes it artificially expensive (hardware + electricity) to validate payments—guards against Sybil attacks.  Miners compete against each other to solve math problem, winner gets to add validated requests to block chain. (Winning) miners compensated in newly-issued bitcoin (and fees).

## So, what?

> A fixed supply of electronic digits that can be transferred over the Internet without traditional middlemen. P2P transactions, no need to relinquish personal info to 3rd parties.

## Other Benefits: 
* Can send $100M of BTC from here to Moscow in 10 min. almost zero user cost (social cost higher).
* Bypass clunky ACH, correspondent banking system.
* Huge deal for international remittances market.
* Block chain has proven to be highly secure (so far, episodes of loss related to 3rd parties (Mt. Gox) not BTC.)


### Use Case: International Payments
Want to send $100 from my Chase NY to your account at Bank of Cyprus, Nicosia ($50 fees at each end?). Align Commerce claims to “use the blockchain” to effect same transfer at much lower cost (price). How? AC ACH debits my USD Chase account (slowest part). AC buys BTC (sells USD) on domestic BTC exchange. AC sells BTC (buys EUR) on foreign BTC exchange. AC SEPA credits your Bank of Cyprus account.

“Using the blockchain” = using BTC as a "vehicle currency".

### Bitcoin as digital gold
Like gold, supply of bitcoin not subject to government manipulation.  Though government can still tax and legislate.  Compliance is an issue (it always is).  Without hassle of storing, assaying, transporting physical gold.  Highly volatile, but may nevertheless be preferable to mismanaged monetary systems?


## Downsides

* Highly volatile exchange rate (e.g., against unit of account).
* inelastic money supply makes it a lousy money.
* While users costs are (presently) low, total costs (miner compensation) range between 2-4% of transaction volume.

* Most of this cost is financed through seigniorage revenue.  Since BTC supply will cease to grow, user fees will have to replace seigniorage.  Not entirely clear where this cost will settle.

## Statistics

* BTC in circulation 14M = $3B (compare USD, $1.3T).
* 75 transactions/min (compare Visa, 200,000/min).
* (Ironically) Most are intermediated via Coinbase, Bitpay, etc.

## History: Bitcoin and banking

Bitcoin solves a payment problem, not a credit problem. Credit supported by reputation, collateral.  Banks turn illiquid assets (reputation, collateral) into money. Demandable liabilities, redeemable for base money @ par.

Base money = historically specie, today fiat currency.  Fractional reserve banking (liquidity transformation).  What prevents banks from issuing demandable liabilities redeemable in BTC (or any other object)?

During U.S. “free” banking era 1836-63, thousands of private state-chartered banks issuing their own banknotes redeemable on demand for specie.  Private clearinghouses (e.g., Suffolk Bank 1818-58), then national banking era 1863-1913.

National banknotes redeemable for specie on demand. State banknotes replaced by checking accounts.  No central bank, no lender-of-last resort.

## Bitcoin vs. Fedcoin

* Existing banking system largely based on pre-Internet tech. Why not permit online utility accounts with Fed?
* Dirt cheap payment processing costs (vs. POW).
* No exchange rate volatility relative to USD.

> New monetary policy instrument: interest-bearing money? But subject to U.S. monetary policy, not permissionless, etc.

## Will bitcoin take over the world?

Fiat systems with politically insulated protocols have little to fear. USD already faces fierce competition, none of which have successfully usurped the greenback as reserve currency.

POW is costly relative to trusted central ledger—mining is a waste of resources (that may be worth paying). Fedcoin?

> Primary consequence of BTC will be to drive rents lower.

Consumers will benefit, but can MSBs using block chain compete? Where is comparative advantage? Technology? Compliance?

Credit side of banking (liquidity transformation) in regulated and shadow banking sectors not immediately affected (Bitcoin 2.0?)


[1]: https://mediacentral.princeton.edu/media/BENDHEIM+Lecture+5-1-15/1_7c94ne0g?utm_source=BitFlash+Subscribers&utm_campaign=407887e6de-BitFlash+Weekly+Review+%286.1.15%29&utm_medium=email&utm_term=0_ad02b6b1a8-407887e6de-181828737


************************

# Bill Janeway

Old school, no slides (as far as I can tell). **Update: 1 Slide!  Love it**

## Bitcoin / Blockchain issues 

* Anarcho-Libertarian rebellion vs. Regulatory compliance 
* Apps vs Infrastr.
* Money: Means of payment vs. store of value vs. unit of account 
* Volatility vs Liquidity
* Retail vs Wholesale
* Infrastructure: protocol vs implementation
* Alternative Protocols v. Alt Implementations
* Anonymous Mining Guilds v. Private Blockchain(s) v. Utility Blockchain(s) 

He and his firm (ref) are not currently invested, but very interested bitcoin observers.

Bitcoin is an app running on infrastructure implement to run a protocol.  It's a money-ish app.  Bitcoin is unique among protocols in that it can be both BOUGHT and USED.  In the early days people didn't use bitcoin, they mostly purchased it on spec.  Perhaps that's still the case in 2015 (7 years after the first 50 btc were mined on the genesis block).

## Volatilty hurts utility as currency 

Bitcoin need more liquidity, a function of usage, which is dependent on regulatory acceptance.  Liquidity enables the moneyness of the asset.  Progress being made, but it's an issue.

> Liquidity requires regulatory compliance.

## Recent breakthrough

Coinbase has secured an investment in the New York Stock Exchange, to create a US-based, regulated exchange. (Tone indicates this could be a watershed event, and many US investors would take note).  This could lead to the desirable boosts in liquidity, also reputation boost.  A good step forward.

Small 'b' *bitcoin* is just an app.  There could be numerous other similar apps.  Ecosystems of compliance and regulation, culture and political capital. 

The taxi industries are unique to a given jurisdiction (SF vs London vs Toronto etc).

### Retail apps 

will experience friction from the establishment.  ie.  When you sell your house for bitcoin, the idiot town clerk will be stumped when you present the blockchain to verifiy the transaction. 

### Wholesale apps

Consenting adults can address a pain point in their business.  Blythe Masters and Co are setting up a blockchain for syndicated loans.  Currently it take 27 days, in which a bank incurs real capital costs, for all the admin to get done. 

Skepticism around mining guilds.  Could they fork the blockchain.  Hints at some unwritten rules.  Avoids the obvious retort to 51% attack: you immediately devalue that which you're attempting to steal.  (Has Bill Janeway ever used git?)

Warburg see openness around how the implementation works. 

> More rapid penetration will take place in less developed, less-government, more open jurisdictions (more frictionless environments).

## Infrastructure 

Alt coins, like Ripple, are alt distributed trust systems (in the case of Ripple, presented as more bank friendly).

> Don't think that there will be one bitcoin -- or block chain -- to rule them all.

It can be emulated through alt protcols and implenet through alt infra.

Closes with image of masked man behind bitcoin hardware company.  Valery Nebesny, of Georgia, the headquarters of BitFury.

> I think we have a ways to go in this new phenomenal capability.   

