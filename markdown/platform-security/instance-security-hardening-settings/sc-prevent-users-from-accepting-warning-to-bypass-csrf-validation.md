---
title: Prevent users from accepting warning to bypass CSRF validation
description: Reduce the risk of Cross-Site Request Forgery \(CSRF\) by preventing users from accepting warning to bypass CSRF validation.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent users from accepting warning to bypass CSRF validation

Reduce the risk of Cross-Site Request Forgery \(CSRF\) by preventing users from accepting warning to bypass CSRF validation.

Enable CSRF token strict validation to prevent Cross-Site Request Forgery \(CSRF\) tokens from being reused, which may allow CSRF attacks.

Set the **glide.security.csrf.strict.validation.mode** system property value to **true** to enable CSRF token strict validation. If this property doesn’t exist on your System Properties \[sys\_properties\] table, the default value is **true** starting in Xanadu.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.security.csrf.strict.validation.mode|
|Plugin applicability|None|
|Security risk|Cross-site request forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack on any instance user by abusing the trust of the instance user. With the help of social engineering attacks, a user can submit a malformed request to the instance on behalf of the attacker.|
|Common Vulnerability Scoring System \(CVSS\) score|3.7|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|This remediation enables an extra validation step before the user submits a write request to the instance. It checks whether the current CSRF token has been used previously. If it has, then it prevents submission of further write requests.|
|Dependencies and prerequisites|None|
|Data type|Boolean|
|Base system value|true|
|Fallback value|true|
|Recommended value|true|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

