---
title: Enable CAPTCHA in password reset
description: Use the password\_reset.captcha.ignore property to enable or disable requiring a CAPTCHA challenge when a user resets their password.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-enable-captcha-in-password-reset.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable CAPTCHA in password reset

Use the **password\_reset.captcha.ignore** property to enable or disable requiring a CAPTCHA challenge when a user resets their password.

Set **password\_reset.captcha.ignore** to the recommended value of **false** to require a CAPTCHA challenge for a user to reset their password. Set the value to **true** to ignore the CAPTCHA option for a password reset.

CAPTCHAs help prevent automation attacks by prompting the user for a challenge-response that is not easily answered by automated systems. If CAPTCHA is disabled, an attacker may be more successful during automated attacks against the password reset feature.

**Note:** This property is used for password reset automation only.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**password\_reset.captcha.ignore**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|This property is used to enable or disable CAPTCHA validation during password reset.|
|Recommended value|false|
|Configuration type|Boolean|
|Security risk|\(Moderate\) Unideal value may result in security vulnerability.|
|Security risk rating|5.5|

To learn more about adding or creating a system property, see .

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

