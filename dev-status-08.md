## A Development Update  

Stratis has grown quite a lot this last two month with many new exciting updates.  

1. We moved to new offices located in WeWork Moorgate London (come say hi).
2. We hired a few Developers (full/part time), Product Managers and hopefully some Testers soon.
3. We built several teams to deliver some of our planned products and now are quite a decentralized company as the team members are from all around the globe.
4. We are now implementing Agile methodologies, and I encourage autonomous and self-managing teams working to Sprint goals.

### What have we been so busy on?

**TumbleBit:**  
The TB framework is cutting edge tech and extremely complex. It is currently being heavily tested by the community, with bugs and commits going in on a daily basis. The community are very helpful and I want to thank several members who did a great job.  

Our TB dedicated team are working on the Breeze TB integration and the master node registration processes. Part of their work is to remove the TB dependency on the core client and use the C# Fullnode, first on the client and later on the server (those will become the master nodes). The team members are @carlton @zeptin @dangould and @nopara73 just joined.  

With the Breeze release around the corner this is a very exciting time for our C# Node and the TB protocol.  

**Identity:**
The Identity team are working on, well I can't at this stage specify more. 

**ICO team:**
@robertcarr recently joined Stratis and he is working on the ICO platform.  
The ICO platform is getting a Dev boost as we are adding very interesting features.  
It will essentially be an HD-based wallet for enhanced security, and will be hosted in the azure marketplace.  

**Fullnode team:**
The fullnode is our core tech, it's important to note the fullnode is fully functional 
and can track both the Bitcoin and Stratis blockchains, we can mine POW blocks with all kind of hash algorithms 
(all the X13 hash functions) and we can also use the node to stake (up to now we only stake on the stratis testnet).

However there is more work to be done on the fullnode.   

In order to achieve higher code quality and get the node to be production ready (for enterprise standards).

- We need to have more percent of unit test coverage.
- Adding documentation and refactoring of code (improve internal node components).
- Improve the node IBD performance (this may not be a big deal for new blockchains).
- Extending the Stratis test network to run a network of C# nodes for a period of time.
- Ideally we need to get our C# node on an exchange (how and what currency is not yet clear) and on a block explorer

## Sidechains and smart-contracts
I have just released a post on our approach to sidechains [here](sidechains.md) 

For smart-contracts I have joined with Jean Lehmann (https://www.cybercapitalhq.com/team.html) 
a cyber security academic to help with writing a paper on how we can securely deliver smart-contracts on the stratis node, 
this is still not final.

Smart contracts enable applying logic over ownership of assets on the blockchain, 
we will need to change some core components of our fullnode to support smarter logic over assets, 
the node is built mainly on top of bitcoin with a limited smart-contract support. 
We may need to change NBitcoin and the way the Bitcoin protocol stores UTXO 
(the UTXO set will need to be extended to allow contracts access to a key value pair storage among other things)   

We are also exploring executing C# scripts directly in a node environment (smart contract scripts in C#) using a Roslyn compiler 

The fullnode team members are full/part time developers and we also have some contributors, developing on the fullnode
The team: @jeremy @dev0tion @aprogenia @fassadir @mikedennis @someguy (and @bep42)

**The end goal** for the fullnode is to make it THE blockchain framework for C# developers.   
It is becoming evident that in the near future there will be countless blockchains 
(analogues to websites, but maybe not at that scale) and developers will need user-friendly frameworks to develop blockchains and applications on top of blockchains.  
Stratis aims to provide such a platform, we will create out of the box templates of a stratis hybrid sidechain.

**The first sidechain on stratis, an ICO chain**  
A proposal was discussed where the first Stratis sidechain will be created by the devs and community.   
This will serve as a blockchain for issuing tokens/assets, effectively enabling users to host ICOs directly on a specifically-designed blockchain with token issueing in mind.  
Among other things this will allow for community members and developers to raise funds to work on projects that add value 
and yet even more benefit our community.

Having a dedicated blockchain only for raising funds makes sense, token issuers that want to have their 
own blockchain after the ICO may do so by transferring tokens to a sidechain (or burning the tokens).

To achieve this we'll need smarter logic, building on top of the existing *script* language, we'll extend the blockchain to include smart-contracts written in C#.

Some characteristics of such an 'ICO chain':
- The ICO creators set a target and if the target was not reached the senders may claim their coins back.
- Funds will be released based on time locks or voting
- Mile-stones can be set with approval keys distributed to industry experts.
- Single address account 
- Transfer tokens to a sidechain

And more rules can be built in to this blockchain.  

In summery the stratis teams are very busy and rest assure we will deliver some very interesting technology.  
This are exiting times to be a developer.  

Danger