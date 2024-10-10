---
layout: userid
title: Rewarded Interest ID
description: Rewarded Interest User ID Submodule
useridmodule: rewardedInterestIdSystem
---

**Rewarded Interest Advertising ID aka CMAID**: A durable, cross-site, cross-device advertising identifier. This ID remains consistent across visits and across a Rewarded Interest user’s various enrolled devices, unless they reset or pause it.

**CMAID**: An acronym for Consumer Mediated Advertising Identifier

Add support for Rewarded Interest ID to your Prebid.js package using:

{: .alert.alert-info :}
gulp build --modules=userId,rewardedInterestIdSystem

## Rewarded Interest ID Configuration

<div class="table-responsive" markdown="1">
| Param under userSync.userIds[] | Scope | Type | Description | Example |
| --- | --- | --- | --- | --- |
| name | Required | String | The name of this module. | `"rewardedInterestId"` |
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
