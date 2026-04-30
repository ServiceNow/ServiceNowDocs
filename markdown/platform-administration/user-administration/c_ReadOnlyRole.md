---
title: Read-only role
description: The read-only role \(snc\_read\_only\) restricts a user or a group of users to read-only access on the tables to which the user already has access.If it isn’t already active, an administrator can activate the Read-Only User Role \(com.snc.read\_only.role\) plugin.These system properties control the snc\_read\_only role. The following default values are used for the properties.
locale: en-US
release: yokohama
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Base system roles, Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Read-only role

The read-only role \(snc\_read\_only\) restricts a user or a group of users to read-only access on the tables to which the user already has access.

This role is designed to complement other roles a user possesses. Its purpose is to restrict actions like the insert, update, or delete operations on the tables accessible through their existing roles.

After you assign this role to a user, they can no longer create, update, or delete records on ANY tables.

**Note:** Assign this role only to users. Don’t assign this role to other resources in the system, including applications, access control levels \(ACLs\), and so on.

The snc\_read\_only role can be assigned to any user to limit access to data without having to create ACLs for system tables, custom tables, and fields. This practice is useful for performing internal or external audits without enabling a user to have insert or update access to data.

Users with the snc\_read\_only role have the following restrictions regardless of other roles and privileges that they have.

-   Can’t insert, update, or delete records from the UI or when using the GlideRecord API.
-   Can’t activate or upgrade plugins.
-   Can’t directly run SQL.
-   Can’t upload XML files.
-   Can only run background scripts when on an instance in the public sandbox environment.

**Note:** These role restrictions are in place even if impersonating another user with write access such as an admin.

**Parent Topic:**[Base system roles](../../roles/reference/r_BaseSystemRoles.md)

## Activate the read-only role

If it isn’t already active, an administrator can activate the Read-Only User Role \(com.snc.read\_only.role\) plugin.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Read-Only User Role \(com.snc.read\_only.role\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## Read-only role properties

These system properties control the snc\_read\_only role. The following default values are used for the properties.

<table id="simpletable_tqr_1hx_4zb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.security.snc\_read\_only\_role.tables.exempt\_create**

</td><td>

Specifies which tables are exempt from the read-only role enforcement and enable the creation of new records.

 -   Type: string
-   Default value: sys\_user\_session, sysevent, syslog, syslog\_transaction, sys\_user\_preference, sys\_ui\_list, sys\_ui\_list\_element, sys\_db\_cache, user\_multifactor\_auth
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.security.snc\_read\_only\_role.tables.exempt\_write**

</td><td>

Specifies which tables are exempt from the read-only role enforcement and enable the updating of existing records.

 -   Type: string
-   Default value: sys\_user\_session, sysevent, syslog, syslog\_transaction, sys\_user\_preference, sys\_ui\_list, sys\_ui\_list\_element, sys\_db\_cache, user\_multifactor\_auth
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.security.snc\_read\_only\_role.tables.exempt\_delete**

</td><td>

Specifies which tables are exempt from the read-only role enforcement and enable the deletion of existing records.

 -   Type: string
-   Default value: sys\_user\_preference, sys\_ui\_list, sys\_ui\_list\_element, sys\_db\_cache, user\_multifactor\_auth
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>After you configure these properties, assign the read-only role as needed. When you log in, you’re restricted from creating, updating, or deleting records on ANY tables unless you modified these properties.

**Note:** Test the read-only role by assigning it to a user and then impersonating that user.

