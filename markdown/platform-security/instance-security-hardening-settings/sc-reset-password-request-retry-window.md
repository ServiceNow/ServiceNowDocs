---
title: Maximize reset password request retry window duration \[Updated in Security Center 1.3\]
description: The password\_reset.request.retry\_window property controls the number of minutes before the count for password reset attempts refreshes.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password request retry window duration \[Updated in Security Center 1.3\]

The **password\_reset.request.retry\_window** property controls the number of minutes before the count for password reset attempts refreshes.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.retry\_window**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Denotes the length of time in minutes before the count for password attempts refreshes from the last request before the retry count is reset to zero.|
|Recommended value|Set to a positive integer value of **1440** or more. The default value is **1440** minutes.|
|Configuration type|Positive integer values.|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or more, then it could be possible to perform account brute force against password reset process.|
|Security risk rating|7.5|
|References|[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

