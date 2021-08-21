# Chainlink-Keepers

## Steps

- Create contract with `KeeperCompatibleInterface` which supports functions `checkUpkeep` and `performUpkeep`
- Deploy in testnet for testing. Chainlink keepers supports `Kovan Network`. 
- Keepers wants contract to be verified in etherscan to check whether contract is `KeeperCompatible`. Its optional.
- Keeper contract has to be registered with the Chainlink Keeper Network. `https://keepers.chain.link/upkeeps/new`
- Upkeep address should be the Deployed contract.
- After registration, funds has to be added to the upkeep id. Done via the `view upkeep` page.
- Once the fund got transferred, keeper will start checking for `checkUpkeep` and once the condition mets `performUpkeep` will be called.