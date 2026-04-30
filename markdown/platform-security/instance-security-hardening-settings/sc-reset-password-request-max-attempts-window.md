---
title: Control Lockout Time for Invalid Password Reset Attempts \[Updated in Security Center 1.3 and 2.0\]
description: The password\_reset.request.max\_attempt\_window property controls the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the password\_reset.request.max\_attempt property.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Control Lockout Time for Invalid Password Reset Attempts \[Updated in Security Center 1.3 and 2.0\]

The **password\_reset.request.max\_attempt\_window** property controls the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the **password\_reset.request.max\_attempt** property.

The **password\_reset.request.max\_attempt\_window** property defines the number of minutes a user must wait to reset or change their password after exceeding the maximum number of unsuccessful attempts that is set with the **password\_reset.request.max\_attempt property**. A small number of minutes for the **password\_reset.request.max\_attempt\_window** property increases the risk of successfully brute forcing a password as a greater number of password reset attempts can be made. The default of 1440 minutes is recommended.

Ensure the property **password\_reset.request.max\_attempt\_window** is set to 1440 or greater.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.max\_attempt\_window**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Denotes the lockout period in minutes after the maximum number of unsuccessful password reset attempts has been met.|
|Recommended value|1440|
|Default value|1440|
|Configuration type|Positive integer values|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or less, then it could be possible to perform account brute force as the account will not be locked after a maximum number of wrong authentication attempts.|
|Security risk rating|7.5|
|References|[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

