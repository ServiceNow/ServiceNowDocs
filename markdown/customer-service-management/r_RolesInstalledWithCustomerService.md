---
title: Roles installed with Customer Service Management
description: The Customer Service Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Components installed with Customer Service Management, Reference, Customer Service Management]
---

# Roles installed with Customer Service Management

The Customer Service Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users.

## Primary roles

Customer Service Management provides several primary roles that support the following business models:

-   Business-to-business \(B2B\): With this business model, you can support accounts and contacts. Additionally, you can create relationships and account teams to support your customers.
-   Business-to-consumer \(B2C\): With this business model, you can support individual consumers.

These roles ensure access to data while maintaining data security for different types of business relationships.

<table id="table_ql1_rw4_rkb"><thead><tr><th>

Internal Roles

</th><th>

External Roles

</th></tr></thead><tbody><tr><td>

**Business-to-business \(B2B\)** -   sn\_customerservice\_agent
-   sn\_customerservice\_manager

</td><td>

**Business-to-business \(B2B\) Customer** -   sn\_customerservice.customer
-   sn\_customerservice.customer\_admin
-   sn\_customerservice.customer\_case\_manager

</td></tr><tr><td>

**Business-to-consumer \(B2C\)** -   sn\_customerservice.consumer\_agent
-   sn\_customerservice\_manager

</td><td>

**Business-to-business \(B2B\) Partner** -   sn\_customerservice.partner
-   sn\_customerservice.partner\_admin

</td></tr><tr><td>

 

</td><td>

**Business-to-consumer \(B2C\)** sn\_customerservice.consumer

</td></tr></tbody>
</table>For details about these roles, see [CSM roles and descriptions](r_RolesInstalledWithCustomerService.md#section_p5t_gcr_3mb) below.

## Internal and external roles

Customer Service Management includes both internal and external user roles.

-   Internal roles are assigned to users within your organization. These roles are for agents and managers using the Customer Service Management application to support customers.
-   External roles are assigned to users outside your organization. These roles are for customers, customer partners, and consumers using the self-service portals.

With these roles, you can give both internal users and external users access to your instance. This role structure gives you the flexibility to provide different levels of access to different users. As an additional security measure, every user must have at least one role so that the instance can distinguish between internal and external users.

## Base roles

The primary roles available in Customer Service Management are based on the following base roles:

-   sn\_esm\_agent
-   sn\_esm\_admin
-   sn\_esm\_partner
-   sn\_esm\_partner\_admin
-   sn\_esm\_user
-   sn\_esm\_user\_admin

For more information about these roles, see [Roles installed with the Customer Service Base Entities plugin](r_RolesInstalledWithCustomerService.md#section_uff_bbj_x2b) below.

For more information about the CSM primary role structure and included roles, see [CSM roles and descriptions](r_RolesInstalledWithCustomerService.md#section_p5t_gcr_3mb) below.

## Explicit roles

You may have business requirements that change the use of these roles. In addition, the [Explicit Roles in CSM](../../../administer/contextual-security/concept/explicit-roles-in-csm.md) feature may assign both internal and external roles to external users. It is important to regularly review user role assignments to ensure that they are set according to your business requirements.

For more information about reviewing and updating user role assignments, see:

-   [KB0829930](https://support.servicenow.com/kb_view.do?sysparm_article=KB0829930)
-   [Fix external user role assignments](../concept/fixing-external-role-assignment.md)

## CSM roles and descriptions

<table id="table_fch_3kk_w5b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Customer service agent\[sn\_customerservice\_agent\]

</td><td>

An agent who assists customers and partners with questions, issues, and problems. This user creates cases, views and edits cases, and works with customers and subject matter experts to resolve cases.A customer service agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

</td><td>

-   knowledge
-   chat\_admin
-   sn\_customerservice.deescalation\_requester
-   timecard\_user
-   template\_editor
-   sn\_esm\_agent
-   sn\_shn.editor
-   domain\_expand\_scope

 **Note:** The sn\_esm\_agent role contains the cmdb\_read role.

</td></tr><tr><td>

Customer service manager\[sn\_customerservice\_manager\]

</td><td>

Customer service agent with the additional responsibility for managing agents or agent groups and overriding agent actions.

</td><td>

-   sn\_customerservice\_agent
-   timecard\_manager
-   timecard\_approver
-   skill\_admin
-   sn\_app\_cs\_social\_social\_profile\_user
-   sn\_customerservice.consumer\_agent
-   asset
-   sn\_shn.admin
-   sn\_publications.approver
-   contract\_manager
-   sn\_app\_cs\_social\_log\_user
-   awa\_manager
-   sn\_majorissue\_mgt.major\_issue\_manager
-   email\_client\_quick\_message\_author
-   workspace\_admin
-   skill\_model\_user
-   sn\_templated\_snip.template\_snippet\_writer
-   approver\_user

**Note:** For customers upgrading to Xanadu, the approver\_user role replaces the approval\_admin role. Users with the customer service manager role can approve the approval requests that are assigned to them.

-   notify\_view

**Note:** The notify\_view role is added to the sn\_customerservice\_manager role only when the Chat Zoom Connector application is installed.


</td></tr><tr><td>

Consumer service agent\[sn\_customerservice.consumer\_agent\]

</td><td>

An agent who assists consumers with questions, issues, and problems. This user creates, views, and edits cases and works with consumers to resolve cases. An agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

</td><td>

-   sn\_esm\_agent
-   chat\_admin
-   sn\_shn.editor
-   template\_editor
-   knowledge

</td></tr><tr><td>

Customer\[sn\_customerservice.customer\]

</td><td>

Customer role for researching questions, issues, or problems. Customers can create cases and view and edit existing cases for themselves. They can also view a list of assets belonging to their accounts.

</td><td>

-   sn\_esm\_user
-   snc\_external

</td></tr><tr><td>

Customer administrator\[sn\_customerservice.customer\_admin\]

</td><td>

Administrator role for a customer account. This user has access to data within the account.

</td><td>

-   sn\_customerservice.customer
-   sn\_esm\_user\_admin

</td></tr><tr><td>

Customer case manager\[sn\_customerservice.customer\_case\_manager\]

</td><td>

Customer role for managing the cases in an account and any related child accounts. The customer case manager role includes the privileges of the customer role and adds the following privileges:-   Create a case on behalf of another contact in the account.
-   View a list of cases belonging to the account.
-   Edit cases belonging to the account.

 **Note:** The customer case manager role is not automatically added to the **sn\_customerservice.contact\_role\_assignment** system property. To expose this role to customer and partner administrators, navigate to **Customer Service** &gt; **Administration** &gt; **Properties** and add it to this property.

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Partner\[sn\_customerservice.partner\]

</td><td>

Partner who is serving customer accounts. A partner can create a case for their own account or on behalf of a customer account.

 A partner can view and edit all of the cases that they have created:

-   For their own account.
-   On behalf of customer accounts that they are related to.

**Note:** If you are establishing a new relationship between a partner and a customer, the partner or partner admin does not have access to historic cases created for the customer. This is because the historic cases do not have the **Partner** or **Partner Contact** fields populated on the Case form.

</td><td>

-   sn\_customerservice.customer
-   sn\_esm\_partner

</td></tr><tr><td>

Partner administrator\[sn\_customerservice.partner\_admin\]

</td><td>

Administrator role for a partner account. The partner administrator can do the following:

-   Access the data within the partner account.
-   Access the data created by the contacts in their company in the customer account.
-   Manage users for the partner account and for customer accounts.
-   View all of the cases created by a partner.

</td><td>

-   sn\_customerservice.partner
-   sn\_customerservice.customer\_admin
-   sn\_esm\_partner\_admin

</td></tr><tr><td>

Consumer\[sn\_customerservice.consumer\]

</td><td>

Consumer role for researching questions, issues, or problems. Consumers can create cases and view and edit existing cases for products that they have purchased. They can also view a list of their products.

</td><td>

-   sn\_esm\_user
-   snc\_external

</td></tr></tbody>
</table><table id="table_bxx_zpb_kt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Case contributor editor\[sn\_customerservice.case\_contributor\_editor\]

</td><td>

This role provides limited write access to the fields on the Case form. It provides limited write access to those cases for which the user already has read access provided by another role.

 Limited write access is available for the following fields:

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

This role provides read-only access to all of the tables associated with a case.With this role, a user can view the information in the related lists for a case if:

 -   The user has been added to the **Contributor User** field or the **Contributor Group** field on the Case form.
-   The user has read-only access to cases through another role, such as the case viewer role \(sn\_customerservice.case\_viewer\) or the case task agent role \(sn\_customerservice.case\_task\_agent\).

 With this role, a user can access the following modules in CSM Agent Workspace:**All tasks I participate in**

</td><td>

-   sn\_shn.user
-   wm\_read

</td></tr><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

This role provides access to case tasks and related case information. A user with this role can work on the following case tasks: -   Tasks that are assigned to the user or to the user's assignment groups.
-   Tasks that have been created by the user.

 With this role, the user can:

-   View and update assigned case tasks.
-   Create case tasks and assign those tasks to other users.
-   View and update created case tasks.
-   Add work notes, comments, and attachments to case tasks.
-   Update the status of case tasks.
-   Perform additional actions from a case task such as sending email.

 With this role, users have read-only access to customer information for the case:

-   Account and contact records \(for B2B cases\)
-   Consumer and household records \(for B2C cases\)
-   Service organization records \(business location cases\)

</td><td>

-   sn\_customerservice.customer\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.case\_contributor\_editor

</td></tr><tr><td>

Case task viewer\[sn\_customerservice.case\_task\_viewer\]

</td><td>

This role provides read-only access to all case task records. **Note:** When combined with the case viewer role \(sn\_customerservice.case\_viewer\), a user can access all customer service cases and all case tasks.

</td><td>

 

</td></tr><tr><td>

Case viewer\[sn\_customerservice.case\_viewer\]

</td><td>

This role provides read-only access to all cases.

</td><td>

 

</td></tr><tr><td>

Contact manager\[sn\_customerservice.contact\_manager\]

</td><td>

User who can manage contacts.

</td><td>

 

</td></tr><tr><td>

Customer project manager\[sn\_customerservice.projectmanager\]

</td><td>

A user who creates and manages projects for customer accounts.-   Creates new projects.
-   Sets up project tasks and resource plans.
-   Identifies customer contacts who have access to projects and project tasks.
-   Assigns and manages tasks and dependencies.

 **Note:** This role is added with the Customer Project Management plugin \(com.snc.csm\_ppm\)

</td><td>

sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

Customer project stakeholder\[sn\_customerservice.projectstakeholder\]

</td><td>

A user who is responsible for activities that require viewing customer project details and project tasks.**Note:** This role is added with the Customer Project Management plugin \(com.snc.csm\_ppm\)

</td><td>

 

</td></tr><tr><td>

Customer Data viewer\[sn\_customerservice.customer\_data\_viewer\]

</td><td>

User with read-only access to customer data entities such as:-   Install base items
-   Contracts
-   Entitlements
-   Accounts, contacts, and account team members
-   Assets
-   Consumers
-   Sold product

**Note:** Starting with the Australia release, the Customer Data Viewer \[sn\_customerservice.customer\_data\_viewer\] role has extended access to the following tables:

-   Account Relationship \[account\_relationship\]
-   Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]
-   Contact Relationship \[sn\_customerservice\_contact\_relationship\]
-   Account Consumer \[sn\_acct\_consumer\_account\_consumer\]
-   Consumer Team Member \[sn\_customer\_rel\_consumer\_to\_user\]
-   Consumer to Consumer Relationship \[sn\_customer\_rel\_consumer\_to\_consumer\]
-   Household Member Relationship \[sn\_customer\_rel\_household\_member\_relationship\]
-   Household Team Member \[sn\_customer\_rel\_household\_to\_user\]
-   Responsibility Definition \[sn\_customerservice\_responsibility\_def\]
-   Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\]

Additionally, it also has access to the following menu modules and workspace lists.

-   Menu modules: Customer, Partners, Contacts, Consumers, and Households
-   Workspace lists: Partners

</td><td>

 

</td></tr><tr><td>

De-escalation requester \[sn\_customerservice.deescalation\_requester\]

</td><td>

User who can deescalate a case or account when the cause of the escalation is resolved.

</td><td>

sn\_customerservice.escalation\_requester

</td></tr><tr><td>

Escalation requester \(sn\_customerservice.escalation\_requester\)

</td><td>

User who can request an escalation for a case or account.

</td><td>

sn\_customerservice.consumer\_agent

</td></tr><tr><td>

Proxy case creator\[sn\_customerservice.proxy\_case\_creator\]

</td><td>

Users with the proxy case creator role can create customer service cases directly from community questions created by contacts or consumers

</td><td>

 

</td></tr><tr><td>

Proxy contact\[sn\_customerservice.proxy\_contact\]

</td><td>

Role that enables employees to create cases for customer accounts and contacts. Employees can also be proxy case contacts on behalf of customers. Assign this role to employees in your company who are not fulfillers or do not have other CSM-specific roles. Users with this role can:

-   Create customer service cases using a record producer.
-   Add work notes and comments to any case.
-   Update the watch list of any case.

**Note:** The CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\) plugin adds this role.

</td><td>

 

</td></tr><tr><td>

Workspace user \[sn\_customerservice.csm\_workspace\_user\]

</td><td>

This role provides access to case tasks from the following modules in CSM Agent Workspace:-   My Case Tasks
-   My Group's Case Tasks

 Users can also:

-   Use Agent Assist to search for knowledge articles \(if the User Criteria is set to provide access to knowledge\).
-   Create email \(if the user has write access to the record and the email\_composer role\).
-   View response templates \(if response templates have been configured for the record.

**Note:** By default, this role is added to the case task agent role \(sn\_customerservice.case\_task\_agent\).

</td><td>

 

</td></tr></tbody>
</table>For detailed information on the granular admin roles in Custmer Data Foundation \(CDF\) and their associated privileges, see [Platform security granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platsec-granular-roles.md).

## Roles installed with the Customer Service Base Entities plugin

The following roles are installed with the Customer Service Base Entities plugin.

<table id="table__csm_base_entities_plugin_roles"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

CSM admin\[csm\_admin\]

</td><td>

Provides admin access to all CSM features and data.

</td><td>

-   sn\_shn.admin
-   sn\_res\_shaper.admin

</td></tr><tr><td>

Service management agent

 \[sn\_esm\_agent\]

</td><td>

 

</td><td>

-   assignment\_workbench
-   wm\_read
-   cmdb\_read
-   agent\_schedule\_user
-   interaction\_agent

</td></tr><tr><td>

Service management partner\[sn\_esm\_partner\]

</td><td>

 

</td><td>

sn\_esm\_user

</td></tr><tr><td>

Service management user admin\[sn\_esm\_user\_admin\]

</td><td>

 

</td><td>

sn\_esm\_user

</td></tr><tr><td>

Service management admin\[sn\_esm\_admin\]

</td><td>

 

</td><td>

None

</td></tr><tr><td>

Service management user\[sn\_esm\_user\]

</td><td>

 

</td><td>

-   snc\_external
-   sn\_apptmnt\_booking.appointment\_booking\_user

</td></tr><tr><td>

Service management partner admin\[sn\_esm\_partner\_admin\]

</td><td>

 

</td><td>

-   sn\_esm\_user\_admin
-   sn\_esm\_admin

</td></tr><tr><td>

Role for REST APIs related to CSM web services\[csm\_ws\_integration\]

</td><td>

 

</td><td>

snc\_internal

</td></tr></tbody>
</table>-   **[Internal user data](../concept/customer-service-internal-user-data.md)**  
Internal user data includes information about the users who are internal to your organization, such as managers, agents, and other employees. Internal users can also belong to user groups.
-   **[Business Stakeholder for Customer Service Management](../concept/business-stakeholder-for-csm.md)**  
Business Stakeholder for Customer Service Management includes plugins and roles that provide access to business stakeholder features.
-   **[Explicit Roles in CSM](../../../administer/contextual-security/concept/explicit-roles-in-csm.md)**  
You can give both internal users and external users access to your instance. However, you might not want both types of users to have the same level of access. To provide added security, every user must have at least one role so that the instance can distinguish between internal and external users.
-   **[Provide external users access to a table](../../../administer/contextual-security/task/t_ProvideExternalUsersAccessToTables.md)**  
To enable users with only the snc\_external role to access the list view of a table, you must create a series of ACLs.
-   **[Creating custom user roles](../concept/creating-custom-csm-user-roles.md)**  
System administrators can create custom roles or modify the access of existing roles by using script includes and extension points/instances.

**Parent Topic:**[Components installed with Customer Service Management](r_InstalledWithCustomerService.md)

**Related topics**  


[Fix external user role assignments](../concept/fixing-external-role-assignment.md)

