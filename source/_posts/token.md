---
title: Token(通证)
---

Web3 中的 Token 的作用：

- 代币：ERC20 类型的通证基本都属于这种类型，可用于众筹，债券发行，商品与服务的买卖，其总市值代表一个项目的总资产合总价值
- 金融工具与金融衍生品
- 所有权令牌：ERC721 代币属于这种类型
- 激励工具：如比特币
- 安全保障手段：如比特币、ETH
- 投票权：如 EOS
- 股权证书
- 门票或通行证
- 自治组织(DAO)的治理工具

什么是同质化和非同质化通证呢

同质化：具有相同的某种特质或某个种类，那么就会认为是同质化的，每个个体之间没有差别，每个个体之间的价值完全相同，可以互相交换，如代币之间就属于同质化通证

非同质化：不同物品之间具有独特、不可替代、不可互换这些特性的话，就满足了非同质化通证的特点，如艺术作品、人、游戏角色、房产等

## 以太坊不同通证的标准

| ERC20        | 可替换资产的原始代币合约                                                |
| ------------ | ----------------------------------------------------------------------- |
| ERC-165      | 创建标准方法以发布和检测只能合约的借口                                  |
| ERC-173      | 合同所有权的标准接口                                                    |
| ERC-223      | 向后兼容 ERC-20，保护投资者以防意外的转账                               |
| ERC-721      | 非同质化代币(NFTs)标准，可作为产权进行交易                              |
| ERC-725      | 密钥管理和执行的代理合同，简历区块链身份                                |
| ERC-777      | 基于操作者的代币标准，具有高度可定制性                                  |
| ERC-809      | 非同质化的租赁标准，用户可使用一系列指令来出租 NFTs                     |
| ERC-827      | 允许转让通证并允许持有人允许第三方使用通证                              |
| ERC-864      | NFTs 共有产权，旨在 NFT 合约中分享 NFT 的所有权                         |
| ERC-865      | 此项标准允许用户委托第三方帮忙转账，并以代币形式支付 Gas 费用           |
| ERC-918      | 可开采性代币，允许加入挖矿算法                                          |
| ERC-874      | 加权的不可替代代币，便于了解到独特的资产拥有的价值                      |
| ERC-888      | 多维代币标准，使用标识符代表余额和数据                                  |
| ERC-998      | 可拆解非同质化代币，可包含多个 ERC-721 和 ERC-20 的形式                 |
| ERC-1067     | 可升级代币合约的标准，提供代币在合约在内的多种用途的事件锁仓功能        |
| ERC-1132     | 代币锁定能力的标准，提供代币在合约多种用途的事件锁仓功能                |
| ERC-1155     | 多代币标准，可追踪多个代币余额和所有权的合约，及定义多个物品            |
| ERC-1178     | 多级别代币的标准，为多个级别的代币的合约提供标准接口                    |
| ERC-1190     | 非同质化版税代币标准，可向创造者以及/或者所有者支付版税                 |
| ERC-1203     | 多层级代币标准，提供多层级代币合约的标准接口                            |
| ERC-1238     | 不可转账代币标准，代表徽章的不可转账代币                                |
| ERC-1400     | 证券通证标准，部分可互换代币，该 EIP 标准具有能力进行强制转移           |
| ERC-1404     | 为证券通证、通证化证券以及其他携带复杂要求的其他通证儿准备              |
| ERC-2612     | 该标准可以取消 ERC-20 的 approve + transform，同时海允许无 Gas 通证转账 |
| Minime Token | 带更多功能的 ERC-20 代币（易克隆），获得余额转账历史及代币控制          |