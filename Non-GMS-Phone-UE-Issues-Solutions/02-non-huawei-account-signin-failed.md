# Non-Huawei account sign-in failed


### Issues:
Non-Huawei Account sign-in does not work on non-GMS devices.

### Root Cause:
GPS is not installed on the devices or Non-Huawei sign-in method is incompatible on the non-GMS devices.

### Possible Solutions:

|     | Solutions | Pros | Cons | Remarks |
| --- | --- | --- | --- | ---|
| 1   | Possible use of Google Login REST API to sign into 3rd-party Account | User will be able to sign-in using 3rd-party ID. | Developer needs to change the code to use Google Login REST API. | Need to have a conversation with the developer to understand if they are willing and have the resource to do the work.
