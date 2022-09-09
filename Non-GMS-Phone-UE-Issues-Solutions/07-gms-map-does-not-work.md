# GMS Map does not work


### Issues:
Android apps with integrated GMS Map SDK cannot show maps on non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable/hide this feature if it's not important. | User will not see any error. | User cannot use the map or be aware of the feature available on other GMS devices. | Easy | Need to have a conversation with the developer to understand the priority to support GMS Map in their app before recommending it.
| 2   | Use PWA APK or Quick App | Non-GMS device users can use the map feature from developer's website. | N/A | Easy | This solution works only if developer has a website with mobile layout, UI similar to native app and supports Google Map (or other map providers).
| 3   | Developer can use WebView with Google Map if possible. | User can still use the Google Map service. | Developer needs to do a lot of work removing GMS Map and switching to a WebView. | Medium | Need to understand why the developer picks GMS Map in the first place. Do not recommend before understanding the reasons.
| 4   | Developer can use 3rd-party maps which can work well on non-GMS devices |  User can still use the Map service. | Developer needs to do a lot of work removing GMS Map and switch to a new, 3rd-party map platform. It cost developer the resources to use and manage the platform (vs free/cheaper GMS Map). | Hard | Need to understand why the developer picks GMS Map in the first place. Do not recommend before understanding the reasons.
| 5   | Integrate Huawei Map kit | Huawei users can use the map feature. | Developer needs to do a lot of work adding support for HMS Map SDK. It cost the developer resources to add and manage additional map service. Developer also needs to consider future maintenance and support for new ecosystem users. | Hard | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if they are not willing to do more work. If the developer is willing to use HMS Map, they might as well publish the app in AppGallery since they've already become a Huawei developer.