---
title: 永续合约
---

永续合约已经成为了加密货币交易量最大的交易方式，但永续合约是一个币圈独创的产品，与平时接触的普通金融衍生品不同，币圈永续合约的设计理解起来有点困难，甚至很多人虽然经常用永续合约，但依然不知道各种指标是什么意思。

很多人爆仓，是因为不能理解币圈永续合约的本质。

### 永续合约的全称，叫做「期货永续合约」

三个关键词：期货，永续，合约

期货：相较于现货而言，在现货交易中，双方直接一手交钱一手交货，而在期货交易中，约定了在将来某个时间以某个价格交易商品，举个例子，A 和 B 约定，在两个月后，A 以 200 元/斤的价格卖 100 斤大米给 B，双方签订了合同，则 A 是合约的卖方，B 是合约的买方，这个交易的过程，就是以期货的交易形式的合约，期，即未来的时间的意思，和现货对应

在这个过程中，如果 A 和 B 的双方的某一方不想要按照原来的约定买大米了，那么，他们签订的这份合同可以卖给别人，如果是 B 卖的，那么 B 就变成了合同的卖方，期货合约都是有到期期限的，在最后时间是一定要交割的，到了`交割日`，买卖双方会强制按照当初的约定进行交割，这个中合约也叫做`期货交割合约`

为了让合约购买的双方，在合约的到期日都能遵循约定进行交割，双方都需要缴纳一定的资金，这个就叫`保证金`。

在交易所中，假设当前 BTC 的价格为 2W 美金，而 A 觉得，到了下个星期，BTC 能涨到 2.5w 美金，那么 A 就会买入看涨合约，同时要缴纳一定的保证金，（这个保证金的缴纳需要看当时买入的合约本位是什么），这份看涨合约代表：下个星期，A 有权利以 2w 美金的价格买入 BTC，而合约市场（期市）是需要对手盘的，也就是交易对手才能成交，假设对手是 B，B 觉得下个星期 BTC 会跌，所以 B 想在下个星期以 2w 美金的价格卖出 BTC，对于 A 来说是先低买高卖，对于 B 来说是先高借后低还。

到了下个星期，如果 BTC 的价格跌到了 1.8w 美金，那么 A 亏损，B 盈利

以上的例子讲的期货合约，最后都要交割，称之为`交割合约`，还有一种没有交割时间的合约，就是`期货永续合约`，永续合约分为两种，`正向合约`和`反向合约`

正向合约很好理解，跟踪的交易标的是 BTC，以 USDT 计价，保证金也是 USDT

反向合约的跟踪标的和计价都和正向合约一样，但是以 BTC 为保证金，这个就是`X本位合约`的意思，

<aside>
<img src="/icons/cow_yellow.svg" alt="/icons/cow_yellow.svg" width="40px" /> 举例：`U本位`就是正向合约，`币本位`就是反向合约

</aside>

从交易体验来说，正向合约使用 USDT 一种币种作为保证金，可以开多币种的合约，确实是更灵活，更适合新手使用，合约的单位是张，但一张正向合约和一张反向合约所代表的面值分别是多少呢？一张 BTC 合约的面试通常是需要提前约定，不一样的地方在于，正向合约一张合约面值按 BTC 数量算（价值多少个 BTC），而反向合约是按 USDT 数量（价值多少 USDT），比方说可以假设

| 合约类型              | 合约面值 |
| --------------------- | -------- |
| 一张正向 BTC 合约面值 | 0.1BTC   |
| 一张反向 BTC 合约面值 | 100USDT  |

以上说明什么呢，正向合约需要拥有币种标的如：BTC，反向合约是按 USDT 计价的，只需要拥有 USDT 即可，这也是反向合约入场门槛低的原因，其次也和看涨看跌合约有关，一般，如果是看涨合约，那么就买正向合约，如果盈利的话则是币值涨 + 合约收益

## 保证金

保证金是开仓是需要缴纳的资金，正向何雨两者保证金计算如下：

正向合约的仓位价值 = 合约面值 _ 合约张数 _ 标记价格

正向合约的仓位价值 = 杠杆倍数 \* 保证金数量

$$
合约价值*合约张数*标记价格 = 杠杆倍数 * 保证金数量
$$

以上的公式可以看出，杠杆倍数越高，保证金数量不变的情况下，能开的张数越多，如果盈利，收益越高，如果亏损，保证金数量需要追加的数量越大。

举个例子：在 BTC 价格是 2w 美金的时候，买 5 张 BTC 正向合约，以 2 倍杠杆买入，则保证金：

$$
保证金=0.1*20000*5/2=5000 USDT
$$

0.1 是合约面值，20000 标记价格，5 为合约张数，2 位杠杆倍数

反向合约的情况是

反向合约的仓位价值=合约价值\*合约张数

反向合约的仓位价值=杠杆倍数*保证金数量*标记价格

所以反向合约中：**合约价值*合约张数=杠杆倍数*保证金数量\*标记价格**

上面的例子中正向合约的仓位价值是 1w 美金，所以在反向合约中我们也买入同样的仓位价值（这在真实的交易市场中是同样的情况）需要买入 100 张合约（假设一张 BTC 反向合约 100USDT，买入 100 张就是 1w 美金），那么保证金是：100*100/（2*20000）= 0.4BTC，而 0.4BTC 的价值就等于 5000USDT

## 盈亏计算

在正向合约中，

做多时：盈亏 = (平仓价-开仓价)*合约面值*合约张数

做空时：盈亏 = (开仓价-平仓价)*合约面值*合约张数

在上面的例子中：在 2w 美金买入 5 张 BTC 合约，并在币价 2.5w 美金时卖出，则盈亏是：

$$
(2.5w-2w)*0.1*5 = 2500USDT
$$

在反向合约中

做多时：盈亏 = (1/开仓价 - 1/平仓价)*合约面值*合约张数

做空时：盈亏 = (1/平仓价 - 1/开仓价)*合约面值*合约张数

在上面的例子中：在 2w 美金买入 100 张 BTC 合约，则开仓时仓位价值=100\*100=1w 美金，并在币价 2.5w 美金时卖出，则这个操作的盈亏是：

$$
(1/20000-1/25000)*100*100=0.1BTC
$$

盈亏是 0.1BTC\*25000 = 2500USDT

也就是反向合约中挣到的 BTC 如果以平仓时价格卖出，则与正向合约挣到的 USDT 相等

正向合约与开仓平仓价差的关系是线性的，但是反向合约不是，反向合约的关系是凸函数的关系

强平的基本原理：`亏损 = 保证金`，就会触发爆仓

在正向合约做多的场景中，开仓时仓位价值=合约面值*张数*开仓价，强平时仓位价值=合约面值*张数*强平价，当仓位损失=（开仓价-强平价）*合约面值*张数=保证金，仓位被强平

已知：合约面值*合约张数*标记价格=杠杆倍数\*保证金数量

下面的`N`是杠杆倍数，`O`是开仓价格，强平价是`L`，保证金是`M`

即可推导出：强平价=1/杠杆倍数，表明开仓价跌了 1/N 就会触发爆仓

在上面的例子中，开仓价为 2w 美金，2 倍杠杆的情况下，则价格到 1w 美金就爆仓，如果是 50 倍杠杆，则价格到 19600 美金就爆仓

做空的情况也是一样，价格涨了 1/N 就爆仓

再看看反向合约

做多时：开仓时仓位价值=O*N*M，平仓时仓位价值=L*N*M，则亏损=（O-L）*N*M，保证金价值=L*M，所以当（O-L）*N*M=L*M，就会触发强平

上面的公式推导一下，得出：L=O（1-1/N+1），也就是说做多时开仓价跌 1/N+1 就爆仓，

做空时：开仓仓位价值=O*N*M，平仓时仓位价值=L*N*M，亏损=（L-O）*N*M，保证金价值=L*M，所以当（L-O）*N*M=L*M，就触发强平

推导为：L=O（1+1/N-1），就是说做空时开仓涨 1/N-1 就爆仓，2 倍杠杆，即价格涨 50%就会爆仓，如果时 1 倍杠杆，则永不爆仓，得出结论：

**反向合约，一倍做空，永不爆仓**

## 资金费率

资金费率每 8 小时结算一次，分别是 0 点、8 点、16 点

只哟再结算时间持有仓位，才会进行结算

<aside>
<img src="/icons/cow_yellow.svg" alt="/icons/cow_yellow.svg" width="40px" /> 为什么要有资金费率

</aside>

用于维持合约价格与资产现货价格的平衡的机制，永续合约是没有到期日的金融衍生品，价格理论上会与现货价格保持一致，然而，由于市场波动，市场供需关系变化等因素，永续合约的价格可能会偏离现货价格，因此资金费率就是用来调整永续合约的价格，使其与现货价格保持一致的手段，通过经济刺激的方式影响市场参与者：

正资金费率：当永续合约的价格高于现货价格时，资金费率为正，这意味着多头看涨持仓者需要向空头支付费用，这种机制鼓励更多的市场参与者做空，以期降低永续合约的价格，使其向现货价格靠拢

负资金费率：当永续合约价格低于现货价格的时候，资金费率为负，此时，空头持仓需要向多头持仓者支付费用，这激励更多的市场参与者做多，以提升永续合约的价格。

那么，为什么一定要有这个资金费率呢，不能没有这个机制吗

首先，交易所的目的是鼓励市场参与者参与交易，提高市场效率，没有这个机制，市场的自我调节能力会减弱，而且没有这个机制的话也会导致更多的投机行为，因为交易者可以不受持有成本的影响长期持有头寸，最后，最重要的是，资金费率可以提高市场流动性

## 全仓/逐仓

两种交易模式：

开全仓的情况下，如果 A 账户内有 1w，花了 5k 开 BTC 多单，花了 3K 开了 ETH 多单，账户内留了 2k，如果此时暴跌，那么除了开的多单，账户内的余额（前提是同一币种，不同币种没有讨论价值）也会被自动用来补仓，直到价格回升或者跌倒谷底直接爆仓。因为此时保证金是共享的

开逐仓的情况下：每个保证金是独立的，互相不受影响，只需要手动单独添加保证金

## 做多还是做空

做多不仅仅是合约对赌收益，还有相应的币价上涨带来的收益，理论上收益无上限

做空的收益最高是 100%\*杠杆倍数，还得要承受币价下跌带来的无常损失

因此做多的收益会高于做空，而且做多也是提振市场信心，做空除了加剧 FOMO，毫无意义

## 期现套利

这是一种吃交易所资金费率的方式，交易者在资金费率为正的时候，同时买入永续合约和相应数量的现货，这样期望从多头支付给空头的资金费率中获利

常见的现货做多，合约做空，获取其中的空头资金费率

跨交易所套利：不同交易所的资金费率不同，因此可以吃掉这个价差

三角套利：多种资产品种进行 swap，最后会出现一个缺口，这个缺口可以作为套利空间