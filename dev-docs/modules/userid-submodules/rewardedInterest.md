---
layout: userid
title: Rewarded Interest ID
description: Rewarded Interest User ID Submodule
useridmodule: rewardedInterestIdSystem
---

[Rewarded Interest](https://www.rewardedinterest.com/) is an identity provider that empowers users to monetize and control the visibility of their identity to various ad providers through a browser extension.

This submodule transmits the Identity Token obtained from the browser extension into the oRTB request. The Identity Token is included only if the user has installed the extension and has authorized it to share their ID token.

The Identity Token itself does not reveal the user's identity, as it is encrypted and frequently refreshed. However, interested parties (such as DSPs, SSPs, and publishers) can use the Rewarded Interest Backend API to exchange the Identity Token for a CMAID (Consumer Mediated Advertising Identifier), a durable, cross-site, cross-device advertising identifier. The CMAID remains consistent across visits and devices enrolled by a Rewarded Interest user, unless they choose to reset or pause it.

Add this submodule to your Prebid.js wrapper with:

{: .alert.alert-info :}
gulp build --modules=userId,rewardedInterestIdSystem

## Rewarded Interest ID Configuration

<div class="table-responsive" markdown="1">
| Param under userSync.userIds[] | Scope | Type | Description | Example |
| --- | --- | --- | --- | --- |
| name | Required | String | The name of the Rewarded Interest user ID submodule. | `"rewardedInterestId"` |
{: .table .table-bordered .table-striped }
</div>

## Rewarded Interest ID Example

```javascript
pbjs.setConfig({
    userSync: {
        userIds: [{
            name: "rewardedInterestId"
        }]
    }
})
```
