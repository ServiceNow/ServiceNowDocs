---
title: Configure Source-to-Pay
description: Configure the Source‑to‑Pay business unit to manage procurement, supplier, and invoice requests from submission to fulfillment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Core Business Suite using guided setup, Configure, Core Business Suite]
---

# Configure Source-to-Pay

Configure the Source‑to‑Pay business unit to manage procurement, supplier, and invoice requests from submission to fulfillment.

## Before you begin

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite Foundation card, select **View product overview**.

3.  In the configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the configuration console.

4.  From the configuration summary navigation menu, select **Source-to-Pay**.

    Alternatively, select **Continue** on the Source‑to‑Pay tile.

    Configure the following settings as needed:

    -   Intake forms \(preconfigured by default\)
    -   Manage groups
    -   Role assignment
    -   Supplier management
    -   Supplier contacts
    -   Email address
    -   Notifications \(preconfigured by default\)
    **Note:** By default, only the admin can configure the manage groups or role assignment.

5.  Customize existing intake forms or create intake forms to collect Source‑to‑Pay requests.

    The following intake forms are preconfigured by default:

    |Intake form|Description|
    |-----------|-----------|
    |General supplier request|Submit general questions related to suppliers.|
    |Procurement request|Submit procurement‑related questions or requests.|
    |Invoice request|Submit invoice‑related questions to Accounts Payable.|

    -   To customize an existing intake forms, select the **Edit** icon.
    -   To create an intake form, select **Create new**. For more information, see [Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

        **Note:** Create intake forms directly in the new instance. Moving intake forms configurations to a new instance using an update set isn’t supported.

    -   After customizing or creating an intake form, select **Mark as configured**.
6.  Manage groups to organize users who handle Source‑to‑Pay requests and configure access.

    -   Default groups

        The following groups are preconfigured with associated roles:

        |Source-to-Pay groups|Description|
        |--------------------|-----------|
        |Accounts payable admins|Manage Accounts Payable roles, processes, and workflows.|
        |Procurement admins|Manage Procurement roles, processes, and workflows.|
        |Supplier operations admins|Manage supplier operations roles and supplier management activities.|
        |S2P Employee Center managers|Manage Source‑to‑Pay content in the Employee Center.|
        |Invoice Request managers|Receive, assign, and respond to invoice requests.|
        |Procurement request managers|Receive, assign, and respond to procurement requests.|
        |Supplier request managers|Receive, assign, and respond to supplier requests.|

        To assign user to a default group:

        1.  Select **Assign people** icon next to the group name.
        2.  In the assign people to this group field, search for and select users.
        3.  Select **Save**.
        4.  On the mange groups page, select **Mark as configured**.
    -   Create custom groups to organize your Source‑to‑Pay team.

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
8.  Configure the Source‑to‑Pay email address.

    1.  Enter the email address.
    2.  Select **Save**.
    3.  Select **Mark as configured**.
    **Note:** Emails sent to this address automatically create requests and send the request number to the sender.

9.  Supplier management.

    Manage suppliers by adding supplier details or by uploading a template.

    -   Add suppliers:

        1.  Select **Add suppliers**.
        2.  On the form, fill in the fields.

<table id="table_n13_tw1_s3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal name

</td><td>

Legal name of the supplier.

</td></tr><tr><td>

Country of registration

</td><td>

Country where the supplier is registered.

</td></tr><tr><td>

Website

</td><td>

Supplier’s official website.

</td></tr><tr><td>

DUNS number

</td><td>

DUNS identifier for the supplier.

</td></tr><tr><td>

Description

</td><td>

Short description of the supplier.

</td></tr><tr><td>

ERP company code

</td><td>

Unique ERP company code.If no code exists, assign a unique code for each record \(for example, 100, 101, 102\)

</td></tr><tr><td>

ERP source

</td><td>

ERP source for the supplier.If no source is available, select CBS.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the supplier is active.

</td></tr></tbody>
</table>        3.  Select **Save**.
        4.  On the manage your supplier details page, select **Mark as configured**.
        **Note:** To add multiple suppliers, select **+ New supplier** and repeat the steps.

    -   Bulk upload:
        1.  Select **Upload suppliers**.
        2.  Download the supplier template.
        3.  Enter the supplier details in the template.
        4.  Save the file in .xlsx or .xls format.
        5.  Upload the updated file.
        6.  Select **Complete upload**.
        7.  On the manage your supplier details page, select **Mark as configured**.
    **Note:** Verify that all required fields are completed and the file size doesn’t exceed 50 MB.

10. Add or upload contacts associated with each supplier.

    Add contacts:

    1.  Select **Add contacts**.
    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |First name|First name of the contact.|
        |Last name|Last name of the contact.|
        |Email|Email address of the contact.|
        |Is this primary contact|Designates the primary contact. Default is Yes.|
        |Organization \(Supplier\)|Supplier associated with the contact.|

    3.  Select **Save**.
    4.  On the manage your supplier contacts page, select **Mark as configured**.
    **Note:** You can add up to 10 contacts at a time by selecting **+ New contact**.

    Bulk upload:

    1.  Select **Upload contacts**.
    2.  Download the template.
    3.  Update the contact details.
    4.  Upload the updated template.
    5.  Select **Save**.
    6.  On the manage your supplier contacts page, select **Mark as configured**.
    **Note:** Verify that all fields are complete and accurate before uploading.

11. Configure notifications sent through Email, Portal, and Workspace to users about submitted or assigned Source‑to‑Pay requests.

    -   To create an email notification, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   To create Portal or Workspace notifications, see [Trigger conditions form](https://www.servicenow.com/docs/access?context=notif-trigger-form&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).
    -   After configuring notifications, select **Mark as configured**.

**Parent Topic:**[Configure Core Business Suite using guided setup](../concept/config-cbs-using-guided-setup.md)

