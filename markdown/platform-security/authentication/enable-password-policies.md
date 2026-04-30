---
title: Enabling password policies on your instance
description: Implement password policy controls at login. Force users to change their password if the password does not meet the password policy criteria.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Password complexity requirements, Local Authentication, Authentication, Access Management]
---

# Enabling password policies on your instance

Implement password policy controls at login. Force users to change their password if the password does not meet the password policy criteria.

## Before you begin

Role required: admin

## About this task

The Password Policy plugin \(com.glide.password\_policy\) is enabled by default. The policy goes into effect when a user changes or resets the password.

The **Password Strength Preset** field is automatically set to **Default Strong**. If you want to add new criteria, you can perform the following procedure.

If you customized your instance through the **ValidatePasswordStronger** installation exit or your Password Reset credential store **pwd\_cred\_store** property, then see [password policy properties](../reference/password-policy-properties.md) to know how to implement a password policy for your instance.

**Note:** The active password policy is highlighted for the Instance as shown.

![Password Highlighted when set as active](../images/password-highlight.png)

To change the password policy navigate to **All** &gt; **Password Reset** &gt; **Credentials Stores**, select the credentials and change the **Password policy** field to the required policy input.

## Procedure

1.  Navigate to **All** &gt; **Password Policy** &gt; **Password Policies**.

2.  Click **New**.

    The Password Policy form appears.

3.  Specify the **Name** for your password policy.

4.  In the Password Policy Criteria section, select one of the following presets from the **Password Strength Preset** field.

<table id="choicetable_syn_nd3_yrb"><thead><tr><th align="left" id="d57261e144">

Password Strength Preset

</th><th align="left" id="d57261e147">

Description

</th></tr></thead><tbody><tr><td id="d57261e153">

**Default**

</td><td>

Auto-populates the fields for required password characters as follows:-   Sets **Minimum Uppercase Character\(s\)** to 1.
-   Sets **Minimum Lowercase Character\(s\)** to 1.
-   Sets **Minimum Numeric Character\(s\)** to 1.
-   Sets **Minimum Special Character\(s\)** to 0.
 The minimum password length is 8 characters, and the maximum is 100.

</td></tr><tr><td id="d57261e192">

**Medium**

</td><td>

Auto-populates the fields for required password characters as follows:-   Sets **Minimum Uppercase Character\(s\)** to 1.
-   Sets **Minimum Lowercase Character\(s\)** to 1.
-   Sets **Minimum Numeric Character\(s\)** to 1.
-   Sets **Minimum Special Character\(s\)** to 1.
 The minimum password length is 12 characters, and the maximum is 40.

</td></tr><tr><td id="d57261e231">

**High**

</td><td>

Auto-populates the fields for required password characters as follows:-   Sets **Minimum Uppercase Character\(s\)** to 1.
-   Sets **Minimum Lowercase Character\(s\)** to 2.
-   Sets **Minimum Numeric Character\(s\)** to 1.
-   Sets **Minimum Special Character\(s\)** to 3.
 The minimum password length is 8 characters, and the maximum is 100.

</td></tr><tr><td id="d57261e270">

**Default Strong**

</td><td>

Auto-populates the fields for required password characters as follows:-   Sets **Minimum Uppercase Character\(s\)** to 1.
-   Sets **Minimum Lowercase Character\(s\)** to 1.
-   Sets **Minimum Numeric Character\(s\)** to 1.
-   Sets **Minimum Special Character\(s\)** to 1.
 The minimum password length is 8 characters, and the maximum is 100.

</td></tr><tr><td id="d57261e310">

**Custom**

</td><td>

Auto-populates the fields for required password characters as follows:-   Sets **Minimum Uppercase Character\(s\)** to 1.
-   Sets **Minimum Lowercase Character\(s\)** to 1.
-   Sets **Minimum Numeric Character\(s\)** to 1.
-   Sets **Minimum Special Character\(s\)** to 1.
 The minimum password length is 8 characters, and the maximum is 100.

 You can also customize the **Password Policy Script** that is displayed.

</td></tr><tr><td id="d57261e355">

**Advanced**

</td><td>

Selecting **Advanced** displays **Password Rule Script** and **Password Strength Script**. Based on your requirement you can customize these scripts.

</td></tr></tbody>
</table>    **Note:** Password policy is applied based on the selected preset.

5.  On the form, fill in the remaining fields.

<table id="table_sks_f5c_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum Password Length

</td><td>

Minimum length of the password. This option is displayed for all the presets except for **Advanced**. Set this field to a minimum of 8–10 characters.

</td></tr><tr><td>

Maximum Password Length

</td><td>

Maximum length of the password. This option is displayed for all the presets except **Advanced**. Set this field to a maximum of 100 characters.

</td></tr><tr><td>

Minimum Uppercase Character\(s\)

</td><td>

Minimum number of uppercase characters in the password, from 0 to 10.

</td></tr><tr><td>

Minimum Lowercase Character\(s\)

</td><td>

Minimum lowercase characters in the password, from 0 to 10.

</td></tr><tr><td>

Minimum Numeric Character\(s\)

</td><td>

Minimum numeric of characters in the password, from 0 to 10.

</td></tr><tr><td>

Minimum Special Character\(s\)

</td><td>

Minimum number of special characters in the password, from 0 to 10.

</td></tr><tr><td>

Included Special Characters

</td><td>

Allow a restricted set of special characters without any delimiter. For example, if you enter `$,!`, then users can only use "$" and "!" as special characters in the password. No other special characters can be used. A password with other special characters is not allowed.

</td></tr><tr><td>

Excluded Special Characters

</td><td>

Allow a restricted set of special characters without any delimiter.For example, if you enter `@$!`, then users cannot use '@', '$' and '!' as special characters in their passwords.

**Note:** This option is available if the **glide.password\_policy.use\_excluded\_special\_char** property is enabled.

</td></tr><tr><td>

Disallow User Data

</td><td>

Option to disallow user data that is authentication-related.

</td></tr><tr><td>

Sequence Length Threshold

</td><td>

The sequence length of your password.

</td></tr><tr><td>

Repetition Length Threshold

</td><td>

The repetition length of your password.**Note:**

-   Both the sequence length threshold and repetition length threshold can have a maximum of eight characters. These fields enable you to restrict weak combinations of passwords that have predictable and repeating sequences such as "123456", "qwerty", "!@\#$%^", "aaaaa", and so on.
-   If **Password Strength Preset** is set to **Default Strong**, then the length for both sequence length threshold and repetition length threshold is set to four characters.


</td></tr><tr><td>

Test Your Password

</td><td>

Specify your actual password in this field.

</td></tr></tbody>
</table>6.  Click **Test Your Password**.

7.  After the password is tested as valid, click **Submit** to submit the password.

    **Note:** Always test your password before submitting.


