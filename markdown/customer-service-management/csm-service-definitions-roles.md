---
title: Service definition roles
description: Service definition roles included with the Customer Service Case Types plugin enable users to view, create, and update service definitions, service definition categories, and service definition category relationships. Agents and end users can use these definitions and categories to view and create cases based on the selected service.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Service definition roles

Service definition roles included with the Customer Service Case Types plugin enable users to view, create, and update service definitions, service definition categories, and service definition category relationships. Agents and end users can use these definitions and categories to view and create cases based on the selected service.

## Service definition roles

The following service definition roles are installed with the Customer Service Case Types \(com.snc.csm\_case\_types\) plugin.

<table id="table_nyy_5qq_tzb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service definition admin\[sn\_csm\_case\_types.service\_definition\_admin\]

</td><td>

Administrator role for the [Customer Service case types](customer-service-case-types.md) tables. Users with this role can view, create, update, and delete service definitions, service definition categories, and service definition category relationships.

</td><td>

-   sn\_csm\_case\_types.service\_definition\_manager
-   sn\_service\_org.service\_criteria\_delete

</td></tr><tr><td>

Service definition manager\[sn\_csm\_case\_types.service\_definition\_manager\]

</td><td>

Manager role for the [Customer Service case types](customer-service-case-types.md) tables. Users with this role can view, create, and update service definitions, service definition categories, and service definition category relationships.

</td><td>

-   sn\_csm\_case\_types.service\_definition\_report\_view
-   sn\_csm\_case\_types.service\_definition\_all\_table\_viewerr
-   sn\_service\_org.service\_criteria\_write
-   sn\_service\_org.service\_criteria\_create
-   sn\_service\_org.service\_criteria\_read

</td></tr><tr><td>

Service definition viewer\[sn\_csm\_case\_types.service\_definition\_viewer\]

</td><td>

Users with this role can view service definitions, service definition categories, and service definition category relationships.

</td><td>

sn\_service\_org.service\_criteria\_read

</td></tr><tr><td>

Service definition report viewer\[sn\_csm\_case\_types.service\_definition\_report\_view\]

</td><td>

Provides report view access to service definition related tables.

</td><td>

None

</td></tr><tr><td>

Service definition all table viewer\[sn\_csm\_case\_types.service\_definition\_all\_table\_viewer\]

</td><td>

Provides view access to the service definition tables. Users with this role can view service definitions, service definition categories, and service definition category relationships.

</td><td>

None

</td></tr></tbody>
</table>## How users can use service definitions

In CSM Configurable Workspace, users with the admin role or one of the following agent roles can access the **Service** field for cases and case tasks.

-   Customer service agent \(sn\_customerservice\_agent\)
-   Consumer service agent \(sn\_customerservice.consumer\_agent\)
-   Customer service manager \(sn\_customerservice\_manager\)

The admin and agent roles can do the following:

-   See the **Service** column on Case Task lists. For example, My Case Task and My Contributing Tasks.
-   See the **Service** field on the Case Task form.
-   Select a service in the **Service** field and save the Case Task form.
-   Create a case task and see the **Service** field on the Case Task form.

In the Core UI, users with the admin role or one of the agent roles listed above can do the following:

-   See the **Service** column on Task list.
-   See the **Service** field on the Task form.
-   Select a service in the **Service** field and save the Case Task form.

From the Customer and Consumer Service Portals, users with the admin role or an end user role can see the **Service** field on case tasks that the user has access to. See the following table for the end user roles that can see this field.

<table id="table_wxl_2sj_rxb"><thead><tr><th>

Users and Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**B2B user roles**

</td></tr><tr><td>

Customer service agent\[sn\_customerservice.customer\]

</td><td>

An agent who assists customers and partners with questions, issues, and problems.

</td></tr><tr><td>

Customer administrator\[sn\_customerservice.customer\_admin\]

</td><td>

An administrator role for a customer account. This user has access to all of the data within the account.

</td></tr><tr><td>

Customer case manager\[sn\_customerservice.customer\_case\_manager\]

</td><td>

A customer role for managing the cases in an account and any related child accounts.

</td></tr><tr><td>

Partner\[sn\_customerservice.partner\]

</td><td>

A partner who is serving customer accounts.

</td></tr><tr><td>

Partner administrator\[sn\_customerservice.partner\_admin\]

</td><td>

An administrator role for a partner account.

</td></tr><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

A role that provides access to case tasks and related case information.

</td></tr><tr><td>

Case task viewer\[sn\_customerservice.case\_task\_viewer\]

</td><td>

A role that provides read-only access to all case task records.

</td></tr><tr><td>

Customer contacts with configured contact relationships

</td><td>

For more information, see [Contact Relationships](c_ContactRelationships.md).

</td></tr><tr><td class="sub-head" colspan="2">

**B2C user roles**

</td></tr><tr><td>

Consumer service agent\[sn\_customerservice.consumer\_agent\]

</td><td>

An agent who assists consumers with questions, issues, and problems.

</td></tr><tr><td>

Consumers with configured consumer relationships

</td><td>

Use relationships to provide internal and external users with additional access to customer data. For more information, see [Create relationships](../task/configure-data-model-relationships.md).

</td></tr><tr><td>

Consumers who are designated as head of household

</td><td>

A household is made up of a group of consumers who live at a common address and share products and services. A household can have a designated head of household and multiple current members. For more information, see [Create or update a household](../task/create-consumer-household.md).

</td></tr><tr><td class="sub-head" colspan="2">

**Contributor roles**

</td></tr><tr><td>

Account contributor\[sn\_customerservice.account\_contributor\]

</td><td>

This role enables users to create cases and case tasks for any account.

</td></tr><tr><td>

Consumer contributor\[sn\_customerservice.consumer\_contributor\]

</td><td>

This role enables users to create cases and case tasks for any consumer.

</td></tr><tr><td>

Self contributor\[sn\_customerservice.self\_contributor\]

</td><td>

This role enables users with snc\_internal role to create cases and case tasks for themselves.

</td></tr><tr><td>

Location manager contributor\[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

A location manager contributor is employed at the business location and manages a business location in the location hierarchy along with all its child business locations.

</td></tr><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

</td><td>

-   View all CSM entities.
-   Create cases for any account, household, consumer, or service organization.
-   Fulfill cases for any account, household, consumer, or service organization created at the agent’s location.

</td></tr><tr><td>

Location consumer agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

-   View all CSM entities.
-   Create cases for any household or consumer.
-   Fulfill cases for any household or consumer created at the agent's location.
-   Assign related staff to any account, household, or consumer.

</td></tr><tr><td>

Relationship contributor\[sn\_customerservice.relationship\_contributor\]

</td><td>

This role enables users to create cases for customers with which they have an established relationship.

</td></tr><tr><td>

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

Manage cases for the accounts, contacts, consumers, and households that the agent has relationships with. This includes the following relationships that are provided with the Service Model Foundation plugins:-   Account Manager: Creates a relationship between an internal user and an account.
-   Relationship Manager: Creates a relationship between an internal user and a consumer or a household.

</td></tr><tr><td>

Location relationship manager\[sn\_bus\_loc.location\_relationship\_manager\]

</td><td>

A location relationship manager is employed by the parent business and acts as a point of contact for one or more external business locations.

</td></tr><tr><td>

Service organization contributor\[sn\_customerservice.service\_organization\_contributor\]

</td><td>

This role enables users to create cases for their service organization \(business location\)

</td></tr><tr><td>

Case Authorized Contributor\[sn\_customerservice.case\_authorized\_contributor\]

</td><td>

This role provides access to add additional comments and attachments, accept or reject a solution, receive notifications on case updates, close a case, and update case tasks.

</td></tr><tr><td>

Outsourced external agent\[sn\_csm\_ocs.ext\_agent\]

</td><td>

An Outsourced Service Provider \(OSP\) role. Users with this role can fulfill the cases and case tasks belonging to the service provider organization they belong to.

</td></tr></tbody>
</table>For more information about these roles, see the following topics:

-   [Roles installed with Customer Service Management](../reference/r_RolesInstalledWithCustomerService.md)
-   [Contributor user roles](../reference/csm-contributor-user-roles.md)
-   Service Model Foundation - [Assign roles](../task/configure-data-model-roles.md)
-   [Roles installed with customer access management](../reference/r_rolesinstalledwithcustaccessmgmt.md)
-   [Roles for Outsourced Customer Service](../reference/roles-ocs.md)

**Related topics**  


[Configuring service definitions](csm-service-definitions-configure.md)

[Customer service case types](customer-service-case-types.md)

[Manage customer service case types](manage-csm-case-types.md)

[Create a customer service case of a specific type](../task/create-case-of-specific-case-type.md)

