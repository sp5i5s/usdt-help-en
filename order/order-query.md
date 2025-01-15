# 🔍Order Inquiry

> This interface allows merchants to actively query order information.

**URL：**/v1/order/search

**Method：**POST

**Parameter Type:**application/json

**Parameter：**

| Field Name | Field Type | Required | Signature | Instruction
| --- | --- | --- | --- | --- |
| appId | string  | True  | True | APP ID
|  merchantOrderNo |  string | True  | True | Merchant order number
|  signature | string  |True  | True | Data signature

**返回值 data 参数：**

| Field Name | Field Type |  Instruction
| --- | --- | --- |
| appId | string  | APP ID
|orderNo | string | UPay order number
|  merchantOrderNo |  string | Merchant order number
| crypto| string  | Order amount, unit USDT / PYUSD
| status | string | Order status
|  attach |  string | User-defined data
|  createdAt|  string | Order creation time
