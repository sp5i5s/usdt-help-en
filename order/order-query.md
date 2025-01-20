# 🔍Order Inquiry

> This interface allows merchants to actively query order information.

**URL：** /v1/orders/search

**Method：** POST

**Parameter Type:** application/json

**Parameter：**

| Field Name | Field Type | Required | Signature | Instruction
| --- | --- | --- | --- | --- |
| app_id | string  | True  | True | APP ID
|  merchant_order_no |  string | True  | True | Merchant order number
|  signature | string  |True  | True | Data signature

**返回值 data 参数：**

| Field Name | Field Type |  Instruction
| --- | --- | --- |
| app_id | string  | APP ID
|order_no | string | UPay order number
|  merchant_order_no |  string | Merchant order number
| amount| string  | Order amount, unit USDT / PYUSD
| status | string | Order status
|  attach |  string | User-defined data
| chain_type | string | Network: TRC20 ERC20  BEP20
|  created_at|  string | Order creation time
