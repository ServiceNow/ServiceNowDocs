---
title: Configure Workplace Services
description: Configure the Workplace Services business unit to manage workplace service requests and space arrangements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/config-workplace.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Workplace Services

Configure the Workplace Services business unit to manage workplace service requests and space arrangements.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  From the Configuration Summary navigation menu, select **Workplace Services**.

    Alternatively, select **Continue** on the Workplace Services tile.

    Configure the followings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage Groups
    -   Role assignment
    -   Email address
    -   Workplace locations
    -   Notifications \(preconfigured by default\)
    **Note:** By default, the CBS admin role cannot configure Manage Groups or Role assignment. To complete these tasks, assign the User admin role \(user\_admin\) to the CBS admin \(sn\_cbs.admin\).

    for more information, see .

5.  Customize existing intake form or create new ones to collect workplace requests.

    The following intake form is preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |Workplace Services request|Report outages, maintenance issues, or submit general workplace services questions.|

    -   To customize an existing intake form, select the **Edit** icon.
    -   To create a intake form, select **Create new**. For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/catalog-builder.md).

        **Note:** Create intake forms directly in the production instance. Intake forms created in sub-production instances are not supported for promotion to production.

6.  Manage groups to organize users who handle workplace requests, manage content, and configure access.

    -   Workplace Services default groups

        The following groups are preconfigured with associated roles:

        |Workplace Services groups|Description|
        |-------------------------|-----------|
        |WSD Administrators|Manage Workplace Services roles, processes, and workflows.|
        |WSD Employee center managers|Manage Workplace Services support topics, quick links, and knowledge articles in the Employee Center.|
        |WSD Request managers|Receive, assign, and respond to Workplace Services requests.|

        To assign users to a default group:

        1.  Select **Edit** icon next to the group name.
        2.  In the Assign people to this group field, search for and select users.
        3.  Select **Save**.

            **Note:** Users added to a default group are automatically assigned the roles listed under Default assigned role.

    -   Create custom groups to organize your Workplace Services team.

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
8.  Configure the Workplace Services email address and select **Save**.

    Emails sent to this address automatically create requests and send the request number to the sender.

9.  Manage your work spaces by adding space details or by uploading a template file.

    -   Add spaces:

        1.  Select **Add spaces**.
        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Region|Geographic region of the space.|
            |Site|Site name, such as a city or campus.|
            |Campus|Campus associated with the site.|
            |Building|Building where the space is located.|
            |Floor|Floor number or identifier.|
            |Space name|Name of the space, such as a meeting room.|
            |Space type|Type of space, such as office or conference room.|
            |Time zone|Time zone for accurate scheduling.|

        3.  Select **Save**.
        **Note:** To add multiple spaces, select **+ New Space** and repeat the steps.

    -   Bulk upload:

        1.  Select **Upload spaces**.
        2.  Download the space template.
        3.  Enter space details in the template.
        4.  Save the file in .xlsx or .xls format.
        5.  Upload the updated file.
        6.  Select **Complete upload**.
        **Note:** Ensure all required fields are completed and the file size does not exceed 50 MB.

    -   Bulk edit:
        1.  From the more options menu \(three dots\), select **Bulk edit spaces**.
        2.  Download the file and update the space details.
        3.  Save the file in .xlsx or .xls format.
        4.  Upload the updated file.
        5.  Select **Complete upload**.
    **Note:** Ensure all changes are accurate before uploading.

10. Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned workplace requests.

    -   To create an email notifications, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateANotification.md).
    -   To create new Portal or Workspace notifications, see [Trigger conditions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/notif-trigger-form.md).
11. After you finish all configuration steps, select **Mark as configured**.


**Parent Topic:**[Configure Core Business Suite using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/config-cbs-using-guided-setup.md)

