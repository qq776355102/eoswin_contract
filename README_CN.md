# 欢迎加我微信相互交流

momo1106714071

# EOS.Win - 纯链上去中心化游戏平台

我们很高兴开源所有的合约代码，包括骰子、彩票、21点以及jackpot，为EOS的生态贡献自己的力量。

#### 正如我们之前一直强调的，EOS.Win没有服务器，所有的随机数都是在链上生成的。

对于将来的每一次合约更新，我们将在更新合约之后：
1. 同步更新eospark的代码验证。
1. 同步更新github。

#### 检验与线上的合约hash是否一致（以骰子为例）：
```sh
$ sha256sum dice.wasm
$ db7174b9bf28874c7e30d3b3e4aade0ce96779d582ad5a9cdf98727134a529be  dice.wasm
```

#### 线上的合约hash
1. [骰子](https://eospark.com/MainNet/contract/eosluckydice)
1. [彩票](https://eospark.com/MainNet/contract/eosluckygame)
1. [21点](https://eospark.com/MainNet/contract/iamblackjack)

可以将本地的hash与线上的合约hash对比看是否一致

#### 骰子随机数验证：
```sh
$ cleos push action eosluckydice verify '["your_receipt_seed"]' -p youraccount
```
#### 骰子幸运抽奖随机数验证：
```sh
$ cleos push action eosluckydice luckreceipt '["your_receipt_seed"]' -p youraccount
```
当然这些操作也可以在[bloks](https://bloks.io/account/eosluckydice)上完成。
