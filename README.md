# Aave Dai Flash Loan

1. verify smart contract locally:<br>
truffle run verify Flashloan@smart_contract_address_here -- network kovan

2. Send some kovan Dai to the smart contract for fee payment

3. perform the flash loan:<br>
truffle console --network kovan<br>
migrate --reset<br>
let f = await Flashloan.deployed<br>
amount = web3.utils.toWei('1000') //borrow dai<br>
asset = 'insert_dai_address_here' //Dai kovan<br>
f.flashloan(asset, amount)

example of flashloan performed:<br>
https://kovan.etherscan.io/tx/0xcbc2e7163d76c4c31bc1eb88911a9111736db01ea9816ec1aa22e9cd494728e1
