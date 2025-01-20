# 📂 Order Paging Query

> This interface allows merchants to query order information in pages, with a maximum of 100 items per page.

**URL：** /v1/orders/queryall

**Method：** POST

**Parameter Type：** application/json

**Parameter：**

| Field Name | Field Type | Required | Signature | Instruction
| --------- | -------- | -------- | -------- | -------- |
| appId     | string   | True       | True       |  APP ID   |
| pageNo    | string   | True       | True       |  Pages     |
| signature | string   | True       | True       | Data signature |

**Return value data parameter：**

| Field Name | Field Type | Instruction     |
| -------- | -------- | -------- |
| total    | string   | Total     |
| current_page   | string   | Pages     |
| last_page | string   | Number of entries per page |
| data     | []array  | Order list |

**Return value list Parameters:**
| Field Name | Field Type | Instruction
| --- | --- | --- |
| order_id | string | APP ID
|order_no | string | UPay order number
| merchant_order_no | string | Merchant order number
| amount| string | Order amount, unit USDT / PYUSD
| status | string | Order status
| attach | string | User-defined data
| chain_type | string | Network: TRC20 ERC20  BEP20
| createdAt| string | Order creation time
