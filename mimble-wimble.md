# Mimblewimble: Private, Massively-Prunable Blockchains 

Preserved bitcoins security model, without having to keep as much data lying around. 

## Links 
Talk: https://www.youtube.com/watch?v=aHTRlbCaUyM
Repo: https://github.com/ignopeverell/grin
Proofs of Proofs of Work:  Can compress lots of blocks... http://fc16.ifca.ai/bitcoin/papers/KLS16.pdf

## Notes 

Like coin join in bitcoin, except you can essentially concat two transactions into 1.  In bitcoin the network needs to do this, but with MW the the two transacting parties can join two transactions into 1.


Supports confidential transactions (reduces data load.  Massive bandwidth savings)...

Could potentially be an altcoin, and a sidechain...

What is UTXO rangeproof? 

Holy shit... 21:20 The length of the chain does not determine the size, but rather the amount of unspent transaction. 

Unspent outputs from each block are determine the size.  Incentives are created to reduce the size of UTXO set, and :. save bandwidth... 

Problems: 

-- unconditionally sound commitments and rangeproofs... (WHHAAAA)

	-- if the crypto were broken, then confidential transactions would be vulnerable to forged transaction amounts.

	-- trade off between soundness and hiding.  Rather expose identity than amount in the crypto...  but this causes an increase in the bandwidth required (~20% performance penalty for adding layer of crypto to secure amounts/values)

-- possible to make 1000 rangeproofs smaller?  Yes!  Regular digital sigs can shrink the size of the blocks (with bitcoin), but perhaps not rangeproofs.

	-- rangeproofs are the bulk of the data and encryption time
	
-- merge conflicts... 

-- quantum resistance 
	-- can we develop new cryptographic primatives that dont break with quantum computers?

### Q&A (32min)

Real time is not effective at increasing transactions per second. In real time, it is inferior to btc... (Long term reduction in blockchain size is the key)

