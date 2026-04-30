---
title: Password policy properties
description: The password policy properties enable you to administrate password policies, exclude list passwords, and apply a password policy during login.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enabling password policies on your instance, Password complexity requirements, Local Authentication, Authentication, Access Management]
---

# Password policy properties

The password policy properties enable you to administrate password policies, exclude list passwords, and apply a password policy during login.

Navigate to **Password Policy** &gt; **Properties** to view and edit the password policy properties.

<table id="table_l1b_gch_yjb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.enable.password\_policy

</td><td>

Enables a password policy for your instance. The policy goes into effect when a user changes or resets a password. This property is automatically set to **true**. **Note:**

-   If your instance is customized, via the **ValidatePasswordStronger** installation exit or your Password Reset credential store \[pwd\_cred\_store\], then you must create this property and add it to your system properties.
-   Prior to the Orlando release, if your instance was customized with the **ValidatePasswordStronger** installation exit, then you had to create the Password Policy property to make the Password Policy work.
-   Starting with the Orlando release, there is no installation exit customization. The Password Policy properties work by default. These properties can be manually turned off.

</td></tr><tr><td>

glide.enable.blacklist\_password

</td><td>

Prohibits using specific passwords. The administrator can insert passwords into the Excluded Password table. This property is automatically set to **true**.

</td></tr><tr><td>

glide.apply.password\_policy.on\_login

</td><td>

Forces users to change the passwords during their next login if the existing passwords are not in compliance with the current password policy. This property is automatically set to **false**. Setting the value to **true** enforces a password policy during login.

**Note:** Enabling this property might force a significant number of users who are not in compliance with the new password policy to change their passwords.

</td></tr><tr><td>

glide.password\_policy.user\_excluded\_special\_char

</td><td>

Enables users to use the excluded special character option on the Password policy form.

</td></tr><tr><td>

glide.validate.sys\_user.password.field

</td><td>

Enables validation on the user password against the password policy when an admin is editing the sys\_user form or list view.

</td></tr><tr><td>

glide.password.policy.generate.password.field.disabled

</td><td>

Disables the **Password** field on the set password pop-up on the sys\_user form.

</td></tr><tr><td>

glide.user.show.password.field

</td><td>

Enables the **Password** field on the sys\_user form.

</td></tr><tr><td>

glide.password\_policy.debug

</td><td>

Enables debug logging for the password policy.

</td></tr></tbody>
</table>