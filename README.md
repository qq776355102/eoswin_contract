#欢迎加我微信相互交流
 momo1106714071
 
# EOS.Win - purely on-chain decentralized platform 

We are glad to announce that all games on EOS.Win are open source, including Dice, Lottery, BLACKJACK and Jackpot. We wish we can contribute to the development of EOS ecosystem.

#### As we emphasized before, EOS.Win doesn't have local servers and all the random numbers are purely generated by blockchain.

For contracts deploying each time in the future, we will update the contract.

1. Synchronize the codes verification on EOSPark.
2. Synchronize the codes on Github.

#### Verifying the consistencey of on-chain contract hash (take Dice for example):
```sh
$ sha256sum dice.wasm
$ db7174b9bf28874c7e30d3b3e4aade0ce96779d582ad5a9cdf98727134a529be  dice.wasm
```

#### On-chain contract hash:
1. [Dice](https://eospark.com/MainNet/contract/eosluckydice)
1. [Lottery](https://eospark.com/MainNet/contract/eosluckygame)
1. [BLACKJACK](https://eospark.com/MainNet/contract/iamblackjack)

You can verify consistency between local hash and on-chain hash.

#### Random Number Verify:
```sh
$ cleos push action eosluckydice verify '["your_receipt_seed"]' -p youraccount
```
#### Lucky Draw Random number verify:
```sh
$ cleos push action eosluckydice luckreceipt '["your_receipt_seed"]' -p youraccount
```
These implements also can be done on [bloks](https://bloks.io/account/eosluckydice).
