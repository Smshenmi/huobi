# 火币 Javascript SDK（非官方版)
这个项目的目的是提供一个JS环境的火币API接口

## 免责申明
本项目是出于个人兴趣爱好而开发制作，因为本项目涉及到货币交易，对使用者而言存在一定风险，因此在此特此申明，因为使用本项目而对使用者造成财产损失，本项目以及项目成员对此概不负责，一旦您使用本项目便代表您同意本免责申明，否则您无权使用本项目

## 联系我
如果在使用当中有问题可以联系我

**邮箱**: [23489490@qq.com](mailto:23489490@qq.com)

## 安装方法
```
npm install --save huobi
```

## 使用指南
```Javascript
const Huobi = require('huobi')

let huobi = new Huobi({serectKey:'Your Serect Key', accessKey:'Your Access Key'})

huobi.getAccountInfo()
.then(data => console.log(data))
.catch(err => console.log(err))

...
```

## API指南

> 注意！方法的参数都是使用键值对形式传递，所以你不需要记住参数的顺序

### buy | 委托购买
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 购买的币种类型，比特币=1，莱特币=2 |
| price | Number | Yes | 预定购买的价格 |
| amount | Number | Yes | 购买的数量 |
| pwd | String | No | 如果设置了交易密码，那就要设置该参数|
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币

### buyMarket | 按照市场价购买
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 购买的币种类型，比特币=1，莱特币=2 |
| price | Number | Yes | 预定购买的价格 |
| amount | Number | Yes | 购买的数量 |
| pwd | String | No | 如果设置了交易密码，那就要设置该参数|
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币

### sell | 委托卖出
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 卖出的币种类型，比特币=1，莱特币=2 |
| price | Number | Yes | 预定卖出的价格 |
| amount | Number | Yes | 卖出的数量 |
| pwd | String | No | 如果设置了交易密码，那就要设置该参数|
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币


### sellMarket | 按照市场价卖出
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 卖出的币种类型，比特币=1，莱特币=2 |
| amount | Number | Yes | 卖出的数量 |
| pwd | String | No | 如果设置了交易密码，那就要设置该参数|
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币

### getOrders | 获取所有当前正在委托的订单
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 卖出的币种类型，比特币=1，莱特币=2 |
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币

### getNow | 获取当前的市场价格
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 卖出的币种类型，比特币=1，莱特币=2 |
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币

### cancelOrder | 取消订单
| 参数 | 类型 | 是否必要 | 说明 |
|-----|------|---------|-----|
| type | Integer | Yes | 卖出的币种类型，比特币=1，莱特币=2 |
| orderId | String | Yes | 订单ID|
| market | String | No| 交易的市场，人民币=cny，美元=usd，默认是人民币
