# Hardhat Fund Me - Typescript Edition

££ Solhint

```
yarn solhint contracts/*.sol
```

££ Deploy

- Used hardhat-deploy npm package  
```
yarn harhat deploy
```

££ Chainlink Addresses

- https://docs.chain.link/data-feeds/price-feeds/addresses/?network=ethereum

££ Mock Deploy 

- Used the MockV3Aggregator from chainlink https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.6/tests/MockV3Aggregator.sol
- This is placed in contracts/test folder. 

- Check the tags in 00_deploy_mocks.ts 
- This command runs only the tagged ones
```
yarn hardhat deploy --tags mocks
```
- Can check these deployed contracts in the  hardhat node. 
- Run this in another console.

```
yarn hardhat node
```
££ Style Guide 

- https://docs.soliditylang.org/en/v0.8.17/style-guide.html
- Check this Order of Layout :
- https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-layout


££ Testing

- Unit Tests are done locally
- - local hardhat
- - Forked hardhat
--
- Staging Tests are run on Testnetst 
- yarn hardhat test --grep "Withdraw ETH"
- - Runs the test with matching string 

££ 
Ethers Documentation 

- https://docs.ethers.org/v5/
- https://docs.ethers.org/v5/api/utils/display-logic/#utils-parseUnits


££ Cheaper

- State Variables : https://docs.soliditylang.org/en/v0.8.17/internals/layout_in_storage.html
- Check Implementation at https://youtu.be/gyMwXuJrbJQ?t=42753
- OpCodes to calculate GasCosts
- https://github.com/crytic/evm-opcodes
- SLOAD and SSTore are very costly 
- Checkout the different variables and their Conventions

$$ Staging Tests

- Staging Tests only run on Test nets while Normal Unit Tests run on Development ( local ) networks
- These are run before deploying to the main net for the final confirmation

£££ Reference : 
https://github.com/PatrickAlphaC/hardhat-fund-me-fcc
