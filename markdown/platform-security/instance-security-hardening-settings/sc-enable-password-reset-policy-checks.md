---
title: Enable password reset policy checks \[Updated in Security Center 2.0\]
description: Use the glide.enable.password\_policy property to enable password policy checks whenever a user changes their password using the user interface.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable password reset policy checks \[Updated in Security Center 2.0\]

Use the **glide.enable.password\_policy** property to enable password policy checks whenever a user changes their password using the user interface.

To define which password policy to use once this property is enabled, see [Enabling password policies on your instance](../../../integrate/authentication/task/enable-password-policies.md). Ensure the Glide Property **glide.enable.password\_policy** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.

**Note:** The **glide.enable.password\_policy** does not apply when an administrator changes a password or adds a user through script.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.enable.password\_policy**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|To apply password policy at time of password change.|
|Recommended value|true \(for higher strength passwords\)|
|Security risk rating|7.4|
|Functional impact|Setting the property to true turns on password policy checks when a user resets their password.|
|Security risk|\(Moderate\) Without a password policy, a user can create a weak password which increases the likelihood of an adversary gaining access to the instance.|

## Steps to configure

If you configure this setting in the Hardening Compliance Configuration page in the Instance Security Center:

1.  Under **Medium**, Select **Session Management**.
2.  In the **Enable Password Reset Policy Check** setting, select **Medium** for medium strength passwords, or **Strong** for more robust, higher strength passwords. Selecting one of these options sets the **glide.enable.password\_policy** property to true and starts a workflow that automatically updates your password policy.

Additionally, you can set the **glide.apply.password\_policy.on\_login** system property to enable password policy checks at the time of log in.

**Parent Topic:**[Authentication](sc-authentication.md)

