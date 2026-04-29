---
title: Configure Workplace Services
description: Configure the Workplace Services business unit to manage workplace service requests and space arrangements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Workplace Services

Configure the Workplace Services business unit to manage workplace service requests and space arrangements.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite Foundation card, select **View product overview**.

3.  In the configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the configuration console.

4.  From the configuration summary navigation menu, select **Workplace Services**.

    Alternatively, select **Continue** on the Workplace Services tile.

    Configure the followings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage groups
    -   Role assignment
    -   Email address
    -   Workplace locations
    -   Notifications \(preconfigured by default\)
    **Note:** By default, only the admin can configure the manage groups or role assignment.

5.  Customize an existing intake form or create intake forms to collect workplace requests.

    The following intake form is preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |Workplace Services request|Report outages, maintenance issues, or submit general workplace services questions.|

    -   To customize an existing intake forms, select the **Edit** icon.
    -   To create an intake form, select **Create new**. For more information, see [Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

        **Note:** Create intake forms directly in the new instance. Moving intake forms configurations to a new instance using an update set isn’t supported.

    -   After customizing or creating an intake form, select **Mark as configured**.
6.  Manage groups to organize users who handle workplace requests, manage content, and configure access.

    -   Default groups

        The following groups are preconfigured with associated roles:

        |Workplace Services groups|Description|
        |-------------------------|-----------|
        |WSD administrators|Manage Workplace Services roles, processes, and workflows.|
        |WSD Employee Center managers|Manage Workplace Services support topics, quick links, and knowledge articles in the Employee Center.|
        |WSD request managers|Receive, assign, and respond to Workplace Services requests.|

        To assign users to a default group:

        1.  Select **Assign people** icon next to the group name.
        2.  In the assign people to this group field, search for and select users.
        3.  Select **Save**.
        4.  On the mange groups page, select **Mark as configured**.
    -   Create custom groups to organize your Workplace Services team.

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
8.  Configure the Workplace Services email address.

    1.  Enter the email address.
    2.  Select **Save**.
    3.  Select **Mark as configured**.
    **Note:** Emails sent to this address automatically create requests and send the request number to the sender.

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
        4.  On the manage your work spaces page, select **Mark as configured**.
        **Note:** To add multiple spaces, select **+ New Space** and repeat the steps.

    -   Bulk upload:

        1.  Select **Upload spaces**.
        2.  Download the space template.
        3.  Enter space details in the template.
        4.  Save the file in .xlsx or .xls format.
        5.  Upload the updated file.
        6.  Select **Complete upload**.
        7.  On the manage your work spaces page, select **Mark as configured**.
        **Note:** Verify that all required fields are completed and the file size doesn’t exceed 50 MB.

    -   Bulk edit:
        1.  From the more options menu \(three dots\), select **Bulk edit spaces**.
        2.  Download the file and update the space details.
        3.  Save the file in .xlsx or .xls format.
        4.  Upload the updated file.
        5.  Select **Complete upload**.
        6.  On the manage your work spaces page, select **Mark as configured**.
    **Note:** Verify that all changes are accurate before uploading.

10. Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned workplace requests.

    -   To create an email notification, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   To create Portal or Workspace notification, see [Trigger conditions form](https://www.servicenow.com/docs/access?context=notif-trigger-form&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
    -   After configuring notifications, select **Mark as configured**.

**Parent Topic:**[Configure Core Business Suite using guided setup](../concept/config-cbs-using-guided-setup.md)

