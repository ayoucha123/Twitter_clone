## Solidity Twitter Clone Dapp 

## Development Steps

- Development of a CRUD API in Solidity
- Deployment to Rinkeby
- Development of a front-end to interact with the smart contracts

## Learning Objectives and Outcomes

To learn how to lead an Ethereum project, end-to-end:

- Solidity development
- Unit tests
- Deployment

## Specs

- Any user should be able to read all the tweets
- Any user should be able to write tweets
- A user should be able to update a tweet he wrote
- A user should be able to delete a tweet he wrote

## Project Requirment/Setup

1. You need to create a virtual wallet [Metamask](https://metamask.io/) account and select "Rinkeby Test Network", I recommend reading this [article](http://www.alchemy.com/overviews/rinkeby-testnet).
2. To get testnet Ether (ETH) in order to test and troubleshoot our decentralized application, I recommend checking [Chainlink](https://faucets.chain.link/rinkeby) and [Rinkeby Faucet](https://rinkebyfaucet.com/).
3. You have to create an account on [Alchemy](https://www.alchemy.com/) and generate an API key by creating an app. This will allow us to make requests to the Rinkeby Test Network. If you’re not familiar with testnets, check out [this guide](https://docs.alchemy.com/alchemy/guides/choosing-a-network#rinkeby). I also recommend going over this [Alchemy documentation](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract) as it explains every step throughly.
4. After cloning the repo and creating your accounts and generating the API key, now you have to create a `.env` same as [.env.example](https://github.com/EliasAfara/Solidity-Dapp-Twitter-Clone/blob/master/server/.env.example) and fill in your keys.


## 🐑 Clone locally

Make sure you have installed [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), [Node.js](https://nodejs.org/en/) (Please install **16.14.0**, I recommend using [nvm](https://github.com/nvm-sh/nvm)).

Then clone the repo, install dependencies and start the server by running all these commands:

```Bash
git clone https://github.com/EliasAfara/Solidity-Dapp-Twitter-Clone.git
cd Solidity-Dapp-Twitter-Clone/server
npm i
cd ../client
npm i
```

### Test the Smart Contract

```Bash
cd server
npx hardhat test
```

Results in all 4 tests passing:

```text
  Twitter App Contract
    Create Tweet
      ✔ should emit NewTweet event
    Get All Tweets
      ✔ should return the correct number of total tweets (65ms)
    Update Tweet
      ✔ should emit UpdateTweet event
    Delete Tweet
      ✔ should emit delete tweet event


  4 passing (3s)
```

## Deployment

```Bash
cd server
npx hardhat run scripts/deploy.js --network rinkeby
```

copy the genereated contract address and paste it in the [config](https://github.com/EliasAfara/Solidity-Dapp-Twitter-Clone/blob/master/client/src/config.js)

> **_NOTE:_** You can also run the scripts inside package.json inside the server dir.

## Making Your First Transaction

After deploying your smart contract, you can copy the generated contract address and check it out on [Rinkeby Etherscan](https://rinkeby.etherscan.io/).




![image](https://user-images.githubusercontent.com/54351909/160769519-f2ebbc99-afa2-4071-badd-9c28fbf9e17c.png)
