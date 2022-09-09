# Google Nearby service not available


### Issues:
Android apps with integrated GMS Nearby Service SDK cannot use the features on non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot use this feature. | Easy | Need to have a conversation with the developer to understand the priority to support GMS Nearby Service in their app before recommending it.
| 2   | Integrate Huawei Nearby kit | Huawei users can have and use the same services. | Developer needs to do some work adding support for HMS Push SDK. It cost the developer resources to add and manage additional SDK. Developer also needs to consider future maintenance and support for new ecosystem users. | Medium | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if they are not willing to do more work. If the developer is willing to use HMS Nearby, they might as well publish the app in AppGallery since they've already become a Huawei developer.