# GMS ML Scan does not work


### Issues:
Android app with integrated GMS ML SDK cannot scan images (such as QR codes) in non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot scan the images and use ML features. | Easy | Need to have a conversation with the developer to understand the priority to support GMS ML services in their app before recommending it.
| 2   | Developer can integrate 3rd-party or OEM push SDK like ZXing, Huawei Scan Kit (full) |  User can still use scan features like QR codes. | Developer needs to do a lot of work removing GMS ML SDK and switch to a new, 3rd-party SDK. It cost developer the resources to use and manage the SDK. | Medium | Need to understand why the developer picks GMS ML SDK in the first place. Do not recommend before understanding the reasons.