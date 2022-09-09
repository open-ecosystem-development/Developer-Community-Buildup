# FCM & GMS push notifications not working.


### Issues:
Android apps with integrated FCM SDK cannot receive push notification messages on non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer disable this feature if it's not important. | User will not see any error. | User cannot receive push notification messages. | Easy | Need to have a conversation with the developer to understand the priority to support FCM in their app before recommending it.
| 2   | Developer can integrate 3rd-party or OEM push SDK like Airship, OneSignal, Huawei Push Kit |  User can still receive push notifications.  | Developer needs to do a lot of work removing FCM and switch to a new, 3rd-party platform. It cost developer the resources to use and manage the platform (vs free FCM). | Hard | Need to understand why the developer picks FCM in the first place. Do not recommend before understanding the reasons.
| 3   | Work with the device manufacturer (OEM) to add the developer's app to the OS whitelist. | User can still receive push notifications. | The whitelisting process can be lengthy and complicated. Developer may not want to wait or cooperate. | Medium (for OEM) | Need to make sure the OEM is willing to whitelist. Communicate the process to the developer clearly, and set up the right expectation (time, cost, effort).
| 4   | Integrate Huawei Push kit | Huawei users can pay and receive push notifications. | Developer needs to do a lot of work adding support for HMS Push SDK. It cost the developer resources to add and manage additional push channels. Developer also needs to consider future maintenance and support for new ecosystem users. | Hard | Need to understand if the developer has the resource and is willing to support HMS device users. Do not recommend if they are not willing to do more work. If the developer is willing to use HMS Push, they might as well publish the app in AppGallery since they've already become a Huawei developer.