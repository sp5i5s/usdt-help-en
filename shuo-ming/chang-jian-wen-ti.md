# 📌 FAQ

UPay API FAQ. If you have any other questions, please contact customer service.

## Insufficient balance

Merchants need to pre-charge their balance to pay the collection fee to our platform. Please check the merchant's homepage for the specific collection fee rate. 

Recharge tutorial：[https://docs.upay.ink/help/cn/howtouse/recharge](https://docs.upay.ink/help/cn/howtouse/recharge?utm_medium=chat&utm_campaign=link-shared-in-chat&utm_source=livechat.com&utm_content=upay.ink)

## Require collection address

All order amounts will go directly to the merchant's collection address. 

collection address configuration tutorial：[https://docs.upay.ink/help/cn/howtouse/receiving-address](https://docs.upay.ink/help/cn/howtouse/receiving-address?utm_medium=chat&utm_campaign=link-shared-in-chat&utm_source=livechat.com&utm_content=upay.ink)

## Invalid signature

Please make sure that the field names are consistent with those described in the document. Please check whether the fields that do not need to be signed have been signed. Please pay attention to the "Required" and "Signature" columns in the parameter description.

## Response after receiving callback

After receiving the notification information, the merchant outputs OK or ok in the body of the response (PHP example: echo "OK";), otherwise the point-to-point notification will be sent repeatedly 5 times.