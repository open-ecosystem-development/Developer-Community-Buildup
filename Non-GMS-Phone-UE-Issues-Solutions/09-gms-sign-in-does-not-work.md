# GMS sign in does not work


### Issues:
Android app with integrated GMS Auth/Sign-in SDK cannot receive sign-in Google ID on non-GMS devices. Error messages may pop-up or crash the app.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot sign-in using Google ID. | Easy | Need to have a conversation with the developer to understand the priority to support Google accounts in their app before recommending it.
| 2   | Developer can integrate Google Auth REST API | User can still sign in using Google accounts | Developer needs to do a lot of work removing Google Auth SDK and switching to REST API. It cost developer the resources to use and manage additional login methods. | Medium | Need to understand why the developer picks SDK in the first place. Do not recommend before understanding the reasons.
| 3   | Integrate Huawei Account kit | Huawei users can use the account feature. | Developer needs to do a lot of work adding support for HMS Account SDK. It cost the developer resources to add and manage additional account services. Developer also needs to consider future maintenance and support for new ecosystem users. | Hard | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if they are not willing to do more work. If the developer is willing to use HMS Account, they might as well publish the app in AppGallery since they've already become a Huawei developer.