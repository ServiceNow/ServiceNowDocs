---
title: Reduce allowed bypasses for multifactor setup
description: Decrease the window of time an account is at risk of compromise by reducing allowed bypasses for multifactor setup.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Reduce allowed bypasses for multifactor setup

Decrease the window of time an account is at risk of compromise by reducing allowed bypasses for multifactor setup.

Reduce the number of times a user can skip the multifactor passcode setup requirement to decrease the window of time an account is at risk of compromise. Multifactor authentication \(MFA\) protects against password-related attacks or weak passwords by requiring an additional form of verification. Reducing the length of time a user can skip this setup reduces this vulnerability.

Set the **glide.authenticate.multifactor.setup.bypass.count** system property to **0** to prevent users from skipping multifactor passcode setup.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.authenticate.multifactor.setup.bypass.count|
|Plugin applicability|None.|
|Security risk|Multifactor authentication protects against password-related attacks or weak passwords by requiring an additional form of verification. A high number of allowed multifactor setup bypasses increases the risk of account compromise as the account isn’t protected by multifactor. A small number of allowed bypasses reduces this window of time.|
|Common Vulnerability Scoring System \(CVSS\) score|3.9|
|Common Vulnerability Scoring System \(CVSS\) rating|Low|
|Functional impact|Users aren’t allowed to login to an instance without setting up MFA if they’ve surpassed the number of logins specified in the property.|
|Dependencies and prerequisites|None|
|Data type|Integer|
|Base system value|0|
|Fallback value|0|
|Recommended value|0|

To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Authentication](sc-authentication.md)

