---
title: Set minimal password length \[Updated in Security center 2.2\]
description: Set minimal password length to avoid compliance issues and reduce the risk of a successful brute force attack
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Set minimal password length \[Updated in Security center 2.2\]

Set minimal password length to avoid compliance issues and reduce the risk of a successful brute force attack

Enforce a minimum password length of at least 12 characters to avoid compliance issues and reduce the risk of a successful brute force attack.

For every utilized Password credential store in use on your instance, ensure that a Password Policy is being enforced by selecting the **Enable password policy** field on the associated record in on Password Reset Credential Store \[pwd\_cred\_store\] table.

Next, open the record on the Password Policy \[password\_policy\] record table and set the **Minimum Password Length** field to at least **12**. You can find the associated Password Policy record in the **Password policy** field of the Password Reset Credential Store \[pwd\_cred\_store\] record.

For more information configuring a password policy, see [Enabling password policies on your instance](../../../integrate/authentication/task/enable-password-policies.md).

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|Records on the Password Reset Credential Store \[pwd\_cred\_store\] and Password Policy \[password\_policy\] tables.|
|Plugin applicability|None|
|Security risk|Setting the **Minimum Password Length** Policy \[password\_policy\] records to value of less than 12 could lead to compliance issues and increases the risk of an attacker successfully brute forcing passwords.|
|Common Vulnerability Scoring System \(CVSS\) score|5.9|
|Common Vulnerability Scoring System \(CVSS\) rating|Medium|
|Functional impact|The instance will not suffer any impact from a minimum password length of 12.|
|Dependencies and prerequisites|None|
|Data type|Integer|
|Base system value|8|
|Fallback value|8|
|Recommended value|12|

**Parent Topic:**[Authentication](sc-authentication.md)

