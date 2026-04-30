---
title: Create the MID Server user and grant the role
description: To communicate with the instance, MID Servers need a user ID and the appropriate role. Create the user ID for a MID Server and grant the ID the mid\_server role. To prevent MID Server validation failure, the system runs business rules to monitor the settings selected for MID Server users.Real-time system validation of MID Server role assignments prevents incompatible settings.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create the MID Server user and grant the role

To communicate with the instance, MID Servers need a user ID and the appropriate role. Create the user ID for a MID Server and grant the ID the **mid\_server** role. To prevent MID Server validation failure, the system runs business rules to monitor the settings selected for MID Server users.

## Before you begin

Role required: admin

<table id="table_skp_xr4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

The MID Server connects to an instance by using the SOAP web service. To allow authentication with the instance, create a separate user account for each MID Server or share the same account across multiple MID Servers. Grant each MID Server user the mid\_server role, which is required for the MID Server user on any instance on which basic authentication is enabled. The mid\_server role allows the MID Server to access protected tables when strict SOAP security is in place. The system adds the necessary SOAP roles automatically with this role.

**Note:** The strict SOAP security feature, enabled by default for any instance that uses basic authentication, protects all tables with Access Control Lists \(ACL\).

If multiple MID Servers are using the same logged in user, an issue record is created when more than one is **Up** at a time. It is recommended that MID Servers use a unique logged in user. See [\(KB1552863\) MID Server Unique Logged In User](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1552863) for more information and remediation steps.

## Procedure

1.  From the instance, navigate to **User Administration** &gt; **Users**.

2.  Click **New**.

3.  Complete the fields in the form.

<table id="table_isc_b4z_r1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

User name for the MID Server user. This name is specified in the **mid.instance.username** parameter of the configuration file that the MID Server installer creates. For details, see [MID Server parameters](../reference/mid-server-parameters.md#).

 **Note:** Avoid using the same MID Server logged in user across multiple MID Servers.

</td></tr><tr><td>

First name

</td><td>

The user's first name.

</td></tr><tr><td>

Last name

</td><td>

The user's last name.

</td></tr><tr><td>

Password

</td><td>

Password for the MID Server user. This password is specified in the **mid.instance.password** parameter of the configuration file that the MID Server installer creates.

</td></tr></tbody>
</table>4.  Right-click the header and select **Save**.

5.  Under the **Roles** related list, click **Edit**.

6.  Select the **mid\_server** role for this user.

    Each MID Server account must have this role to access protected tables.

7.  Click **Save**.

8.  Confirm that the MID Server account was created successfully and the account has connectivity to the instance.

    1.  On the host machine where you intend to install the MID Server, open a browser and navigate to the instance.

    2.  Use your new MID Server user credentials to log in.

        If the login is successful, then any MID Servers you install on that host will be able to connect to the instance.


## MID Server role validation

Real-time system validation of MID Server role assignments prevents incompatible settings.

To prevent MID Server validation failure and ensure that your MID Server is configured correctly, the system runs several business rules that monitor the roles and settings you select for your MID Server user. The instance displays a warning and blocks the change when you attempt to save an incompatible configuration.

### Elevated privileges not permitted

The mid\_server role cannot be configured for elevated privileges. The **Invalid MID Server settings** business rule runs on the Role \[sys\_user\_role\] table and prevents the **elevated\_privileges** field from being set to true for the mid\_server role.

![MID Server role](../image/ElevatedPrivilegeWarning.png "Warning for elevated privileges on the mid_server role")

### Relationship table protection

The User Role \[sys\_user\_has\_role\] table creates the relationship between the User \[sys\_user\] and the Role \[sys\_user\_role\] tables.

-   **Incompatible role**

    The mid\_server and security\_admin roles are incompatible and cannot be assigned to the same user. The system determines the user's current role and runs the **Security Admin incompatible with MID** business rule on the User Role \[sys\_user\_has\_role\] table. This rule prevents an administrator from adding the security\_admin role for a user who currently has the mid\_server role.

    ![Warnings for incompatible security_admin role assignment](../image/SecurityAdminRoleBlocked.png "Warnings for incompatible security_admin role assignment")

-   **Incompatible user role and user record settings**

    The **Incompatible MID Server user role** business rule runs on the User Role \[sys\_user\_has\_role\] table to protect its data from incompatible configurations. Validation for this related table ensures that an administrator cannot assign the mid\_server role to a user who already holds the security\_admin role.


### What to do next

[Download](t_DownloadMIDServerFiles.md) the MID Server files for your operating system.

