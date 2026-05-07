---
title: Service Model Foundation roles
description: Roles that are included with the plugins that enable the Service Model Foundation feature.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation roles

Roles that are included with the plugins that enable the Service Model Foundation feature.

The following table describes the roles that the administrator can assign to the internal users.

<table id="table_tsh_2rs_jlb"><thead><tr><th>

Role

</th><th>

Responsibility

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

</td><td>

Location agent

</td><td>

Create and fulfill cases for the accounts and contacts in the agent's business location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location consumer agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

Location consumer agent

</td><td>

Create and fulfill cases for the consumers and households in the agent's business location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location manager\[sn\_customerservice.svc\_location\_manager\]

</td><td>

Location Manager Fulfiller

</td><td>

Create and update cases for accounts, contacts, consumers, and households that work with the business locations within their location hierarchy.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_customerservice.svc\_location\_agent
-   sn\_customerservice.svc\_location\_consumer\_agent
-   email\_client\_quick\_message\_author
-   sn\_templated\_snip.template\_snippet\_writer
-   sn\_shn.admin
-   approver\_user
-   sn\_publication.approver

</td></tr><tr><td>

Location manager contributor\[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

Location Manager Contributor

</td><td>

Manage service organizations and create cases for accounts, households, or consumers at the service organization or any of its child service organizations.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_customerservice.svc\_location\_manager\_core
-   sn\_customerservice.consumer\_contributor
-   sn\_customerservice.account\_contributor

</td></tr><tr><td>

Location Project Member

 \[sn\_bus\_loc.location\_project\_stakeholder\]

</td><td>

None

</td><td>

Views project details and project tasks of their respective business location.

 Marks customer visible project tasks as complete.

</td><td>

None

</td></tr><tr><td>

Location Project Manager Contributor

 \[sn\_bus\_loc.location\_manager\_project\_stakeholder\]

</td><td>

None

</td><td>

Views project details and project tasks of their respective business location and child business locations.

 Marks customer visible project tasks as complete.

</td><td>

None

</td></tr><tr><td>

EBL Viewer\[sn\_bus\_loc.ebl\_viewer\]

</td><td>

None

</td><td>

Views all external business location details and location staff

</td><td>

None

</td></tr><tr><td>

IBL viewer\[sn\_bus\_loc.ibl\_viewer\]

</td><td>

None

</td><td>

Views all internal business location details and location staff.

</td><td>

None

</td></tr><tr><td>

Service Organization Project Manager\[sn\_service\_org.project\_manager\]

</td><td>

None

</td><td>

This role can perform the following actions:-   Project initiation: Creates and launches projects

**Note:** Service Organization project manager and customer project manager can access all project modules.

-   Project planning: Develops project plans, such as, task assignments and resource allocation.

**Note:** On task assignment, an automated mail is generated. Update "Send Email to Contact when Customer Project Task is assigned" flow to disable or enable notifications.

-   Task management: Monitors and manages task dependencies and execution.
-   Coordination: Views and collaborates with location staff, assigning, and tracking tasks of their respective location.

</td><td>

-   sn\_bus\_loc.ibl\_viewer
-   sn\_bus\_loc.ebl\_viewer

</td></tr><tr><td>

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

None

</td><td>

This role restricts an agent's access to only those cases for the accounts, contacts, consumers, and households that they have a relationship with. This role includes the following relationships that are provided with the Service Model Foundation plugins:

-   Account Manager: Creates a relationship between an internal user and an account.
-   Relationship Manager: Creates a relationship between an internal user and a consumer or a household.

</td><td>

-   agent\_workspace\_user
-   snc\_internal
-   sn\_shn.editor
-   email\_composer
-   sn\_fsm\_servicedesk\_agent
-   sn\_customerservice.csm\_workspace\_user
-   sn\_templated\_snip.template\_snippet\_reader

</td></tr><tr><td>

Service Management agent \[sn\_esm\_location\_agent\]

</td><td>

None

</td><td>

A service management agent role for a business location

</td><td>

-   sn\_lookup\_verify\_user
-   assignment\_workbench
-   knowledge
-   agent\_workspace\_user
-   chat\_admin
-   cmdb\_read
-   agent\_schedule\_user
-   interaction\_agent
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_shn.editor
-   template\_editor
-   email\_composer
-   template\_editor\_global

</td></tr><tr><td>

Location Support agent\[sn\_bus\_loc.svc\_location\_support\_agent\]

</td><td>

Location Support Agent

</td><td>

This role resolves the cases originated from other business organizations, ensuring access to required information and other details, and facilitating efficient coordination with store personnel

**Note:** This role only applies to the internal business location.

</td><td>

sn\_esm\_location\_agent

</td></tr><tr><td>

Service organization contributor\[sn\_customerservice.service\_organization\_contributor\]

</td><td>

Location Contributor

</td><td>

This user:-   works with accounts and contacts, consumers, and households
-   uses the Customer or Consumer Service Portal to assist customers
-   search knowledge articles and catalog items.
-   create cases on behalf of their business location, including cases for catalog items \(requests\), and follow up on those cases.
-   create cases from communication channels available to customers including phone, web, chat, Virtual Agent, and messaging.
-   view and follow up on other cases created for the user's business location.

If also an internal user on a case, this user can:

-   add additional comments and attachments
-   accept or reject a solution
-   close a case
-   receive notifications of case updates
-   read work notes

</td><td>

-   sn\_customerservice.case\_contributor\_creator
-   sn\_service\_org.service\_criteria\_read
-   sn\_service\_org.customer\_criteria\_read

</td></tr></tbody>
</table>## Granular roles

<table id="table_s4c_rsm_33c"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Inherited by

</th><th>

Inherits

</th></tr></thead><tbody><tr><td>

sn\_service\_org.service\_org\_delete

</td><td>

Provides delete access to service organization, business location, internal business location, and external business location

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_external\_staff\_create

</td><td>

Provides create access to service organization external staff

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_external\_staff\_read

</td><td>

Provides read access to service organization external staff

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_external\_staff\_write

</td><td>

Provides write access to service organization external staff

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_external\_staff\_delete

</td><td>

Provides delete access to service organization external staff

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_assignment\_group\_create

</td><td>

Provides create access to service organization assignment groups

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_assignment\_group\_read

</td><td>

Provides read access to service organization assignment groups

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_assignment\_group\_write

</td><td>

Provides write access to service organization assignment groups

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_assignment\_group\_delete

</td><td>

Provides delete access to service organization assignment groups

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_criteria\_create

</td><td>

Provides create access to organization criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_criteria\_read

</td><td>

Provides read access to organization criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_criteria\_write

</td><td>

Provides write access to organization criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_criteria\_delete

</td><td>

Provides delete access to organization criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_customer\_criteria\_create

</td><td>

Provides create access to organization customer criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_customer\_criteria\_read

</td><td>

Provides read access to organization customer criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_customer\_criteria\_write

</td><td>

Provides write access to organization customer criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_customer\_criteria\_delete

</td><td>

Provides delete access to organization customer criteria

</td><td>

sn\_service\_org.service\_org\_admin

</td><td>

No

</td></tr><tr><td>

sn\_service\_org.service\_org\_offering\_service\_read

</td><td>

Provides all CRUD access to outsourced customer service flow

</td><td>

No

</td><td>

-   sn\_service\_org.service\_external\_staff.create
-   sn\_service\_org.service\_external\_staff.read
-   sn\_service\_org.service\_external\_staff.write
-   sn\_service\_org.service\_external\_staff.delete
-   sn\_contractor.outsourced\_service\_provider\_create
-   sn\_contractor.outsourced\_service\_provider\_read
-   sn\_contractor.outsourced\_service\_provider\_write
-   sn\_contractor.outsourced\_service\_provider\_delete
-   sn\_contractor.outsourced\_service\_provider\_criteria\_create
-   sn\_contractor.outsourced\_service\_provider\_criteria\_read
-   sn\_contractor.outsourced\_service\_provider\_criteria\_write
-   sn\_contractor.outsourced\_service\_provider\_criteria\_delete
-   sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_create
-   sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_read
-   sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_write
-   sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_delete

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_create

</td><td>

Provides create access to outsourced service providers

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_read

</td><td>

Provides read access to outsourced service providers

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_write

</td><td>

Provides update access to outsourced service providers

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_delete

</td><td>

Provides delete access to outsourced service providers

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_criteria\_create

</td><td>

Provides create access to outsourcing criteria

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_criteria\_read

</td><td>

Provides read access to outsourcing criteria

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_criteria\_write

</td><td>

Provides update access to outsourcing criteria

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_contractor.outsourced\_service\_provider\_criteria\_delete

</td><td>

Provides delete access to outsourcing criteria

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_csm\_ocs.csm\_ocs\_case\_transfer\_request\_create

</td><td>

Provides create access to outsourced case transfer requests

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_csm\_ocs.csm\_ocs\_case\_transfer\_request\_read

</td><td>

Provides read access to outsourced case transfer requests

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_csm\_ocs.csm\_ocs\_case\_transfer\_request\_write

</td><td>

Provides write access to outsourced case transfer requests

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr><tr><td>

sn\_csm\_ocs.csm\_ocs\_case\_transfer\_request\_delete

</td><td>

Provides delete access to outsourced case transfer requests

</td><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

No

</td></tr></tbody>
</table>**Related topics**  


[Service Model Foundation Granular admin roles](granular-admin-roles.md)

