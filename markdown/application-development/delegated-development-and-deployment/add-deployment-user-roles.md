---
title: Add deployment user roles
description: A system administrator can assign user roles to specific personnel that allow them to perform first application installations only, or install and upgrade applications in a local instance.
locale: en-US
release: australia
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User roles, Configure, Delegated Development, Planning your application, Building applications]
---

# Add deployment user roles

A system administrator can assign user roles to specific personnel that allow them to perform first application installations only, or install and upgrade applications in a local instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open a user record.

    **Note:** For details on how to assign a role to a user, refer to [Assign a user role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired deployment roles, and then select **Add**.

<table id="table_rng_dtq_jdb"><thead><tr><th>

User Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_appclient.app\_client\_company\_installer

</td><td>

Allows a designated person to perform first-time installations of applications displayed on the Application Client page that contain the same company as the current instance. A user with this role cannot install an application for another company. For example, applications for ABC Company and XYZ Company display on the Application Client page. A user with this role can only install XYZ Company applications when logged in to a XYZ Company instance. The user cannot install applications for ABC Company.

 **Note:** While this role does not grant a user the ability to upgrade applications, the system auto-adds a delegated developer upgrade role after the user does a first-time installation. The user can then perform upgrades for the application in the local instance. For more details, see System-managed developer and deployment roles.

</td></tr><tr><td>

sn\_appclient.app\_client\_user

</td><td>

Allows a designated person to install and upgrade all applications displayed on the Application Client page.

</td></tr></tbody>
</table>4.  Select **Save**.


