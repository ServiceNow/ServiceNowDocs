---
title: Components installed with Targeted Communications
description: Several types of components are installed with the Targeted Communications application.Tables are added with activation of Targeted Communications.Roles are added with activation of Targeted Communications.Properties are added with activation of Targeted Communications.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Customer Service Management, Reference, Customer Service Management]
---

# Components installed with Targeted Communications

Several types of components are installed with the Targeted Communications application.

## Tables installed with Targeted Communications

Tables are added with activation of Targeted Communications.

<table id="table_v3f_nzd_z5"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recipients \(Users\)\[sn\_publications\_recipientslist\_user\_m2m\]

</td><td>

Stores recipients lists of type Internal Users.

</td></tr><tr><td>

Recipients \(Accounts\)\[sn\_publications\_recipientslist\_account\_m2m\]

</td><td>

Stores recipients lists of type Accounts.

</td></tr><tr><td>

Recipients \(Consumers\)\[sn\_publications\_recipientslist\_consumer\_m2m\]

</td><td>

Stores recipients lists of type Consumers.

</td></tr><tr><td>

Publication Recipients\[sn\_publications\_publication\_contact\_m2m\]

</td><td>

Stores recipients lists of type Contacts.

</td></tr><tr><td>

Workflow Config\[sn\_publications\_workflow\_config\]

</td><td>

Workflow configuration page.

</td></tr><tr><td>

Publication \[sn\_publications\_publication\]

</td><td>

Stores all publications.

</td></tr><tr><td>

Recipients List \[sn\_publications\_recipients\_list\]

</td><td>

Stores the recipient lists.

</td></tr><tr><td>

Recurrence \[sn\_publications\_recurrence\]

</td><td>

Stores all of the publication recurrences.

</td></tr></tbody>
</table>## Roles installed with Targeted Communications

Roles are added with activation of Targeted Communications.

<table id="table_a5d_nck_55"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Publications administrator\[sn\_publications.admin\]

</td><td>

The publications administrator can:-   read all publications
-   create, update, and delete publications
-   create recurring publications
-   create recipient lists
-   add or remove approvers to workflows

</td><td>

-   sn\_publications.author
-   sn\_publications.approver
-   workflow\_publisher
-   image\_admin

</td></tr><tr><td>

Publications author\[sn\_publications.author\]

</td><td>

The publications author can:-   read all publications
-   create, update, and delete publications
-   create recurring publications
-   create recipient lists

</td><td>

-   sn\_publications\_recipients\_list\_user
-   sn\_publications\_recipients\_user
-   workflow\_publisher
-   image\_admin
-   sn\_esm\_agent

</td></tr><tr><td>

Publications approver\[sn\_publications.approver\]

</td><td>

The publications approver can approve publications.

</td><td>

approver\_user

</td></tr><tr><td>

Recipients list user\[sn\_publications\_recipients\_list\_user\]

</td><td>

The recipients list user can create and view recipient lists.

</td><td>

None

</td></tr><tr><td>

Recipients user\[sn\_publications\_recipients\_user\]

</td><td>

The recipients user can view recipient lists.

</td><td>

None

</td></tr></tbody>
</table>## Properties installed with Targeted Communications

Properties are added with activation of Targeted Communications.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_publications.max\_email

</td><td>

Limits the number of email recipients.-   **Type**: integer
-   **Default value**: 100000
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>