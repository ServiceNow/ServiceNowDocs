---
title: Contributor user roles
description: The contributor user data model uses several roles that can be assigned to users to control case access, case tasks, and case-related information based on different business needs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Contributor users, Configure Contributor Users, User management, Set up your environment, Configure, Customer Service Management]
---

# Contributor user roles

The contributor user data model uses several roles that can be assigned to users to control case access, case tasks, and case-related information based on different business needs.

These roles are included with several different plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM Contributor User \(com.snc.csm\_contributor\_user\)
-   Business Location \(com.snc.business\_location\)
-   CSM Base Extension Entities \(com.snc.cs\_base\_extension\)

See the following tables for detailedrole descriptions.

## Roles included with the Customer Service plugin

The following table lists the contributor roles that are included with the Customer Service \(com.sn\_customerservice\) plugin along with their descriptions and associated roles.

<table id="table_q3s_wcc_3nb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

This role provides access to case tasks and related case information. A user with this role can work on the following case tasks:

-   Tasks that are assigned to the user or to the user's assignment groups.
-   Tasks that have been created by the user.

 With this role, the user can:

-   View and update case tasks.
    -   Add work notes, comments, and attachments.
    -   Update the status.
    -   Perform additional actions from a case task such as sending email.
-   Create case tasks and assign them to other users.

 With this role, users have read-only access to customer information for the case:

-   Account and contact records \(for B2B cases\)
-   Consumer and household records \(for B2C cases\)
-   Service organization records \(business location cases\)

</td><td>

-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.customer\_data\_viewer
-   sn\_customerservice.case\_contributor\_editor

</td></tr><tr><td>

Case task viewer\[sn\_customerservice.case\_task\_viewer\]

</td><td>

This role provides read-only access to all case tasks. **Note:** When combined with the case viewer role \(sn\_customerservice.case\_viewer\), a user can access all customer service cases and all case tasks.

</td><td>

 

</td></tr><tr><td>

Case viewer\[sn\_customerservice.case\_viewer\]

</td><td>

This role provides read-only access to all cases.

</td><td>

 

</td></tr><tr><td>

Case contributor editor\[sn\_customerservice.case\_contributor\_editor\]

</td><td>

This role provides limited write access to some of the fields on the Case form if the user has read access to the case through another role. Limited write access is available for the following fields:

-   Work notes
-   Additional comments
-   Attachments
-   State or stage changes
-   Contributor users
-   Contributor groups
-   Watchlist
-   Work notes list

</td><td>

 

</td></tr><tr><td>

Case contributor viewer\[sn\_customerservice.case\_contributor\_viewer\]

</td><td>

This role provides read access to all tables associated with a case if the user has read access to the case through another role. The user can access the **All tasks I participate in** module in CSM Agent Workspace.

</td><td>

-   sn\_shn.user
-   wm\_read

</td></tr></tbody>
</table>## Roles included with the CSM Contributor User plugin

The following table lists the contributor roles that are included with the CSM Contributor User \(com.snc.csm\_contributor\_user\) plugin along with their descriptions and associated roles.

<table id="table_e1g_bnt_jnb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Account contributor\[sn\_customerservice.account\_contributor\]

</td><td>

This role enables users to create cases for any account.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr><tr><td>

Consumer contributor\[sn\_customerservice.consumer\_contributor\]

</td><td>

This role enables users to create cases for any consumer.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr><tr><td>

Self contributor\[sn\_customerservice.self\_contributor\]

</td><td>

This role enables users with snc\_internal role to create cases for themselves.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr><tr><td>

Case contributor creator\[case\_contributor\_creator\]

</td><td>

This role enables users to create cases and is included in the top-level contributor roles.

</td><td>

 

</td></tr></tbody>
</table>## Roles included with the Business Location plugin

The following contributor roles are included with the Business Location plugin \(com.snc.business\_location\).

<table id="table_fcs_brt_jnb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service organization contributor \[sn\_customerservice.service\_organization\_contributor\]

</td><td>

This role enables users to create cases for their service organization \(business location\).**Note:** A service organization contributor must be a member of a service organization to create cases on its behalf.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr></tbody>
</table>## Roles included with the CS Base Extension Entities plugin

The following contributor roles are included with the CSM Base Extension Entities plugin \(com.snc.cs\_base\_extension\).

<table id="table_phg_y4t_jnb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Relationship contributor \[sn\_customerservice.relationship\_contributor\]

</td><td>

This role enables users to create cases for customers with which they have an established relationship. **Note:**

-   The CSM Contributor User \(com.snc.csm\_contributor\_user\) plugin must be activated.
-   A relationship contributor must be a member of an account, contact, or household team to create cases on their behalf.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr></tbody>
</table>## Additional roles

<table id="table_hbc_drt_jnb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Customer data viewer\[sn\_customerservice.customer\_data\_viewer\]

</td><td>

This role provides read access to customer data, including account, consumer, and household data, and the information included in the related lists.

</td><td>

 

</td></tr><tr><td>

Workspace user\[sn\_customerservice.csm\_workspace\_user\]

</td><td>

This role provides access to case tasks from the following modules in the CSM workspaces:-   My Case Tasks
-   My Group's Case Tasks

 Users can also:

-   Use Agent Assist to search for knowledge articles \(if the User Criteria is set to provide access to knowledge\).
-   Create email \(if the user has write access to the record and the email\_composer role\).
-   View response templates \(if response templates have been configured for the record.

**Note:** By default, this role is added to the case task agent role \(sn\_customerservice.case\_task\_agent\).

</td><td>

-   agent\_workspace\_user
-   canvas\_user
-   sn\_templated\_snip.template\_snippet\_reader
-   email\_composer

</td></tr></tbody>
</table>