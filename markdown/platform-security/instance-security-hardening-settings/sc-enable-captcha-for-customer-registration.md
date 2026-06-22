---
title: Enable CAPTCHA for customer registration
description: Reduce the risk of requests by malicious bots by enabling CAPTCHA for customer registration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-enable-captcha-for-customer-registration.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable CAPTCHA for customer registration

Reduce the risk of requests by malicious bots by enabling CAPTCHA for customer registration.

Use the **sn\_customerservice.captchaEnabled** system property to determine whether CAPTCHA validation is enabled for customer registration on the Customer Service Management Portal. Use CAPTCHA validation to help prevent potentially malicious bots from automatically submitting requests against an application.

Set the system property **sn\_customerservice.captchaEnabled** to **true** to enable CAPTCHA validation. If the property isn’t on the System Properties \[sys\_properties\] table, the default value is **true**.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|sn\_customerservice.captchaEnabled|
|Plugin applicability|Customer Service Management|
|Security risk|CAPTCHA validation helps prevent potentially malicious bots from automatically submitting requests against an application.|
|Common Vulnerability Scoring System \(CVSS\) score|3.7|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|Registering users may have a negative experience from having to pass the CAPTCHA validation.|
|Dependencies and prerequisites|None|
|Data type|Boolean|
|Base system value|**true**|
|Fallback value|**true**|
|Recommended value|**true**|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

