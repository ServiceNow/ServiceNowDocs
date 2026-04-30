---
title: Disable inbound emails for locked out users
description: Use the glide.pop3.process\_locked\_out property to control inbound email actions for locked out, active users.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable inbound emails for locked out users

Use the **glide.pop3.process\_locked\_out** property to control inbound email actions for locked out, active users.

Set this property to **false** to disable inbound emails for locked out users.

**Note:** Consider the security implications of allowing users from untrusted domains, and why they were locked out, before allowing emails from them to trigger inbound email actions.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.pop3.process\_locked\_out**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|This property controls inbound email actions for locked out users.|
|Data type|boolean|
|Recommended value|false|
|Default value|false|
|Security risk|\(High\) When you set this property to **true**, there may be an information disclosure as inbound emails would be received by users with locked accounts.|
|Security risk rating|7.5|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

