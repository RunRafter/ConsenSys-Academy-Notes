## Definitions
- A ledger is distributed when it has been securely replicated across geographic locations. Some features of DLT include:
1. Consensus formation
2. Peer-to-peer protocols
3. Cryptographic infrastructure

- A blockchain is one type of distributed ledger, which uses blocks as the security mechanism for maintaining shared information and state

## Consensus Mechanisms

- Economic mechanism that facilitates the agreement process among participants to guarantee data consistency.
- Distributed Ledger Technologies use a variety of consensus mechanisms that allow nodes within a given network to share and agree upon state.
- By design consensus mechanisms provide an economic incentive to honest participation within a network.
- Each mechanism includes rules to determine what is a valid block.
- Some examples of Consensus Mechanisms include:

1.  Practical Byzantine Fault Tolerance
    - Guarentees that consensus can be reached within a network even if a minority of nodes are dishonest or absent.
    - Tolerates 1/3 dishonest or absent participants. 
    - A functioning network with 1 out of 4 faulty nodes is byzantine fault tolerant.
2.  Proof of Work
    - Particpants only accept valid block when blockhash is less than target number (difficulty).
    - Miners in a network repeatedly hash the block contents and check the output to see if it matches some specific criteria.
    - When the correct block hash is found it is broadcasted throughout the entire network and the miner is awarded.
    - Block includes cryptocurrency reward for miner.
    - Blocks are mined a deterministic rate (every 15 seconds in the Ethereum Network)
    - POW is computationally expensive - high energy use.
    - Restricted to low txn volume - block times can't be too short (public blockchains where anyone can spin up a node, to allow more ppl to participate limits hardware requirements for nodes).
    - With unknown parties, doesn't make sense to use disincentives system that can increase efficiency.
3.  Proof of Stake
    - Currency holders stake some amount of the currency for the chance to validate a block.
    - The block validator is randomly selected by the network but the chance of selection is proportional to the stake.
    - Participiants will only accept block from validator that is chosen for that period. 
    - Favours large stake holders. Typically higher txn volume than POW.
    - Leased POS: Token holders can lease balances to others. Rewards split among leasers.
    - Delegated POS: Balance holders elect block validators. No sharing of block rewards. Incentivizes validators to maintain good behaviour.

## Mining

- In the Proof-of-Work consensus scheme, mining is the process of validating transaction blocks through hashing the block contents. This process makes it incredibly difficult to guess the correct answer but very easy to verify the correct guess has been made.
- Each time a node wins the block they suggest the next state of the system and broadcast their solution to the network. Other nodes verify that the solution is correct and update their ledgers such that the validator recieves the block reward.
- The difficulty is adjusted based on how quickly the previous block was mined.
- Each block contains a list of transactions, the hash of the most recent block, nonce, and block reward.
- The ethereum proof-of-work algorithm abides by three main rules:
  1.  Rejects invalid blocks
  2.  Requires proof of work to contain a hash less than the target block #
  3.  Longest chain is always considered to be the most up-to-date/ trusted
  
  ![EthereumMining](/images/ethMining.png)

## Public Vs Private Blockchains

### Public

- Anyone is allowed to join as a trust-less participant, they recieve a wallet that does not contain any personal information and allows them to be pseudonymous in the network. Addresses of participants are publicly viewable, but addresses not necessarily linked to any person or identity.
- Anyone can read and write data from/to the blockchain, participants not vetted - permisionless. 
- Transaction processors must invest financially to prevent fraud with Proof of Work or a direct incentive (i.e. cryptocurrency)
- Costs digital currency to process transactions (e.g. Ether, Bitcoin) 
- Censorship resistant - anyone can observe, record, and submit txns
- Examples: public Ethereum and Bitcoin networks

### Consortium (or shared, permissioned chains)

- Only verified participants are allowed to participate - block validator identities known,  allowing participants to punish bad actors. 
- Enables different consensus mechanisms.
- Can achieve higher transaction throughput compared to public networks.

### Private (or permissioned chains / sandboxes)

- Designed for rapid application development, instant deployment, and single-enterprise deployment solutions.
- Prototyping and development needs for learning.
- Participants are known and trusted - Validators are legally accountable and are incentivized by reputational risks
- Potential for a small number of nodes with ability to change data
