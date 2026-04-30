---
title: Enforce current password policy compliance requirements on login
description: Reduce the risk of brute force account login by enforcing current password policy compliance requirements on login.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-10"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enforce current password policy compliance requirements on login

Reduce the risk of brute force account login by enforcing current password policy compliance requirements on login.

Help prevent interactive users from logging in to the instance with passwords that don’t meet current administrator requirements using the **glide.apply.password\_policy.on\_login** system property.

Set the **glide.apply.password\_policy.on\_login** system property to **true** to enforce current password policy compliance requirements. If this property doesn’t exist on the System Properties \[sys\_properties\] table, the default value is **false**.

## More information

<table id="table_zyc_nlf_32c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical configuration name

</td><td>

glide.apply.password\_policy.on\_login

</td></tr><tr><td>

Plugin applicability

</td><td>

None

</td></tr><tr><td>

Security risk

</td><td>

Interactive users may continue to log in to the instance with passwords that don’t meet current administrator requirements. This may mean that the users have weak passwords that don’t meet up-to-date security requirements, potentially leading to an increased risk of brute-force account logins by a malicious user.

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) score

</td><td>

4.4

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) rating

</td><td>

Medium

</td></tr><tr><td>

Functional impact

</td><td>

If the existing passwords aren’t in compliance with your current password policy, enabling this property forces users to change the passwords during their next login. This property is automatically set to **false**. Setting the value to **true** enforces a password policy during login.**Note:** Enabling this property might force a significant number of users who aren’t in compliance with the new password policy to change their passwords.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Base system value

</td><td>

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

