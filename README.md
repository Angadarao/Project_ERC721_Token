1) Downloaded the starter code from the Git Hub @ https://github.com/udacity/nd1309-p2-Decentralized-Star-Notary-Service-Starter-Code

2) /# Check Node version
node -v

3)# Check NPM version
npm -v

4)# Unsinstall any previous version
npm uninstall -g truffle

5) Install truffle latest version
npm install -g truffle

6) Noticed issues while brining up truffle develop
fix:
npm i -g truffle@nodeLTS

6)# Verify the version
truffle version

7) cd into app folder and npm the below packages
npm i copy-webpack-plugin@4.6.0
npm i webpack@4.28.1
npm i webpack-cli@3.2.1
npm i webpack-dev-server@3.1.14
npm i openzeppelin-solidity@2.3

8) Configured Ganache with truffle's port and Network id of 4447

9)Configured the Metamask with the local truffle instance
RPC URL http://127.0.0.1:9545
Chain ID 1337 (node index.js will give you the chain ID)

10) After the code changes compile the code
truffle compile

11) Migrate the code to local network. Make sure that Metamask is connect to the locally running truffle instance
truffle migrate --reset

12)run the tests
truffle test

13) cd to app folder and start the local server
npm run dev
This will make the html page showup on http://localhost:8080/

14) make some addition of the star names and starID followed by validating then by searching on the Lookup start option.

15) Update the truffle-config.js with the infuraKey and the seed phrase.
Enable the rinkeby network options.
rinkeby: {
  networkCheckTimeout: 10000,
  provider: () => new HDWalletProvider(mnemonic, `https://rinkeby.infura.io/v3/${infuraKey}`),
  network_id: 4,       // rinkeby's id
  gas: 4500000,        // rinkeby has a lower block limit than mainnet
  gasPrice: 10000000000
},

16) Observed a timeout issue while migrating the code to rinkeby test network.
Fix: We need to add the networkCheckTimeout: 10000.

17)Run the migrate to rinkeby test net using --skipDryRun attribute.
truffle migrate --network Rinkeby --skipDryRun

18) This will deploy the smartcontract to rinkeby test network
https://rinkeby.etherscan.io/address/0x93711466232De7eC8b3E78358c3d7a955e77a5C3
Your ERC-721 crypto coin
Your ERC-721 CC
