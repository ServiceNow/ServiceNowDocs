---
title: Create an API account for the Check Point NGTP integration
description: An API account role is required in your ServiceNow AI Platform instance for this integration. The Username and Password associated with this account are created in the ServiceNow AI Platform and entered in Check Point, so the Check Point authenticates with the ServiceNow AI Platform when retrieving Block List entries.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an API account for the Check Point NGTP integration

An API account role is required in your ServiceNow AI Platform instance for this integration. The Username and Password associated with this account are created in the ServiceNow AI Platform and entered in Check Point, so the Check Point authenticates with the ServiceNow AI Platform when retrieving Block List entries.

## Before you begin

Role required: admin

## About this task

The ServiceNow AI Platform admin creates an API account role \(sn\_sec\_checkpoint.api\_account\_access\). This account is used exclusively for entering credentials required for authentication on Check Point, so the Gateway can retrieve Block Lists from the ServiceNow AI Platform. This account is a separate, unique API user account in the ServiceNow AI Platform instance, and assigned to the Check Point administrator.

## Procedure

1.  Navigate to **All** &gt; **Organization** &gt; **Users**.

2.  Click the **Users** module.

    ![Users module](../image/users-module.png)

3.  On the Users list that is displayed, click **New**.

    ![New user record](../image/new-user.png)

    A new form is displayed.

    ![New user record](../image/user-new-record.png)

4.  Fill in the form, as needed.

    **Note:** The values for User ID title, and email address shown in the following table and figure are example values.

    |Field|Description|
    |-----|-----------|
    |User ID|Unique User ID for the role in your ServiceNow AI Platform instance. This user ID is entered in the **Username** field in the **Client Authentication** section of the Block List Configuration Check Point gateway. An example is CKPT API account SN.|
    |First Name|Person you are assigning|
    |Last Name|Person you are assigning|
    |Title|Job Title, for example FW admin.|
    |Password|Unique password created for this role. This password is entered in the **Password** field in the **Client Authentication** section of the Block List Configuration on Check Point gateway.|
    |Email|Unique email address|

5.  Click **Submit**.

    Once submitted, you can assign the role.

6.  On the Users list in the User ID column, click the name of the user ID you entered, CKPTAPI account SN, for example.

    ![Users - New form](../image/user-id.png)

7.  On the open record in the Roles section, click **Edit**.

    ![Edit roles](../image/edit-roles.png)

8.  On the **Edit Members** form that is displayed, enter sn\_sec\_checkpoint.api\_account\_access in the **Collection** field.

    ![Collection slushbucket](../image/edit-members-slushbucket.png)

9.  In the **Collection** column, select then move sn\_sec\_checkpoint.api\_account\_access to the **Roles List**.

10. Click **Save**.

11. Navigate to **Users**, and in the **User** column on the list, click the ID name that you created for the role \(CKPT API account SN\).

    ![Collection slushbucket](../image/edit-members-slushbucket2.png)

12. ![Edit roles](../image/edit-roles2.png)

    The user record is displayed. This record verifies that the user account has been assigned.


