# Ebola on Ethereum
It seems like a bad idea, but let's give it a try. This is a [live Smart Contract on Ethereum]() that delivers a link to a text file on [Swarm](http://swarm-gateways.net/bzz:/theswarm.eth/) (Ethereums decentralized storage) which contains the ebola virus genome. A full write up on this project can be found on Medium.

**There is no need to ever send Ether or ERC20 tokens to this contract! Functions are called on, not transactional which means usage is free.**

If you would like to send me a tip or buy me a coffee, us the Ethereum tip address in the contract (0x0).

## Why Ebola?
It was trending in the news at the time when I first had this idea and the public went a little crazy with “ebola fever”; no one was safe. Putting something like the digital version of a virus that caused a some maina on a blockchain that also happened to be causing a disruption seemed like a fun idea.

## Smart Contract Address & ABI
Address: [0x0]()

Contract ABI/JSON Interface:

```[{}]```

## Functions
- *“getInfo”* Returns basic text info of the contract.
- *“getEbola”* Returns a bit.ly link to the genome file (see note below).
- *“tipCreator”* Returns the creators Ethereum tip address if a user is feeling generous and or amused.
- *“kill”* The only function the creator has sole access to. This will destroy the contract and send any Ether in the contracts balance back to the creator.

A bit.ly URL was used because in order to truly decentralize the genome file it had to be hosted on Swarm. Swarm produces a unique hash string of the file which can be used to retrive the file in a browser (prefaced by http://swarm-gateways.net/bzz:/FILE-HASH). The hash string is 64 characters long, which is too long for ease of use in the contract and looks scarry. So using a URL shortner like bit.ly was an easy quick fix that still returns and re-directs to Swarm file.

### Expected Results For Functions
| Function      | Hex Code      | Result Returned | Access        |
|:-------------:|:-------------:|:---------------:|:-------------:|
| *getInfo()*   | 0x0           | Two Text Strings | Public     |
| *getEbola()*  | 0x0           | URL String       | Public     |
| *tipCreator()* | 0x0          | Address String   | Public     |
| *kill()*      | 0x0           | Terminates the Contract | Creator Only |

## Web3 Setup
You will need a node on the main Ethereum network to interact with this contract via web3.

In the example javascript below we're using an Infura API URL, this is free and you'll need to get one before runing the script. You will also need the [Web3.js (1.0.0 or later) Module](https://github.com/ethereum/web3.js/) and [Node.js (8.7.0 or later)](https://nodejs.org/en/) all saved in a project folder you're running this script from.

``` javascript
{}
```
