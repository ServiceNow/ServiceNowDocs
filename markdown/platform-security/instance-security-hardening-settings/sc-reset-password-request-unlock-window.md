---
title: Maximize reset password request unlock window duration \[Updated in Security Center 1.3\]
description: The password\_reset.request.unlock\_window property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-reset-password-request-unlock-window.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
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
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|It denotes the time period in minutes that a user must wait after successfully resetting the password to reset the password again.|
|Recommended value|1440|
|Default value|1440|
|Configuration type|Positive integer values|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or greater, then it increases the opportunity of a malicious actor to brute force password access using automatic tools.|
|Security risk rating|5.9|
|References|[Configure Password Reset properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see .

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

