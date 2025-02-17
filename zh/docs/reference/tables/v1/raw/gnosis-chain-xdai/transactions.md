# 交易表

## gnosis.transactions

交易是由用户账户发送的交易签名触发的，一个账户会发起一个交易来更新以太坊网络的状态，交易总是来自外部账户（EOA）的授权，智能合约不能发起交易。

交易会被广播到整个网络，任何节点都可以用广播的方式，请求在EVM上执行事务，在此之后，矿工将执行这笔交易，并将结果状态传播到网络中的其它节点。

更多信息请阅读以太坊官方文档 [这里](https://ethereum.org/en/developers/docs/transactions).

| **列名**              | **数据类型** | **说明**                                                                                                                                                                                              |
| ---------------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| block\_time                  | timestamptz  | 区块被开采的时间                                                                                                                                       |
| nonce                        | numeric      | 该钱包独有的交易随机数                                                                                                                                                           |
| index                        | numeric      | 区块中的交易索引位置                                                                                                                                                           |
| success                      | boolean      | 显示代交易是否成功的真/假值                                                                                                                                             |
| from                         | bytea        | 交易发送者的地址                                                                                                                                                                                  |
| to                           | bytea        | 接收者的地址。当是合约创建交易时为NULL                                                                                                                                  |
| value                        | numeric      | 在此交易中发送的以 wei 为单位的以太币数量。请注意，erc20 代币不会出现在这里                                                                                                       |
| block\_number                | int8         | 区块链的高度（以块为单位）                                                                                                                                                                 |
| block\_hash                  | bytea        | 该区块的唯一标识符                                                                                                                                                                     |
| gas\_limit                   | numeric      | 以 wei 为单位的 gas 限制                                                                                                                                                                                  |
| gas\_price                   | numeric      | 以 wei 为单位的 gas 价格                                                                                                                                                                                   |
| gas\_used                    | numeric      | 以 wei 为单位的交易消耗的 gas                                                                                                                                                             |
| data                         | bytea        | 一个16进制的编码后的数据，或者智能合约指令说明，可以为空                                                                                                                   |
| hash                         | bytea        | 交易哈希                                                                                                                                                                            |
| type                         | text         | 交易类型：`Legacy`, `AccessList`, 或者`DynamicFee`                                                                                                                                    |
| access\_list                 | jsonb        | 交易打算访问的地址和存储密钥的列表，参见 [EIP2930](https://eips.ethereum.org/EIPS/eip-2930)。适用于交易类型为 `AccessLis`t 或 `DynamicFee` 的情况 |
| max\_fee\_per\_gas           | numeric      | 交易发送者愿意支付的每单位 gas 的最高费用总额（由 [EIP1559](https://eips.ethereum.org/EIPS/eip-1559)引入)                                                              |
| max\_priority\_fee\_per\_gas | numeric      | 交易发送者愿意向矿工支付的每单位 gas 的最高费用，以激励他们包含他们的交易 （由 [EIP1559](https://eips.ethereum.org/EIPS/eip-1559)引入)                      |
| priority\_fee\_per\_gas      | numeric      | 本次交易支付给矿工的优先权费用 （由 [EIP1559](https://eips.ethereum.org/EIPS/eip-1559)引入)                                                                         |