# 📂 Order Paging Query

> This interface allows merchants to query order information in pages, with a maximum of 100 items per page.

**URL：** /v1/order/queryall

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
| pageNo   | string   | Pages     |
| pageSize | string   | Number of entries per page |
| list     | []array  | Order list |

**Return value list Parameters:**
| Field Name | Field Type | Instruction
| --- | --- | --- |
| appId | string | APP ID
|orderNo | string | UPay order number
| merchantOrderNo | string | Merchant order number
| crypto| string | Order amount, unit USDT / PYUSD
| status | string | Order status
| attach | string | User-defined data
| createdAt| string | Order creation time
