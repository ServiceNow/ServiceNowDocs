---
title: Create the API account role for Palo Alto Networks Next-Generation Firewall
description: An API account role is required in your ServiceNow AI Platform instance for this integration. The Username and Password associated with this account are created in the ServiceNow AI Platform and entered in Palo Alto Networks so the Palo Alto Networks Next-Generation Firewall authenticates with the ServiceNow AI Platform when retrieving EDL entries.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create the API account role for Palo Alto Networks Next-Generation Firewall

An API account role is required in your ServiceNow AI Platform® instance for this integration. The Username and Password associated with this account are created in the ServiceNow AI Platform® and entered in Palo Alto Networks so the Palo Alto Networks Next-Generation Firewall authenticates with the ServiceNow AI Platform® when retrieving EDL entries.

## Before you begin

Role required: admin

## About this task

The ServiceNow AI Platform® admin creates an API account role \(sn\_sec\_panfw.api\_account\_access\). This account is used exclusively for entering credentials required for authentication on Palo Alto Networks so the firewalls can retrieve EDLs from the ServiceNow AI Platform®. This account is a separate, unique API user account in the ServiceNow AI Platform® instance, and assigned to the Palo Alto Networks Next-Generation Firewall administrator.

## Procedure

1.  Navigate to **All** &gt; **Organization** &gt; **Users**.

2.  Click the **Users** module.

    ![Select the Users module.](../image/4-30-user-nav.png)

3.  On the Users list that is displayed, click **New**.

    ![New User record.](../image/4-30-user-nav-new.png)

    A new user form is displayed.

4.  Fill in the form.

    **Note:** The values for User ID title, and email address shown in the following table and figure are example values.

    |Field|Description|
    |-----|-----------|
    |User ID|Unique User ID for the role in your ServiceNow AI Platform® instance. This user ID is entered in the **Username** field in the **Client Authentication** section of the External Dynamic Lists dialog on the Palo Alto Networks site. An example is `API account SN`.|
    |First name|Person you are assigning.|
    |Last name|Person you are assigning.|
    |Title|Job title, for example, `FW admin`.|
    |Password|Unique password created for this role. This password is entered in the **Password** field in the **Client Authentication** section of the External Dynamic Lists dialog on the Palo Alto Networks site.|
    |Email|Unique email address.|

    ![User record completed.](../image/4-30-user-listed.png)

5.  Click **Submit**.

    Once submitted, you can assign the role.

6.  On the Users list in the **User ID** column, click the name of the user ID you entered, `API account SN`, for example.

    ![New User ID listed.](../image/4-30-user-listed-callout.png)

7.  On the open record in the Roles section, click **Edit**.

    ![Click Edit to open the record.](../image/4-30-user-form-callout.png)

8.  On the **Edit Members**form that is displayed, enter `sn_sec_panfw.api_account_access` in the **Collection** field.

    Below the **Collection** field, the role is displayed in the column.

    ![Enter new role in Collection column.](../image/4-30-user-add-enter.png)

9.  In the **Collection** column, select then move `sn_sec_panfw.api_account_access` to the **Roles List**.

    ![Move new role to Roles List.](../image/4-30-add-role.png)

10. Click **Save**.

11. Navigate to **Users**, and in the **User** column on the list, click the ID name that you created for the role \(`API account SN`\).

    ![New role displayed on Users list.](../image/4-30-user-role-section.png)

    The user record is displayed. This record verifies that the user account has been assigned. The **State** is active, and the role is not inherited.


**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Set up and install Palo Alto Networks Next-Generation Firewall](paloalto_install.md)

**Next topic:**[Supported External Dynamic Lists for Palo Alto Networks Next-Generation Firewall](../reference/paloalto_supported_edls.md)

