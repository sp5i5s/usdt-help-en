# 📌 FAQ

UPay API FAQ. If you have any other questions, please contact customer service.

## Insufficient balance

Merchants need to pre-charge their balance to pay the collection fee to our platform. Please check the merchant's homepage for the specific collection fee rate. 

## Require collection address

All order amounts will go directly to the merchant's collection address. 

## Invalid signature

Please make sure that the field names are consistent with those described in the document. Please check whether the fields that do not need to be signed have been signed. Please pay attention to the "Required" and "Signature" columns in the parameter description.

## Response after receiving callback

After receiving the notification information, the merchant outputs OK or ok in the body of the response (PHP example: echo "OK";), otherwise the point-to-point notification will be sent repeatedly 5 times.