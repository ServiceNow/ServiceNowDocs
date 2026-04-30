---
title: Configuring your password policy
description: Password policy criteria enables you to secure your password and adhere to the minimum password complexity requirements.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Password complexity requirements, Local Authentication, Authentication, Access Management]
---

# Configuring your password policy

Password policy criteria enables you to secure your password and adhere to the minimum password complexity requirements.

## Before you begin

Role required: admin

## About this task

The Password Policy \[com.glide.password\_policy\] plugin is enabled by default. It goes into effect when a user changes or resets the password. If you customized your instance, through the ValidatePasswordStronger installation exit or your Password Reset credential store \[pwd\_cred\_store\], see [password policy properties](../reference/password-policy-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Password Policy** &gt; **Password Policies**.

    **Note:** **Default Strong** preset in enabled as a default password acceptance criteria. In case, if you want to add a new criteria, you can perform the following steps.

2.  Click **New**.

    The Password Policy New record page, has the following sections that you must specify for setting your password:

    -   **Password Policy Criteria**
    -   **Sequence Matching**
    -   **Test Your Password**
    ![Password policy new record creation](../images/password-policy-new-record.png)

3.  Specify the **Name** for your password policy.

4.  In the **Password Policy Criteria** section, select the preset from the **Password Strength Preset**. The presets available are as follows:

<table id="table_cdt_mtr_1rb"><thead><tr><th>

Password Strength Preset

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default

</td><td>

Selecting **Default** auto-populates the password characters required as follows:-   One Minimum Uppercase Character
-   One Minimum Lowercase Character
-   One Minimum Numeric Character


</td></tr><tr><td>

Medium

</td><td>

Selecting **Medium** auto-populates the password characters required based on characters as follows:-   One Minimum Uppercase Character
-   One Minimum Lowercase Character
-   One Minimum Numeric Character
-   One Minimum Special Character


</td></tr><tr><td>

High

</td><td>

Selecting **High** auto-populates the password characters as follows:-   One Minimum Uppercase Character
-   Two Minimum Lowercase Character
-   One Minimum Numeric Character
-   Three Minimum Special Character


</td></tr><tr><td>

Default Strong

</td><td>

Selecting **Default Strong** auto-populates the password characters required based on characters as follows:-   One Minimum Uppercase Character
-   One Minimum Lowercase Character
-   One Minimum Numeric Character
-   One Minimum Special Character


</td></tr><tr><td>

Custom

</td><td>

Selecting **Custom** auto-populates the password characters required based on characters as follows:-   One Minimum Uppercase Character
-   One Minimum Lowercase Character
-   One Minimum Numeric Character
-   One Minimum Special Character
 You can also customize the **Password Policy Script** that is displayed.

</td></tr><tr><td>

Advanced

</td><td>

Selecting **Advanced** displays **Password Rule Script** and **Password Strength Script**. Based on your requirement you can customize these scripts.

</td></tr></tbody>
</table>    **Note:** Password policy is applied based on the selected preset.

5.  Specify the fields described in the table:

<table id="table_sks_f5c_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum Password Length

</td><td>

Minimum length of the password. This option is displayed for all the presets except **Advanced**.**Note:** **Minimum Password Length** is a required field and recommended setting it to a minimum of 8–10 characters.

</td></tr><tr><td>

Maximum Password Length

</td><td>

Maximum length of the password. This option is displayed for all the presets except **Advanced**.**Note:** **Maximum Password Length** is an optional field and recommended to set it to a maximum 100 characters.

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

Allow a restricted set of special characters without any delimiter. For example, if you enter "$,!" users can only use "$" and "!" as special characters in the password. No other special characters can be used, and a password with other special characters is not allowed.

</td></tr><tr><td>

Excluded Special Characters

</td><td>

Allow a restricted set of special characters without any delimiter. For example, when '@$!' is entered, users should not be able to use '@', '$' and '!' as special characters in their passwords.**Note:** This option is available if the glide.password\_policy.use\_excluded\_special\_char property is enabled.

</td></tr><tr><td>

Disallow User Data

</td><td>

It is enabled to disallow the user data.

</td></tr></tbody>
</table>6.  In the Sequence Matching section, specify the **Sequence Length Threshold** and **Repetition Length Threshold**.

    **Note:**

    -   Both the sequence length threshold and repetition length threshold can have a maximum of eight characters. These fields enable you to restrict weak combinations of passwords that have predictable and repeating sequences such as "123456", "qwerty", "!@\#$%^", "aaaaa", and so on.
    -   For **Default Strong**, the length for both sequence length threshold and repetition length threshold is selected as four characters.
7.  In the **Test Your Password** section, specify your password.

8.  Click **Test Your Password**.

9.  Once the password is valid, click **Submit** to submit the password.

    **Note:** Always test your password before submitting.


