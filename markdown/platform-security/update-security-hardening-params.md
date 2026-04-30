---
title: Adjust instance security settings to increase compliance
description: Using the Hardening Compliance Configuration page, harden and optimize non-compliant security properties that affect the daily compliance score of your instance. Its use ensures that your instance complies with the published security hardening standards, while fulfilling your company's security requirements.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Check the daily compliance score and configure security property settings, Instance Security Center, Platform Security]
---

# Adjust instance security settings to increase compliance

Using the Hardening Compliance Configuration page, harden and optimize non-compliant security properties that affect the daily compliance score of your instance. Its use ensures that your instance complies with the published security hardening standards, while fulfilling your company's security requirements.

## Before you begin

Role required: security\_dashboard\_user or admin.

Refer to the [Hardening settings](../../security-center/reference/security-hardening-settings.md) content for detailed descriptions, and compliance values, for the security-related system properties and plugins in the ServiceNow AI Platform.

-   Consult the Instance Security Hardening Settings whenever you set or update security-related properties, even if some of the compliance values may not be suitable for your instance.
-   When you are updating these properties, ensure that the instance continues to behave as expected. Consult with the appropriate internal personnel who have the expertise to determine the security impacts.

**Note:** If you have an admin role, you can view and edit security controls. If you have a security\_dashboard\_user role, you can view security controls, but you cannot edit them.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Instance Security Center**.

2.  Click the **Daily Compliance Score** tile or the **Hardening** link to access the Hardening Compliance Configuration page.

    ![Instance security center page](../image/isc-hardening-1.png)

3.  In the Hardening Compliance chart, view the statistics for compliant and non-compliant security configuration properties.

<table id="choicetable_lvw_mhf_kfb"><tbody><tr><td id="d81402e125">

**__Compliant__**

</td><td>

Number of security configuration properties that comply with the compliance values in the Instance Security Hardening Settings.**Note:** You cannot change the settings for compliant security properties in the Hardening Compliance Configuration. If you want to do so, you must update them in System Properties. To learn more, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

</td></tr><tr><td id="d81402e144">

**__Non-Compliant__**

</td><td>

Number of security configuration properties that do not comply with the compliance values in the Instance Security Hardening Settings. You can update settings for non-compliant properties.

</td></tr></tbody>
</table>    ![Instance security center page](../image/isc-hardening-2.png)

    **Note:** To view the number of compliant or non-compliant security scores over a range of dates, move the blue dot on the slider below the Daily Compliance Score.

4.  In the **Show** list below the chart, specify whether you want to access all security configuration properties, or only recommended ones.

<table id="choicetable_kwb_2q5_mlb"><tbody><tr><td id="d81402e183">

**__All__**

</td><td>

\(Default\) All compliant and non-compliant security configuration properties in each selected category.

</td></tr><tr><td id="d81402e195">

**__Recommended__**

</td><td>

Only recommended security configuration properties appear in each selected category. These security configuration properties are a selected subset of the most critical ones used to secure the ServiceNow AI Platform. Consider these security configuration properties to be the bare minimum number of settings you must set to secure the ServiceNow AI Platform.

**Note:** To fully secure your instance, use the **All** option. It includes all recommended security configuration properties too.

</td></tr></tbody>
</table>    ![Instance security center page](../image/isc-hardening-3.png)

5.  In **Categories**, select the category that contains the security configuration properties you would like to access:

    ![Instance security center page](../image/isc-hardening-4.png)

<table id="choicetable_lbl_dnx_lgb"><tbody><tr><td id="d81402e257">

**__Access Control__**

</td><td>

Access controls determine whether to grant or deny user access to a particular resource based on who is permitted to use those resources. To learn more, see [Access control](../../security-center/reference/sc-access-control.md) in the Instance Security Hardening Settings.

</td></tr><tr><td id="d81402e279">

**__Attachments__**

</td><td>

Attachment security controls enable validation of incoming attachments to protect your instance against malicious files sent by attackers. To learn more, see [Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]](../../security-center/reference/sc-validate-file-mime-type-in-attachmentcreator.md) in the Instance Security Hardening Settings.

</td></tr><tr><td id="d81402e303">

**__Email Security__**

</td><td>

Email security encompasses security configuration properties an administrator can configure to ensure that proper security policies are in place for all inbound emails. To learn more, see [Enable email spam scoring and filtering \[Updated in Security Center 1.3\]](../../security-center/reference/sc-email-spam-scoring-and-filtering.md) in the Instance Security Hardening Settings.

</td></tr><tr><td id="d81402e331">

**__Input Validation__**

</td><td>

Input validation includes security-related properties that an administrator can configure to minimize entry of malformed data, regardless of source. To learn more, see [Validation, sanitization, and encoding](../../security-center/reference/validation-sanitization-encoding.md) in the Instance Security Hardening Settings.

</td></tr><tr><td id="d81402e353">

**__Secure communications__**

</td><td>

Secure communications properties are those that an administrator can configure to secure the transportation of HTTP traffic. To learn more, see [Communications](../../security-center/reference/sc-communications.md) in the Instance Security Hardening Settings.

</td></tr><tr><td id="d81402e376">

**__Security Best Practices__**

</td><td>

Security best practices encompass Security Tasks that an administrator should perform periodically, within a certain interval of time, and include related configuration properties. To learn more, see [Hardening settings](../../security-center/reference/security-hardening-settings.md).

</td></tr><tr><td id="d81402e404">

**__Security Inclusion Listing__**

</td><td>

Security inclusion listing includes security-related properties that an administrator can configure to restrict behavior to known inclusion listings. To learn more, see [Validation, sanitization, and encoding](../../security-center/reference/validation-sanitization-encoding.md) in the Instance Security Hardening Settings

</td></tr><tr><td id="d81402e426">

**__Session Management__**

</td><td>

Session management includes security-related properties that an administrator can configure to ensure secure session management in the ServiceNow AI Platform. To learn more, see [Session management](../../security-center/reference/sc-session-management.md) in the Instance Security Hardening Settings

</td></tr></tbody>
</table>6.  Configure the non-compliant security properties in the selected category.

    -   Unless otherwise specified, sliding the switch on sets a security property to its recommended setting. For example, you set most controls to true or false, but some require entry of a value, or values, such as a comma-separated value list.
    -   To access the dedicated Instance Security Hardening Settings topic for the security control, and learn more about it, click **More Info**.

## Result

The Daily Compliance score increases or decreases depending on the changes that you make to the non-compliant security control settings.

**Parent Topic:**[Check the daily compliance score and configure security property settings](../concept/instance-sec-center-hardening.md)

**Related topics**  


[Instance Security Center](../concept/instance-security-center.md)

