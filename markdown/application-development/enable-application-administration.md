---
title: Restrict access to an application
description: Restrict management of an application and access to that application to prevent unauthorized users from assigning administrative rights to the application or accessing sensitive information in the application records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Application administration, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Restrict access to an application

Restrict management of an application and access to that application to prevent unauthorized users from assigning administrative rights to the application or accessing sensitive information in the application records.

## Before you begin

-   Records required:
    -   Role record to designate a role as the application-specific admin role
    -   User record to assign an application-specific admin role to a user
    -   Application record to enable application administration for a specific application
-   Role required: admin

If an application-specific admin role does not already exist, create it before beginning this procedure. For example, you can create a role named my\_application.admin that includes the name of the restricted application with the suffix "admin" to indicate that it is the admin role for the application.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Roles** or **User Administration** &gt; **Roles**.

2.  Open the role record for the application-specific admin role.

3.  Configure the form to add the **Application Administrator** field.

    **Note:** The **Application Administrator** check box replaces the **Assignable by** field. By default, when you upgrade from a Jakarta or earlier release to a Kingston or later release, any role that was in the **Assignable by** field is defined as the application-specific admin role, and the **Application Administrator** check box is selected.

4.  In the role record, select the **Application Administrator** check box, and then click **Update**.

5.  Navigate to **System Applications** &gt; **My Company Applications**.

6.  Open the user record for the admin user.

7.  On the Roles tab, add the application-specific role.

    Only users with the application-specific admin role can enable application administration for an application.

    **Note:** Assign the application-specific admin role to more than one user. Then, if a user with the application-specific admin role leaves the company, you are not prevented from performing changes to the application.

8.  Click **Update**.

9.  Log out and then log in with the application-specific admin role.

10. Navigate to **System Applications** &gt; **Applications**.

11. Select the application for which you want to enable application administration.

12. In the application record, select **Application administration**.

13. Click **Update**.

    The system validates that the following requirements have been met:

    -   The application has an application-specific admin role \(there is at least one role with **Application Administrator** selected\).
    -   The current user has the application-specific admin role.
    If the validation passes, the system updates the application record. Otherwise, the system displays this error message and does not update the application record:

    ```
    Application Administration uses the 'Application Administrator' role to define what users are application administrators. None of the roles defined by this application have 'Application Administrator' enabled.
    ```

14. From the Related Links, you can select one of the following options:

<table id="table_n1z_hdf_dbb"><thead><tr><th>

Related Link

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manage Developers

</td><td>

Modal that enables the application-specific admin to manage these tasks: -   Designate developers for the application.
-   Make themselves a delegated developer. After the application-specific admin becomes a delegated developer, the application-specific admin can perform a subset of administration tasks without having the system-level admin role.
 Learn more: [Delegated development and deployment](../concept/c_DelegatedDevelopment.md)

</td></tr><tr><td>

Grant application administration to all admins

</td><td>

Modal that creates a Contained Role \[sys\_user\_role\_contains\] record for the system-level admin role. This adds the application-specific admin role as a contained role of the system-level admin role.**Note:** When you publish the application with this record, users with the application-specific admin role can access the application after installing it.

</td></tr></tbody>
</table>
