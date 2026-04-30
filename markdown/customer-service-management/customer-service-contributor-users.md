---
title: Contributor users
description: With contributor user role, you can engage both internal and external users to resolve the customer issues and requests. This functionality is applicable to the users, recorded within the User \(sys\_user\) table who possess either the snc\_internal or snc\_external role and external users, recorded within the Service Organization External Staff \(sn\_csm\_service\_organization\_external\_staff\) table who possess snc\_external role.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Configure Contributor Users, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Contributor users

With contributor user role, you can engage both internal and external users to resolve the customer issues and requests. This functionality is applicable to the users, recorded within the User \(sys\_user\) table who possess either the snc\_internal or snc\_external role and external users, recorded within the Service Organization External Staff \(sn\_csm\_service\_organization\_external\_staff\) table who possess snc\_external role.

**Note:** The contributor user role don't extend to the users belonging to the Contacts \(customer\_contact\) class who are snc\_external role.

The contributor users feature provides unified customer support for internal and external customers. With this feature, you can serve internal and external customers through shared service teams and service organizations:

-   Enable service organizations to serve one another and external customers.
-   Enable employees to request support for themselves and for external customers.
-   ​Enable middle office agents to work on specific tasks that are required to resolve cases.

## Overview of contributor user roles

The contributor users feature includes several roles that you can assign to users to control access to cases, case tasks, and case-related information. These roles can be assigned to users based on different business needs. In some cases, these roles also provide access to the parent cases and associated customer information.

![Table that defines contributor user roles. For a text description, refer to the Contributor user role description and capabilities table.](../image/csm-contributor-user-role-diagram.png "Contributor user roles")

The contributor users feature also includes viewer roles that enable employees to view cases, cases tasks, or core customer data. These roles include:

-   Case Viewer
-   Case Task Viewer
-   Customer Data Viewer

<table id="table_odd_ppj_snb"><thead><tr><th>

Requester type

</th><th>

Description

</th><th>

Capabilities

</th></tr></thead><tbody><tr><td>

Requester for any customer

</td><td>

A requester who can create cases on behalf of any customer.

 This user:

-   Works with accounts and contacts or consumers.
-   Uses the Customer or Consumer Service Portal to assist customers.

 Roles:

-   Account contributor \(sn\_customerservice.account\_contributor\)
-   Consumer contributor \(sn\_customerservice.consumer\_contributor\)

</td><td>

This user can:

-   Search knowledge articles and catalog items.
-   Create cases for customers who visit a business location, including cases for catalog items \(requests\).
-   Create cases from communication channels available to customers including phone, web, chat, Virtual Agent, and messaging.

 If also an internal user on a case, this user can:

-   Add additional comments and attachments
-   Accept or reject a solution
-   Close a case
-   Receive notifications of case updates
-   Read work notes

</td></tr><tr><td>

Requester for my customers

</td><td>

A requester who can create cases on behalf of customers with whom they have an established relationship.

 This user:

-   Works with accounts and contacts or consumers.
-   Uses the Customer or Consumer Service Portal to assist customers.
-   Manages customer relationships and assists with customer cases.

 Role: Relationship contributor \(sn\_customerservice.relationship\_contributor\)​

</td><td>

This user can:

-   Search knowledge articles and catalog items.
-   Create cases on behalf of customers with whom they have a relationship.
-   Create cases from communication channels available to customers including phone, web, chat, Virtual Agent, and messaging.
-   View and follow up on all cases created for customers with whom they have a relationship.
-   Update customer data such as adding contacts and addresses.
-   Update cases:
    -   Add additional comments and attachments
    -   Accept or reject a solution
    -   Close a case
    -   Receive notifications of case updates
    -   Read work notes

</td></tr><tr><td>

Requester for service organization

</td><td>

A requester who can create cases on behalf of their business location.

 This user:

-   Works with accounts and contacts, consumers, and households.
-   Uses the Customer or Consumer Service Portal to assist customers.

 Role: Service organization contributor \(sn\_customerservice.service\_organization\_contributor\)

</td><td>

This user can:

-   Search knowledge articles and catalog items.
-   Create cases on behalf of their business location, including cases for catalog items \(requests\), and follow up on those cases.
-   Create cases from communication channels available to customers including phone, web, chat, Virtual Agent, and messaging.
-   View and follow up on other cases created for the user's business location.

 If also an internal user on a case, this user can:

-   Add additional comments and attachments
-   Accept or reject a solution
-   Close a case
-   Receive notifications of case updates
-   Read work notes

</td></tr><tr><td>

Requester for self

</td><td>

A requester who can create cases for themselves.

 This requester accesses cases through a unified employee portal, if provided by their organization.

 Role: Self contributor \(sn\_customerservice.self\_contributor​\)

</td><td>

This user can:

-   Search knowledge articles and catalog items.
-   Create cases on behalf of themselves, including cases for catalog items \(requests\).
-   Create cases from communication channels available to customers including phone, web, chat, Virtual Agent, and messaging.
-   View and follow up on the cases that they have created from themselves:
    -   Add additional comments and attachments
    -   Accept or reject a solution
    -   Close a case
    -   Receive notifications of case updates
    -   Read work notes

</td></tr><tr><td>

Case task agent

</td><td>

A fulfiller, such as a middle office agent, who works on a specific set of tasks required to resolve a case. These case tasks:

-   Are assigned to the agent or to their department or group.
-   Focus on a specific function or expertise of the department or group.

 This agent typically uses a workspace to complete these tasks.

 Role: Case task agent \(sn\_customerservice.case\_task\_agent​\)

</td><td>

This user can:

-   View and work on the case tasks assigned to them or to their group or department.
-   View the parent cases for the case tasks that they can access.
-   Communicate with agents on the parent case through work notes and additional comments.
-   Communicate with agents on other case tasks for the parent case through work notes and additional comments.
-   Access customer information needed to complete a case task.
-   Make changes to a case task that causes an update to the state or stage of the parent case.
-   Search for knowledge articles to assist with the case task.

</td></tr></tbody>
</table>The contributor user roles are available with different CSM plugins. For a more detailed description of these user roles, see [Contributor user roles](../reference/csm-contributor-user-roles.md).

## Fields added to the Case form

The contributor users feature adds two fields to the Case form that are used to identify the customer for a case. These fields are used in addition to the **Account** and **Consumer** fields.

<table id="table_lzh_skg_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requesting Service Organization

</td><td>

This field displays the name of a service organization. If this field is filled in, and the **Account** and **Consumer** fields are empty, the customer for the case is a service organization. This field is included with the Service Organization plugin \(com.snc.service\_organization\).

</td></tr><tr><td>

Requested By

</td><td>

This field displays the name of the requester. If this field is filled in and the **Account**, **Consumer**, and **Requesting Service Organization** fields are empty, the customer for the case is an employee. This field is included with the Customer Service plugin \(com.sn\_customerservice\).

</td></tr></tbody>
</table>The Customer Service plugin adds two fields to the Notes section of the Case form for contributor users.

<table id="table_apk_mmj_3nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contributor Users

</td><td>

When a user with the case task agent role is assigned to a case task, the user is added to the **Contributor Users** field. If a user is removed from the **Assigned to** field on the Case Task form, and they are not assigned to any other tasks for the case, they are also removed from the **Contributor Users** field.

</td></tr><tr><td>

Contributor Groups

</td><td>

When a user with the case task agent role is assigned to a case task, the user's assignment group is added to the **Contributor Groups** field.If a user is removed from the **Assigned to** field on the Case Task form, and no other member of their assignment group is assigned to any other tasks for the case, the assignment group is removed from the **Contributor Groups** field.

 If a group is removed from the **Assignment group** field on the Case Task form, and the group is not assigned to any other tasks for the case, the assignment group is removed from the **Contributor Groups** field.

</td></tr></tbody>
</table>## Create Case for Customer record producer

The contributor users feature adds a record producer that contributor users can access from the Customer and Consumer Service Portals and use to create cases. When creating a case, this record producer presents different options for the customer in the **Who are you creating this case for?** field, depending on the roles assigned to the logged-in user.

![Create a Customer Case form to describe who the agent is making a case for: account, consumer, business location, or myself.](../image/create-case-for-customer-record-producer.png "Create Case for Customer record producer")

When the contributor user selects an option, additional fields related to that customer type are displayed.

<table id="table_ktz_sng_h4b"><thead><tr><th>

Customer option

</th><th>

Additional fields

</th></tr></thead><tbody><tr><td>

Account

</td><td>

-   **Reported by**: the logged-in user with the account contributor role.
-   **Account**: the name of the account.
-   **Contact**: the contact for the account.

</td></tr><tr><td>

Consumer

</td><td>

-   **Reported by**: the logged-in user with the consumer contributor role.
-   **Consumer**: the name of the consumer.
-   **Household**: the household that the consumer belongs to.

</td></tr><tr><td>

Business Location

</td><td>

-   **Reported by**: the logged-in user with the service organization contributor role.
-   **Requesting Business Location**: the name of the service organization requesting assistance.
-   **Requesting support from Business Location**: the name of the service organization from which the **Requesting Business Location** is asking assistance.

</td></tr><tr><td>

Myself

</td><td>

**Reported By**: the logged-in user with the self contributor role.

</td></tr></tbody>
</table>Additional fields on the record producer that are common to all customer options include **Priority**, **Channel**, **Subject**, and **Description**.

## Viewing record lists on the Customer and Consumer Service Portals

The My Lists widget on the Customer and Consumer Service Portals includes different filters for viewing records.

![My Lists widget with filters for sorting case records. For a text description of the filters, refer to the My Lists filters table.](../image/contributor-users-portal-my-lists-widget.png "My Lists widget on the Customer Service Portal")

Depending on the roles assigned to the logged-in user, this widget displays the following filters.

<table id="table_hxt_4yg_h4b"><thead><tr><th>

Contributor user

</th><th>

My Lists filters

</th></tr></thead><tbody><tr><td>

Account contributor

</td><td>

**Cases for Accounts**

</td></tr><tr><td>

Consumer contributor

</td><td>

**Cases for Consumers**

</td></tr><tr><td>

Service organization contributor

</td><td>

-   **My Cases for Business Locations**: cases created by the contributor user on behalf of their business locations.
-   **All Cases for Business Locations**: all cases created on behalf of the contributor's business locations, independent of who created the case.

</td></tr><tr><td>

Self contributor

</td><td>

**Cases for myself**

</td></tr><tr><td>

Relationship contributor

</td><td>

Displays filters depending on the relationships established for this user. -   **My Cases for Accounts**: cases created by the contributor user on behalf of accounts where the user is an Account Manager.
-   **All Cases for Accounts**: all cases created on behalf of accounts where the user is an Account Manager, independent of who created the case.
-   **My Cases for Consumers**: cases created by the contributor user on behalf of consumers or households where the user is a Relationship Manager.
-   **All Cases for Consumers**: all cases created on behalf of consumers or households where the user is a Relationship Manager, independent of who created the case.

 For more information, see [Service Model Foundation relationships](../reference/csm-data-model-relationships.md).

</td></tr></tbody>
</table>## Access to case tasks

Users with the case task agent role can view and access case tasks in lists, on dashboards, and on landing pages.

Use widgets to display case tasks on dashboards and landing pages.

<table id="table_rdw_j4j_3nb"><thead><tr><th>

Widget

</th><th>

Task information displayed

</th></tr></thead><tbody><tr><td>

My Case Tasks

</td><td>

This widget includes the following information for each case task:-   Task number
-   Status
-   Subject
-   Priority
-   Case number
-   Case short description

</td></tr><tr><td>

My Group's Case Tasks

</td><td>

This widget includes the following information for each case task:-   Task number
-   Status
-   Subject
-   Priority
-   Assigned to
-   Case number
-   Case short description

</td></tr></tbody>
</table>**Note:** If a playbook is available, the system opens the case task within in the playbook. If no playbook is available, the system opens the Case Task form.

Depending on assigned roles, contributor users can see different modules in CSM Agent Workspace and CSM Configurable Workspace.

<table id="table_qxh_f5h_3nb"><thead><tr><th>

Role

</th><th>

Modules

</th></tr></thead><tbody><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

Users with the case task agent role have access to these modules:-   **Case Task**: includes the case tasks that the user has access to.
    -   My Case Tasks
    -   My Open
    -   Unassigned for my groups
    -   My Accessible Tasks
-   **Customers**: Includes read-only access to customer information.
    -   Accounts
    -   Partners
    -   Contacts
    -   Consumers
    -   Households
    -   Household members

</td></tr><tr><td>

Case task viewer\[sn\_customerservice.case\_task\_viewer\]

</td><td>

Users with the case task viewer role have access to All tasks in the **Case Task** module.

</td></tr><tr><td>

Case contributor viewer\[sn\_customerservice.case\_contributor\_viewer\]

</td><td>

Users with the case contributor viewer role have access to My Contributing Tasks in the **Case Task** module.

</td></tr><tr><td>

Case viewer\[sn\_customerservice.case\_viewer\]

</td><td>

Users with the case viewer role can see the cases that they have access to in the **Cases** module.

</td></tr></tbody>
</table>## Case task agent access to customer information

Users with the case task agent role have read-only access to some of the customer information for the parent case.

-   For B2B cases: Account and contact records, including addresses, sold products, and install base.
-   For B2C cases: Consumer and household records, including addresses, sold products, install base, and head of household.
-   For business location cases: Service organization records, including internal contact information.

**Related topics**  


[Contributor user roles](../reference/csm-contributor-user-roles.md)

[Configure Contributor Users](../task/config-contributor-user.md)

