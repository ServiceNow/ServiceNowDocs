---
title: Disable locked form elements debugging
description: Here's the description for glide.security.explain.write.locks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Disable locked form elements debugging

Here's the description for **glide.security.explain.write.locks**.

Set **glide.security.explain.write.locks** to the recommended value of **false** to prevent the display of explanation of locked form elements. Set the value to **true** to display the explanation of locked form elements.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.explain.write.locks**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Configuration](sc-configuration.md)|
|Purpose|Limits display behavior of SecurityDebugger without dependence on other properties.|
|Recommended value|false|
|Default value|false|
|Configuration type|Boolean|
|Security risk|\(Low\) Will prevent the display of the explanation on locked form elements. This makes the application slightly more secure, as less information is being provided by the security debugger.|
|Security risk rating|3.5|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

