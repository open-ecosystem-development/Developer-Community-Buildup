# Google IAP does not work


### Issues:
Android app with integrated Google In-app Billing (IAP) SDK cannot work on non-GMS devices. The IAP subscribe/purchase buttons may trigger the error pop-up, crash or nothing happens.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Remarks |
| --- | --- | --- | --- | ---|
| 1   | Developer can create another version without Google IAP. | User will not see any error. | User cannot purchase using Google account and able to access the premium content. | Need to have a conversation with the developer to understand the priority to support their users without the Google IAB payment.
| 2   | Developer can use WebView with Google Pay for websites or their own web payment. |  User can still make the purchase using Google ID or credit card and access the paid content. | Developer needs to do a lot of work removing IAB SDK and switching to a web payment. It cost the developer resources to add and manage additional payment channels. | Need to understand if the developer has the resource and is willing to support non-GMS device users. Do not recommend if CP is not willing to do more work.
| 3   | Use Huawei IAP Kit for HMS devices. | Huawei users can pay and access the premium content. | Developer needs to do a lot of work adding support for HMS IAP SDK. It cost the developer resources to add and manage additional payment channels. Developer also needs to consider future maintenance and support for new ecosystem users. | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if CP is not willing to do more work. If the developer is willing to use HMS IAP, they might as well publish the app in AppGallery since they've already become a Huawei developer and merchant.