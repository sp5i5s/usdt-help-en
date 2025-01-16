# 📥 Submit Order

> Used to generate payment data of specified digital currency, merchants can guide users to jump to the UPay checkout counter for payment through the payment link. After the user's payment is successful, the system will immediately issue a callback notification. 

> Note: Users must pay strictly according to the order amount. If the payment amount is inconsistent, the order will not be processed.

**URL：**/v1/order/apply

**Method：**POST

**Parameter Type：**application/json

**Parameter ：**

| Field Name        | Field Type | Required | Signature | Instruction |
| --------------- | -------- | -------- | -------- | ----------------------------------------------------------------------------------- |
| appId           | string   | True       | True       | APP ID                                                                              |
| merchantOrderNo | string   | True       | True       | The order number generated independently by the merchant must be unique on the merchant's end.                                        |
| chainType       | string   | True       | True       | Network: 1: Tron (TRC20) 2: Ethereum (ERC20)3: PayPal (PYUSD)                                      |
| fiatAmount      | string   | True       | True       | Legal currency amount, accurate to 4 decimal places                                                      |
| attach          | string   | False       | False       | User-defined data, if it is not empty, will be returned as is when calling back to notifyUrl.                                |
| notifyUrl       | string   | True       | True       | The callback address for receiving asynchronous notifications. It must be a directly accessible URL and cannot contain parameters, session verification, or csrf verification. |
| redirectUrl     | string   | False       | False       | After the payment is successful, the front-end redirects the address. Be sure to include "http://" or "https://" at the beginning                       |
| signature       | string   | True       | True       | Data signature                                                                            |

**Return value data parameter：：**

| Field Name        | Field Type | Instruction                                         |
| --------------- | -------- | -------------------------------------------- |
| appId           | string   | APP ID                                       |
| orderNo         | string   | UPay order number                                  |
| merchantOrderNo | string   | Merchant order number                                   |
| crypto          | string   | Order amount, unit USDT / PYUSD                  |
| status          | string   | Order status                                     |
| payUrl          | string   | Cashier address, merchants can jump directly to this address for users to pay. |
