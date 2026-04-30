---
title: Service Model Foundation roles
description: Roles that are included with the plugins that enable the Service Model Foundation feature.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation roles

Roles that are included with the plugins that enable the Service Model Foundation feature.

The following table describes the roles that the administrator can assign to the internal users.

<table id="table_tsh_2rs_jlb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

</td><td>

Create and fulfill cases for the accounts and contacts in the agent's business location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location consumer agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

Create and fulfill cases for the consumers and households in the agent's business location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location manager\[sn\_customerservice.svc\_location\_manager\]

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

Location Project Member

 \[sn\_bus\_loc.location\_project\_stakeholder\]

</td><td>

Views project details and project tasks of their respective business location.

 Marks customer visible project tasks as complete.

</td><td>

None

</td></tr><tr><td>

Location Project Manager Contributor

 \[sn\_bus\_loc.location\_manager\_project\_stakeholder\]

</td><td>

Views project details and project tasks of their respective business location and child business locations.

 Marks customer visible project tasks as complete.

</td><td>

None

</td></tr><tr><td>

EBL Viewer\[sn\_bus\_loc.ebl\_viewer\]

</td><td>

Views all external business location details and location staff

</td><td>

None

</td></tr><tr><td>

IBL viewer\[sn\_bus\_loc.ibl\_viewer\]

</td><td>

Views all internal business location details and location staff.

</td><td>

None

</td></tr><tr><td>

Service Organization Project Manager\[sn\_service\_org.project\_manager\]

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

</td></tr></tbody>
</table>