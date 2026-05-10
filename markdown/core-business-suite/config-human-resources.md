---
title: Configure Human Resources
description: Configure the Human Resources \(HR\) business unit to manage payroll inquiries, benefits questions, and general HR requests.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Human Resources

Configure the Human Resources \(HR\) business unit to manage payroll inquiries, benefits questions, and general HR requests.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite Foundation card, select **View product overview**.

3.  In the configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the configuration console.

4.  From the configuration summary navigation menu, select **Human Resources**.

    Alternatively, select **Continue** on the Human Resources tile.

    Configure the followings settings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage groups
    -   Role assignment
    -   Email address
    -   Notifications \(preconfigured by default\)
    **Note:** By default, only the admin can configure the manage groups or role assignment.

5.  Customize existing intake forms or create intake forms to collect HR requests.

    The following intake forms are preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |General HR request|Submit general Human Resources questions.|
    |Payroll request|Get help with payroll-related issues.|
    |Benefits request|Ask questions about employee benefits.|

    -   To customize an existing intake forms, select the **Edit** icon.
    -   To create an intake form, select **Create new**. For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-builder.md).

        **Note:** Create intake forms directly in the new instance. Moving intake forms configurations to a new instance using an update set isn’t supported.

    -   After customizing or creating an intake form, select **Mark as configured**.
6.  Manage groups to organize users who handle HR requests, manage knowledge, and configure access.

    -   Default groups

        The following groups are preconfigured with associated roles:

        |Human Resources group|Description|
        |---------------------|-----------|
        |HR request handlers|Receive, assign, and respond to HR requests.|
        |HR administrators|Manage HR roles, oversee processes, and access HR tools.|
        |HR Employee Center managers|Manage support topics, quick links, and knowledge articles.|

        To assign users to a default group:

        1.  Select the **Assign people** icon next to the group name.
        2.  In the assign people to this group field, search for and select users.
        3.  Select **Save**.
        4.  On the mange groups page, select **Mark as configured**.
    -   Create custom groups to organize HR team.

        1.  Select **Create Group**.
        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Group name|Name used to identify the group within the business unit.|
            |Group manager|Person responsible for managing the group.|
            |Group description|Brief description of the group’s purpose.|
            |Assign people to this group|People that you add as group members.|
            |Assign role|Roles assigned to group members.|

        3.  Select **Save**.
        4.  On the mange groups page, select **Mark as configured**.
7.  Assign roles to give groups the required access.

    1.  Select a role.
    2.  Select **Assign groups**.
    3.  Select the group from the list.
    4.  Select **Update**.
    5.  On the role assignment page, select **Mark as configured**.
8.  Configure Human Resources email address by adding the email address and select **Save**.

    Emails sent to this address automatically create requests and send the request number to the sender.

9.  Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned requests.

    -   To create an email notification, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).
    -   To create Portal or Workspace notification, see [Trigger conditions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/notif-trigger-form.md).
    -   After configuring notifications, select **Mark as configured**.

**Parent Topic:**[Configure Core Business Suite using guided setup](../concept/config-cbs-using-guided-setup.md)

