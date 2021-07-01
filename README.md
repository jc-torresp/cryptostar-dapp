# Decentralized Star Notary Service and DApp

Proof of concept on how a Decentralized Application using ERC-721 Tokens can be implemented in astronomy allowing to register stars and track the ownership of each.

### Dev tools
This project was developed with:

| Library/Module/Tool | Version |
|---|---|
|  *Truffle* | 5.3.13 (core: 5.3.13) |
|  *Solidity* | 0.5.16 (solc-js) |
|  *Node* | 14.16.0 |
|  *Web3.js* | 1.3.5 |
|  *truffle-hdwallet-provider* | 1.0.17 |
|  *openzeppelin-solidity* | 2.3 |
|  *MetaMask* | 9.6.1 |
|  *dotenv* | ^10.0.0 |

### Contracts

The project was deployed in the Rinkeby Network with the next contract addresses:

| Contract | Address |
|---|---|
|  *Migrations* | [0xBeE8cE7027abE0d3152e7c7C94bCc95090bec868](https://rinkeby.etherscan.io/address/0xBeE8cE7027abE0d3152e7c7C94bCc95090bec868) |
|  *StarNotary* | [0xF4902d19f827C9046167DEcA5F2550B0417477F7](https://rinkeby.etherscan.io/address/0xF4902d19f827C9046167DEcA5F2550B0417477F7) |

You can find the complete deployment log in the file "*rinkeby-deployment.log*".

We use a ERC-721 token with the next metadata:

- **Name:** CrytoStar Token
- **Symbol:** CST

### Run the application

1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version
node -v
# Check NPM version
npm -v
```

2. **Truffle v5.X.X** - A development framework for Ethereum. 
```bash
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version
npm install -g truffle@5.0.2
# Verify the version
truffle version
```

3. **Dependencies**
```bash
# Project's root directory
npm install
# App directory
cd app
npm install
```

4. **MetaMask** - Install MetaMask extension in your browser.

5. **Add a Custom RPC** in MetaMask with these information:

| Network Name | New RPC URL | Chain ID |
|---|---|---|
|Private Network 1|`http://127.0.0.1:9545/`|1337 |

6. **Add at least two accounts** using the private keys that shows when you run `truffle develop`. MetaMask must show the balance of the two accounts.

7. **Create a .env file** in project's root with the next environment variables:
```bash
INFURA_KEY=<YOUR INFURA KEY>
SECRET=<YOUR METAMASK 12 WORD SEED>
```

8. **Start Truffle**
```bash
# For starting the development console
truffle develop

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test
```

9. **Start web server**
```bash
cd app

# Enter the url => http://localhost:8080/ in your browser
npm run dev
```