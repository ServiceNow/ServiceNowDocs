---
title: Contributor user roles
description: The contributor user data model includes several roles that control access to cases, case tasks, and related information, assigned to users based on business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-contributor-user-roles.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Contributor users, Configure contributor users, User management, Set up your environment, Configure, Customer Service Management]
---

# Contributor user roles

The contributor user data model includes several roles that control access to cases, case tasks, and related information, assigned to users based on business needs.

These roles are included with several different plugins:

-   Case Management Core \(com.sn\_customerservice\)
-   CSM Contributor User \(com.snc.csm\_contributor\_user\)
-   Business Location \(com.snc.business\_location\)
-   CSM Base Extension Entities \(com.snc.cs\_base\_extension\)

See the following tables for detailed role descriptions.

## Roles included with the Case Management Core plugin

The following table lists the contributor roles that are included with the Case Management Core \(com.sn\_customerservice\) plugin along with their descriptions and associated roles.

<table id="table_q3s_wcc_3nb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

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

Self-contributor\[sn\_customerservice.self\_contributor\]

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

This role enables you to create cases for your service organization \(business location\).**Note:** A service organization contributor must be a member of a service organization to create cases on its behalf.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td></tr><tr><td>

Business Org Account Contributor\[sn\_bus\_loc.business\_org\_account\_contributor\]

</td><td>

This role enables you to create cases for accounts associated with your business organization using criteria-based restricted customer access. Track and manage cases created by you for the accounts associated with your business organization.

</td><td>

 

</td></tr><tr><td>

Business Org Consumer Contributor\[sn\_bus\_loc.business\_org\_consumer\_contributor\]

</td><td>

This role enables you to create cases for consumers and households associated with your business organization using criteria-based restricted customer access. Also, track and manage cases created by you for the consumers or households associated with your business organization.

</td><td>

 

</td></tr></tbody>
</table>## Roles included with the CSM Base Extension Entities plugin

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

This role enables you to create cases for customers with which they have an established relationship. **Note:**

-   The CSM Contributor User \(com.snc.csm\_contributor\_user\) plugin must be activated. This plugin is moved to the App Store beginning with Australia release.
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

This role provides access to case tasks from the following modules in the CSM workspaces for internal users only:-   My Case Tasks
-   My Group's Case Tasks

 You can also:

-   Use Agent Assist to search for knowledge articles \(if the User Criteria are set to provide access to knowledge\).
-   Create email \(if you have the written access to the record and the email\_composer role\).
-   View response templates \(if response templates have been configured for the record\).

**Note:** An external user who is given contributor roles can't access workspace even if they’re given this role.

</td><td>

-   agent\_workspace\_user
-   canvas\_user
-   sn\_templated\_snip.template\_snippet\_reader
-   email\_composer

</td></tr></tbody>
</table>**Related topics**  


[Configure contributor users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-contributor-user.md)

[Contributor users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-service-contributor-users.md)

[Cases and case tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-cases-case-tasks-overview.md)

[Roles installed with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/r_RolesInstalledWithCustomerService.md)

[Business Stakeholder for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/business-stakeholder-for-csm.md)

