# GMS location services are not working


### Issues:
Android apps with integrated GMS Location SDK cannot get the user's geo-coordinates on non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot use the location and map services. | Easy | Need to have a conversation with the developer to understand the priority to support location and map services in their app. Do not recommend if developer has a high priority to support it.
| 2   | Use PWA APK or Quick App and native browser's location API | Non-GMS device users can use the location feature from native browser location API | N/A | Easy | This solution works only if developer has a website with mobile layout, UI similar to native app and supports Google map (or other map providers).
| 3   | Developer can use native Android Location API. |  User can still get the location geo-coordinates.  | The location data may not be as accurate as the OEM location kit. | Easy | Need to understand why the developer picks GMS Location in the first place. Do not recommend before understanding the reasons.
| 4   | Developer can integrate 3rd-party or OEM push SDK like Huawei Location Kit |  User can still get the location geo-coordinates.  | Developer needs to do some work removing GMS Location and switch to a 3rd-party SDK. It cost developer the resources to maintain and support additional SDK. | Medium | Need to understand why the developer picks GMS Location in the first place. Do not recommend before understanding the reasons. If the developer is willing to use HMS Location, they might as well publish an HMS app in AppGallery since they've already become a Huawei developer.
