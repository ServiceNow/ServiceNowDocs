---
title: Enable account recovery \[Updated in Security Center 1.3 and 1.5\]
description: The glide.sso.acr.enabled property controls the account recovery feature.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable account recovery \[Updated in Security Center 1.3 and 1.5\]

The **glide.sso.acr.enabled** property controls the account recovery feature.

Set **glide.sso.acr.enabled** to the recommended value of **true** to allow account recovery by userid possible. Set the value to **false** to disallow account recovery by userid.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.sso.acr.enabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Controls the account recovery by userid feature.|
|Recommended value|True \(default\)|
|Configuration type|Boolean|
|Security risk|Critical \(Without this property enabled, users will not be allowed to recover their account by userid.|
|Security risk rating|9.1|
|References|See [Account recovery \(ACR\)](../../../integrate/single-sign-on/concept/sso-acct-recovery.md) for additional information.|

**Parent Topic:**[Authentication](sc-authentication.md)

