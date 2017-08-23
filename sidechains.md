## Sidechains Overview

The purpose of this post is to describe sidechains and how we may intend to implement sidechains on the Stratis Node. 

Sidechains are a way of transferring coins (more accurate is transfer value) between blockchains. 
In various papers this is also referred to as pegged sidechains.

There are two sidechain types one-way/two-way pegs, one-way means coins are burned on the parent chain and cannot transferred back form the sidechain.

### Sidechain Consensus Rules
Sidechains are essentially blockchains that allow unlocking of pre-defined coins, the same concepts of a distributed consensus model apply in a sidechain.  
The consensus rules of a sidechain can be 'adapted' to be fit to purpose, the rules will be built in to the consensus model of the sidechain.  
Some examples of possible rules are:  
- Transfer between blockchains can have built in limitation for example up to a total of X amount are allowed to be transferred in to the sidechain.  
- Transfers can be time locked (i.e. the pegging window will only be open between block N -> N+1000).  
- Transfers can only come from predefined Blockchains by hardcoding allowed genesis blockchains either in the genesis block or in the consensus rules (this can be hard forked to add more genesis chains)  
- Transferred coins may have a different denominator (not necessarily a 1:1 scale but 1:N)  

