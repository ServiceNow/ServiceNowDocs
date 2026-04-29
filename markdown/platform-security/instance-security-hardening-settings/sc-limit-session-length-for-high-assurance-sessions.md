---
title: Limit session length for high assurance sessions
description: Reduce the risk of account takeover in high assurance sessions by limiting session length
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit session length for high assurance sessions

Reduce the risk of account takeover in high assurance sessions by limiting session length

Reduce the risk of account takeover in high assurance sessions by limiting the length of the session. After the specified length of time, end-users must re-authenticate.

Use the **glide.zta.high\_assurance.session.timeout** system property to set a time, in minutes, after which users must re-authenticate. The value of this property must be between 1 and 480 minutes. Consider limiting this value to 30 or lower to reduce the risk of account takeover.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.zta.high\_assurance.session.timeout|
|Plugin applicability|Zero Trust - Continuous Authentication \(com.snc.zero\_trust\_continuous\_authentication\)|
|Security risk|Shorter session lengths reduce the risk of account takeover by forcing users to re-authenticate.|
|Common Vulnerability Scoring System \(CVSS\) score|3.3|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|Users in high assurance sessions must re-authenticate at the interval set by this property.|
|Dependencies and prerequisites|None|
|Data type|Integer|
|Base system value|30|
|Fallback value|30|
|Recommended value|30 or lower|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Session management](sc-session-management.md)

