---
title: Maximize reset password request unlock window duration \[Updated in Security Center 1.3\]
description: The password\_reset.request.unlock\_window property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password request unlock window duration \[Updated in Security Center 1.3\]

The **password\_reset.request.unlock\_window** property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.

This property controls the number of minutes a user must wait to start a reset request after the last successful unlock account. If **password\_reset.request.unlock\_window** is not set to the recommended value of 1440 or more, it increases the opportunity for a malicious actor from brute forcing the user's password using automated tools.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.unlock\_window**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|It denotes the time period in minutes that a user must wait after successfully resetting the password to reset the password again.|
|Recommended value|1440|
|Default value|1440|
|Configuration type|Positive integer values|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or greater, then it increases the opportunity of a malicious actor to brute force password access using automatic tools.|
|Security risk rating|5.9|
|References|[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

