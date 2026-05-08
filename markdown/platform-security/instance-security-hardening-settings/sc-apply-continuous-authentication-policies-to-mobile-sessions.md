---
title: Apply continuous authentication policies to mobile sessions
description: Reduce the risk of session hijacking by applying continuous authentication policies to mobile sessions.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Apply continuous authentication policies to mobile sessions

Reduce the risk of session hijacking by applying continuous authentication policies to mobile sessions.

Ensure that mobile users are using the high assurance session feature of the Zero Trust - Continuous Authentication plugin by setting the **glide.zta.high\_assurance.mobile.session.allowed** system property to **false**. To bypass continuous authentication policies for mobile sessions, set this property to **true**.

Set the **glide.zta.high\_assurance.mobile.session.allowed** system property to **false**. This action decreases the risk of session hijacking and persistent access if a session is compromised. If this property doesn’t appear in the System Properties \[sys\_properties\] table, the default value is **false**.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.zta.high\_assurance.mobile.session.allowed|
|Plugin applicability|Zero Trust - Continuous Authentication \(com.snc.zero\_trust\_continuous\_authentication\)|
|Security risk|If this system property set to **true**, the high assurance session feature isn’t applied to mobile sessions. Reauthentication doesn't happen as defined in policies for high role sessions. This increases the risk of session hijacking and persistent access if a session is compromised.|
|Common Vulnerability Scoring System \(CVSS\) score|3.9|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|If set to **true**, the high assurance session feature doesn’t apply to mobile sessions, which increases the risk of session hijacking and persistent access if a session is compromised.|
|Dependencies and prerequisites|None|
|Data type|Boolean|
|Base system value|false|
|Fallback value|false|
|Recommended value|false|

To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Session management](sc-session-management.md)

