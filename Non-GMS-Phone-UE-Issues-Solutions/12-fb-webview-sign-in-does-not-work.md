# Facebook WebView sign in does not work


### Issues:
Android apps that have Facebook WebView sign in method fail to sign in Facebook users. This issue is not related to missing GMS.

### Root Cause:
On 10/05/2021, Facebook deprecated its support for Facebook login authentication on Android embedded browsers (WebView) and the Passwordless flow is no longer an available option for developers. 

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | All developers need to make changes in their code to handle Facebook sign in. | User can use the website for Facebook account sign in. | Developer's web team needs to have resources to modify the sign in method. | Easy | Need to have a conversation with the developer to understand the priority to support this feature.
