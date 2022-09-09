# Desktop web layout being displayed in Quick App or PWA APK


### Issues:
Quick App or PWA APK that uses developer's website URL to display app content cannot show mobile layout or UI. This issue is not related to missing GMS.

### Root Cause:
1. Quick App (H5) uses a desktop user agent to request the developer's website.
2. PWA APK users turn on the desktop mode in their default browser (such as Huawei Browser). 
3. Developer's website has no mobile or partial mobile web layout.
4. Developer's website has a mobile layout but cannot detect the mobile browser user agent correctly.

### Possible Solutions:

|     | Solutions | Pros | Cons | Difficulty | Remarks |
| --- | --------- | ---- | ---- | ---------- | ------- |
| 1   | Developer to provide mobile layout website. | User can see and use the website content like a native user. | Developer's web team needs to have resources to revamp their website, or add support for mobile layout and user agent requests. | Medium to hard | Need to have a conversation with the developer to understand the priority to support mobile web layout and detecting user agent.
