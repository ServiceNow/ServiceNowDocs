---
title: Minimize reset password request expiration duration \[Updated in Security Center 1.3\]
description: The password\_reset.request.expiry denotes the time period in minutes during which a user must perform the password reset process.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password request expiration duration \[Updated in Security Center 1.3\]

The **password\_reset.request.expiry** denotes the time period in minutes during which a user must perform the password reset process.

**Note:** The setting for the**password\_reset.request.expiry** property takes precedence over the setting for **glide.pwd\_reset.onetime.token.validity**property that has a 12 hour default.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.expiry**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Denotes the time period in minutes during which a user must perform the password reset process.|
|Recommended value|Set to an integer of **10** or less. The default value is 10.|
|Configuration type|Integer values|
|Security risk|\(Moderate\) If the property is not set to the recommended value of 10 or less, then it increases the opportunity for someone else to guess and use the request and attempt to reset the password.|
|Security risk rating|4.2|
|References|[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

