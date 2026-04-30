---
title: Minimize failed login attempts for high assurance sessions
description: Decrease the likelihood of a brute force attack by minimizing failed login attempts for high assurance sessions.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-10"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize failed login attempts for high assurance sessions

Decrease the likelihood of a brute force attack by minimizing failed login attempts for high assurance sessions.

Use the **glide.zta.high\_assurance.session.max.login.failed\_attempts** system property to limit the number of failed authentication attempts allowed before users are logged out when re-authenticating through Continuous Authentication.

Set the value of this system property to a low value \(such as 5\) to decrease the likelihood of a brute force attack.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.zta.high\_assurance.session.max.login.failed\_attempts|
|Plugin applicability|Zero Trust - Continuous Authentication \(com.snc.zero\_trust\_continuous\_authentication\)|
|Security risk|A high number of allowed authentication attempts increases the likelihood of a brute force attack.|
|Common Vulnerability Scoring System \(CVSS\) score|3.3|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|Users are logged out of their sessions after the number of authentication failures selected in the property.|
|Dependencies and prerequisites|None|
|Data type|Integer|
|Base system value|5|
|Fallback value|5|
|Recommended value|5|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

