# GMS Mobile Vision does not work


### Issues:
Android app with integrated GMS Mobile Vision SDK cannot scan on non-GMS devices. Pop-up message: “XXXX won’t run without GPS, which are not supported by your device”.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot use the scan feature. | Easy | Need to have a conversation with the developer to understand the priority to support it in their app before recommending it.
| 2   | Developer can integrate 3rd-party or OEM push SDK like Zxing |  User can still use the scan feature.  | Developer needs to do a lot of work removing Mobile Vision and switch to a new, 3rd-party SDK. It cost developer the resources to use and manage the other SDK. | Medium | Need to understand why the developer picks GMS MV in the first place. Do not recommend before understanding the reasons.
| 3   | Integrate Huawei Scan kit (full kit) | Huawei users can use the scan feature. | Developer needs to do a lot of work adding support for HMS Scan SDK. It cost the developer resources to add and manage additional services. Developer also needs to consider future maintenance and support for new ecosystem users. | Medium | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if they are not willing to do more work. If the developer is willing to use HMS Scan, they might as well publish the app in AppGallery since they've already become a Huawei developer.