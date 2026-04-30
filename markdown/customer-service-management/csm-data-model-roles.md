---
title: Service Model Foundation roles
description: Roles that are included with the plugins that enable the Service Model Foundation feature.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation roles

Roles that are included with the plugins that enable the Service Model Foundation feature.

The following table describes the roles that the system administrator can assign to the internal users.

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

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

This role restricts an agent's access to only those cases for the accounts, contacts, consumers, and households that they have a relationship with. This includes the following relationships that are provided with the Service Model Foundation plugins:

-   Account Manager: creates a relationship between an internal user and an account.
-   Relationship Manager: creates a relationship between an internal user and a consumer or a household.

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