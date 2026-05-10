---
title: Configure Legal
description: Configure the Legal business unit to submit and manage legal requests.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Legal

Configure the Legal business unit to submit and manage legal requests.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite Foundation card, select **View product overview**.

3.  In the configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the configuration console.

4.  From the configuration summary navigation menu, select **Legal**.

    Alternatively, select **Continue** on the Legal tile.

    Configure the following settings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage groups
    -   Role assignment
    -   Notifications \(preconfigured by default\)
    **Note:** By default, only the admin can configure the manage groups or role assignment.

5.  Customize an existing intake form or create intake forms to collect legal requests.

    The following intake form is preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |Legal request|Submits general legal questions or requests legal services.|

    -   To customize an existing intake forms, select the **Edit** icon.
    -   To create an intake form, select **Create new**. For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-builder.md).

        **Note:** Create intake forms directly in the new instance. Moving intake forms configurations to a new instance using an update set isn’t supported.

    -   After customizing or creating an intake form, select **Mark as configured**.
6.  Manage groups to organize users who handle legal requests, manage content, and configure access.

    -   Default groups

        The following groups are preconfigured with associated roles:

        |Legal groups|Description|
        |------------|-----------|
        |Legal administrators|Manage Legal roles, processes, and workflows.|
        |Legal Employee Center managers|Manage Legal support topics, quick links, and knowledge articles in the Employee Center.|
        |Legal request managers|Receive, assign, and respond to Legal requests.|

        To assign user to a default group:

        1.  Select the **Assign people** icon next to the group name.
        2.  In the assign people to this group field, search for and select users.
        3.  Select **Save**.
        4.  On the mange groups page, select **Mark as configured**.
    -   Create custom groups to organize your Legal team.

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
8.  Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned legal requests.

    -   To create an email notification, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).
    -   To create Portal or Workspace notification, see [Trigger conditions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/notif-trigger-form.md).
    -   After configuring notifications, select **Mark as configured**.

**Parent Topic:**[Configure Core Business Suite using guided setup](../concept/config-cbs-using-guided-setup.md)

