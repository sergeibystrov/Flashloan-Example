# Aave Dai Flash Loan

1. verify smart contract locally:
truffle run verify Flashloan@smart_contract_address_here -- network kovan

2. Send some Dai to smart contract for fee payment

3. perform flash loan:
truffle console --network kovan
let f = await Flashloan.deployed
amount = web3.utils.toWei('1000') //borrow dai
asset = 'insert_dai_address_here' //Dai kovan
f.flashloan(asset, amount)

example of flashloan performed:
tx hash flashloan:
https://kovan.etherscan.io/tx/0xcbc2e7163d76c4c31bc1eb88911a9111736db01ea9816ec1aa22e9cd494728e1
