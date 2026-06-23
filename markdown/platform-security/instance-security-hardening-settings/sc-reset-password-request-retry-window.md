---
title: Maximize reset password request retry window duration \[Updated in Security Center 1.3\]
description: The password\_reset.request.retry\_window property controls the number of minutes before the count for password reset attempts refreshes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-security/instance-security-hardening-settings/sc-reset-password-request-retry-window.html
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
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
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|Denotes the length of time in minutes before the count for password attempts refreshes from the last request before the retry count is reset to zero.|
|Recommended value|Set to a positive integer value of **1440** or more. The default value is **1440** minutes.|
|Configuration type|Positive integer values.|
|Security risk|\(High\) If the property is not set to the recommended value of 1440 or more, then it could be possible to perform account brute force against password reset process.|
|Security risk rating|7.5|
|References|[Configure Password Reset properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/t_SetPwdResetProps.md)|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/instance-security-hardening-settings/sc-authentication.md)

