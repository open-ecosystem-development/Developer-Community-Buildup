# Missing GPS pop-up


### Issues:
Android apps with integrated GMS SDK may pop up missing GPS messages on non-GMS devices.

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer can integrate use `isGooglePlayServicesAvailable` to hide/disable this message if it's not important on non-GMS devices. | User will not see any error. | User is not aware some GMS-dependent features are not working on their devices. | Easy | Need to have a conversation with the developer to understand the priority to show the missing GMS error in their app. Some developers have explicit intent to show the pop-up.