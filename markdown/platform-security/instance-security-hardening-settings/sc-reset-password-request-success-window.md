---
title: Minimize reset password request success window duration \[Updated in Securty Center 1.3\]
description: The password\_reset.request.success\_window property controls the number of minutes a user must wait to reset or change their password again after successfully resetting the password. The user will be blocked to reset the password again for the specified duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-reset-password-request-success-window.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password request success window duration \[Updated in Securty Center 1.3\]

The **password\_reset.request.success\_window** property controls the number of minutes a user must wait to reset or change their password again after successfully resetting the password. The user will be blocked to reset the password again for the specified duration.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.request.success\_window**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|It denotes the time period in minutes that a user must wait after successfully resetting the password to reset the password again.|
|Recommended value|1440|
|Default value|1440|
|Configuration type|Positive integer values|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or less,then it increases the opportunity of someone else abusing the password reset functionality to gain unauthorized access to a user account.|
|Security risk rating|4.9|
|References|[Configure Password Reset properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see .

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

