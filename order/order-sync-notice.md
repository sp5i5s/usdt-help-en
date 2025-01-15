# 🔔Order Asynchronous Notification

> After the order is completed, the system will automatically send a notification message to the callback address (notifyUrl) associated with the order to inform you of the final status of the order.

**Method：**POST

**Parameter Type：**application/json

**Parameter：**

| Field Name | Field Type | Required | Signature | Instruction
| --- | --- | --- | --- | --- |
| appId | string  | True  | True |  APP ID
|  merchantOrderNo |  string | True  | True | Merchant order number
|  chainType | string  |True  | True | Network: 1: Tron (TRC20)2: PayPal (PYUSD)3: Ethereum (ERC20)  
|  fiatAmount| string  |True  | True | Amount, Unit: USDT / PYUSD
|  attach| string   |False  | False | User-defined data will be returned unchanged when calling back to notifyUrl.
|  notifyUrl| string   |True  | True | 接收异步通知的回调地址。必须为可直接访问的 URL，不能带参数、session 验证、csrf 验证
|  redirectUrl| string   |False  | False | 支付成功后，前端重定向地址。务必包含 http:// 或 https:// 开头
|  signature | string  |True  | True | Data signature

## Notification return：

After receiving the notification information, the merchant will output OK or ok (php example: echo "OK";) in the body of the response body. Otherwise, the point-to-point notification will be sent 5 times.

## Notification retry policy

If the first notification fails