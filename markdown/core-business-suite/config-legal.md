---
title: Configure Legal
description: Configure the Legal business unit to submit and manage legal requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/config-legal.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Legal

Configure the Legal business unit to submit and manage legal requests.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  From the Configuration Summary navigation menu, select **Legal**.

    Alternatively, select **Continue** on the Legal tile.

    Configure the following settings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage Groups
    -   Role assignment
    -   Notifications \(preconfigured by default\)
    **Note:** By default, the CBS admin role cannot configure Manage Groups or Role assignment. To complete these tasks, assign the User admin role \(user\_admin\) to the CBS admin \(sn\_cbs.admin\).

    for more information, see .

5.  Customize existing intake form or create new ones to collect legal requests.

    The following intake form is preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |Legal request|Submits general legal questions or requests legal services.|

    -   To customize an existing intake form, select the **Edit** icon.
    -   To create a intake form, select **Create new**.

        For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/catalog-builder.md).

        **Note:** Create intake forms directly in the production instance. Intake forms created in sub-production instances are not supported for promotion to production.

6.  Manage groups to organize users who handle legal requests, manage content, and configure access.

    -   Legal default groups

        The following groups are preconfigured with associated roles:

        |Legal groups|Description|
        |------------|-----------|
        |Legal Administrators|Manage Legal roles, processes, and workflows.|
        |Legal Employee center managers|Manage Legal support topics, quick links, and knowledge articles in the Employee Center.|
        |Legal Request managers|Receive, assign, and respond to Legal requests.|

        To assign user to a default group:

        1.  Select the **Edit** icon next to the group name.
        2.  In the Assign people to this group field, search for and select users.
        3.  Select **Save**.

            **Note:** Users added to a default group are automatically assigned the roles listed under Default assigned role.

    -   Create custom groups to organize your Legal team.

        1.  Select **Create Group**.
        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Group name|Name used to identify the group within the business unit.|
            |Group manager|User responsible for managing the group.|
            |Group description|Brief description of the group’s purpose.|
            |Assign people to this group|Users to add as group members.|
            |Assign role|Roles assigned to group members.|

        3.  Select **Save**.
7.  Assign roles to give groups the required access.

    1.  Select a role.
    2.  Select **Assign groups**.
    3.  Select the group from the list.
    4.  Select **Update**.
8.  Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned legal requests.

    -   To create an email notifications, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateANotification.md).
    -   To create Portal or Workspace notifications, see [Trigger conditions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/notif-trigger-form.md).
9.  After you finish all configuration steps, select **Mark as configured**.


**Parent Topic:**[Configure Core Business Suite using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/config-cbs-using-guided-setup.md)

