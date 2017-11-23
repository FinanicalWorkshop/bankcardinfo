# (银行卡号) => { 银行名称, 银行卡类型 }

## 用法：
推荐使用Promise方式调用，如查到银行卡相关信息，在成功回调中传入json格式对象；如未查到，成功回调中传入空对象。

调用：
```js
import BIN from 'bank-card-data'

BIN.getBankBin('6227003320240034988').then(data => {
    // do somthing
})
```

data格式：
```js
{
  bankName:"中国工商银行",
  bankCode:"ICBC",
  cardType:"DC",
  cardTypeName:"储蓄卡"
}
```



## 说明

* Forked from [navyxie/bankcardinfo](https://github.com/navyxie/bankcardinfo)
* 去掉了支付宝API调用，方便浏览器端运行
* 去掉了bluebird dependency