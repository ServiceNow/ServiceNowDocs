---
title: Enable Captcha for External User Registration \[Updated in Security Center 1.3 and 1.5\]
description: The sn\_ext\_usr\_reg.captchaEnabled controls if CAPTCHA will be validated for external user registration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-enable-captcha-external-user-registration.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable Captcha for External User Registration \[Updated in Security Center 1.3 and 1.5\]

The **sn\_ext\_usr\_reg.captchaEnabled** controls if CAPTCHA will be validated for external user registration.

Set **sn\_ext\_usr\_reg.captchaEnabled** to the recommended value of **true** to help prevent automatic account creation attacks with requiring CAPTCHA for external user registration. Set the value to **false** to not require CAPTCHA for external user registration.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**sn\_ext\_usr\_reg.captchaEnabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|This property is used to enable or disable CAPTCHA validation while doing external user registration on portals like CSP, Community. This is also used in store apps like VAM and CSM Guest Walkup to enable/disable captcha.|
|Recommended value|True|
|Configuration type|Boolean|
|Security risk|\(Low\) The property controls CAPTCHA enablement in external user registration. Unideal value may result in security vulnerability.|
|Security risk rating|3.7|

To learn more about adding or creating a system property, see .

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

