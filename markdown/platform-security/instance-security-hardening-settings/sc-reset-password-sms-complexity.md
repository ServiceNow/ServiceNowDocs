---
title: Maximize reset password SMS complexity \[Updated in Security Center 1.3\]
description: The password\_reset.sms.default\_complexity property controls the minimum required SMS code verification size required during password reset.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password SMS complexity \[Updated in Security Center 1.3\]

The **password\_reset.sms.default\_complexity** property controls the minimum required SMS code verification size required during password reset.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.sms.default\_complexity**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Denotes the SMS code verification size required during password reset.|
|Recommended value|6|
|Default value|4|
|Configuration type|Integer value greater than zero|
|Security risk|\(Low\) If the property is not set to the recommended value, then a weak SMS validation token is used. This increases the possibility of token guessing which could lead to account takeover.|
|Security risk rating|3.8|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

