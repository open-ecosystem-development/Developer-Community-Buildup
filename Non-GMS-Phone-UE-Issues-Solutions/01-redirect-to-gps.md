# Redirect to GPS


### Issues:
Redirects to GPS do not work (for examples: rating apps, downloading apps).

### Root Cause:
GPS is not installed on the devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Remarks |
| --- | --- | --- | --- | ---|
| 1   | Developer to disable this feature if it's not important. | User will not see any error or redirect. | Developer may lose the ability to redirect users to GPS. | Need to have a conversation with the developer to understand the priority to support the redirect to GPS in their app.
| 2   | Developer can use  `isGooglePlayServicesAvailable` to hide the redirect to GPS banner, buttons, etc. on the non-GMS devices. |  Non-GMS device users will not see this error message. The amount of work is very minimal (about 10 lines of code). The solution is already available in GMS SDK, it does not require additional 3rd-party solutions.  | Developer needs to do some work to show/hide the redirect logic. Developer may not want to do any work. | Need to understand if the developer is willing to support non-GMS device users and if they are willing to do some work to support it. Do not recommend before understanding the reasons.
| 3   | Detect the GMS, HMS availability (combine solution #2 above) and redirect/show/open the correct app store. [https://stackoverflow.com/questions/53705612/how-to-open-the-huawei-appgallery-directly](https://stackoverflow.com/questions/53705612/how-to-open-the-huawei-appgallery-directly) | User can see the correct app store on different devices. | The developer must be convinced to support other app stores, and their app must be available in other app stores (like AppGallery). | Need to make sure to communicate to the developer the benefits clearly.