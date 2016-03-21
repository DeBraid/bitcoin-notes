# Random Notes on Ethereum and History of Crypto. 

Links: 

* On-Chain transaction growing steady for [Ethereum](https://twitter.com/ofnumbers/status/711620882578350080) 
* Ethereum for Dummies - lecture by Dr. Gavin Wood [at DEVCON1 via YouTube][2] .

## Ethereum: customized, user-created blockchains

From [ethereum][1] white paper: underlying blockchain technology as a tool of distributed consensus is the other major breakthrough provided by bitcoin.

> Ethereum: provide a blockchain with a built-in programming language that can be used to create "contracts".

Broad categories of such alternative blockchain applications include: 

* coloured coins
* smart property
* smart contracts

These contracts encode arbitrary state transition functions, allowing *users to create* any of the systems listed above, and others not yet imagined, simply by writing the business logic in a few lines of code.

## Ethereum Guarantees 

All of the messages in our computer have some origin.  They can be checked to see WHO sent the message.

Currently, there is no other object-oriented message execution environment where you can *always* check and verify who sent the message.  Moreover, this message is permanent!

From Gavin Wood on guarantees that Ethereum makes.  When code is executed on the computer that is Ethereum, you get the following:

* Atomicity
	* all or nothing operation.  The whole program runs or nothing runs.
* Synchrony
	* no 2 operations can interfere with one another
* Provenance
	* all messages can be inspected to verify them
* Permenence
	* there is no OFF mode.  All the objects will exist forever.
* Immortality 
	* object can never be externally deleted.  Can only voluntarily commit suicide.
* Immutable 
	* the code that executes cannot change.


## Innovation Commons



Compared to the walled garden that is a server, E is an open, common platform.

> Ethereum is worlds first decentralized computer.   

Servers, by contrast, are cumbersome and make interoperability difficult.  They create privacy, security, and authenticity issues.


# History of Cryptography

#### 1970s

Public key cryptography changed dramatically in early 1970s, when Bailey Diffie and Martin Hellman developed the fundamental ideas of dual-key, aka public key, cryptography. 

They published their results in 1976—solving one of the fundamental problems of cryptography: key distribution.  The consequences were profound as they essentially broke a monopoly held by government entities on cryptographic technology.

Diffie-Hellman key-exchange paper allowed every company, every citizen the sorts of crypto that not many years prior ranked alongside the atomic bomb as a source of government/NSA power.

#### 1980s and 1990s

Anonymous e-cash protocols were created but failed to gain traction as they relied on central intermediary. 

1988 Wei Dai proposed b-money, the first to propose creating money through computational puzzles + decentralized consensus.  

#### 2000s

In 2005 Hal Finney introduced RPOWs, 'reusable proofs-of-work' which combined elements of b-money with Adam Back (of Blockstream.io) Hashcash, but again fell short of long-run success due to the reliance on central authority (trusted computing as backend).

In 2009, Satoshi Nakamoto successfully created and built a public-key cryptography 

[1]: https://github.com/ethereum/wiki/wiki/White-Paper
[2]: https://www.youtube.com/watch?v=U_LK0t_qaPo&list=LL6rYoXJ_3BbPyWx_GQDDRRQ&index=4&ab_channel=Ethereum