---
title: Limit Invalid Password Reset Attempts \[Updated in Security Center 1.3 and updated in 2.0\]
description: The password\_reset.request.max\_attempt is used to control the maximum number of unsuccessful attempts that a user can reset or change their password before being locked out for a specified period of time.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Limit Invalid Password Reset Attempts \[Updated in Security Center 1.3 and updated in 2.0\]

The **password\_reset.request.max\_attempt** is used to control the maximum number of unsuccessful attempts that a user can reset or change their password before being locked out for a specified period of time.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.max\_attempt**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Denotes the maximum number of unsuccessful password reset attempts that can be taken before the user is locked out of password reset process. The lockout period is determined by the value in **password\_reset.request.max\_attempt\_window**.|
|Recommended value|Set to a positive integer value less than three. The default value is **3**. When you determine the limit for the upper range of the property, consider the task that the user is performing.|
|Configuration type|Positive integer values|
|Security risk|\(High\) If the property is not set to the recommended value of "**3**" or other reasonable small value, then it could be possible to perform a brute force attack against the password reset process.|
|Security risk rating|7.5|
|References|[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)|

**Parent Topic:**[Authentication](sc-authentication.md)

