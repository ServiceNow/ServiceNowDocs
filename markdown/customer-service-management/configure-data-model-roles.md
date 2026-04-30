---
title: Assign roles
description: Assign roles to internal and external users to facilitate proper access to service organizations, business locations, and households. By assigning required roles, you can enable each user to have the necessary permissions to perform their tasks effectively.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Assign roles

Assign roles to internal and external users to facilitate proper access to service organizations, business locations, and households. By assigning required roles, you can enable each user to have the necessary permissions to perform their tasks effectively.

## Before you begin

Role required: admin

## About this task

The Service Model Foundation plugins add the following roles to Customer Service Management.

<table id="table_tls_5tk_2mb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Location manager contributor\[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

A location manager contributor is employed at the business location and manages a business location in the location hierarchy along with all its child business locations.

 A location manager contributor performs the following tasks:

 -   Manage service organization.
-   Manages staff at the business locations.
-   Track products and services at the business locations.
-   Report cases for any account, household, or consumer created at the parent or any child business locations.

</td><td>

-   sn\_customerservice.consumer\_contributor
-   sn\_customerservice.svc\_location\_manager\_core
-   sn\_customerservice.service\_organization\_contributor
-   sn\_customerservice.account\_contributor

</td></tr><tr><td>

Location relationship manager\[sn\_bus\_loc.location\_relationship\_manager\]

 **Note:** This role only applies to the external business locations.

</td><td>

A location relationship manager is employed by the parent business and acts as a point of contact for one or more external business locations.

 A location relationship manager performs the following tasks:

 -   Manage and monitor all activities related to products and services at an external business location.
-   Monitor the performance of external business locations.
-   Respond to queries on case status from external business location stakeholders.

</td><td>

sn\_customerservice.svc\_location\_manager\_contributor

</td></tr><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

 **Note:** This role only applies to the internal business location.

</td><td>

A location agent performs the following tasks:

-   View all customer service management \(CSM\) entities.
-   Create cases for any account, household, consumer, or service organization.
-   Fulfill cases for any account, household, consumer, or service organization created at the agent’s location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location consumer agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

 **Note:** This role only applies to the internal business location.

</td><td>

A location consumer agent performs the following tasks:

-   View all CSM entities.
-   Create cases for any account, household, consumer, or service organization.
-   Fulfill cases for any account, household, consumer, or service organization created at the service organization or any child service organization.
-   Assign related staff to any account, household, or consumer.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location manager\[sn\_customerservice.svc\_location\_manager\]

 **Note:** This role only applies to the internal business locations.

</td><td>

A location manager performs the following tasks:

-   View all CSM entities for a related account, household, consumer, or service organization.
-   Create, update, and close cases for any related account, household, consumer, or service organization created at the consumer’s location.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_customerservice.svc\_location\_agent
-   email\_client\_quick\_message\_author
-   sn\_templated\_snip.template\_snippet\_writer
-   sn\_customerservice.svc\_location\_manager\_core
-   sn\_shn.admin
-   approver\_user
-   sn\_customerservice.svc\_location\_consumer\_agent

</td></tr><tr><td>

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

Manage cases for the accounts, contacts, consumers, and households that the agent has relationships with. It includes the following relationships that are provided with the Service Model Foundation plugins:

-   Account Manager: Creates a relationship between an internal user and an account.
-   Relationship Manager: Creates a relationship between an internal user and a consumer or a household.

</td><td>

-   agent\_workspace\_user
-   sn\_fsm\_servicedesk\_agent
-   snc\_internal
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_customerservice.csm\_workspace\_user
-   sn\_shn.editor
-   email\_composer

</td></tr><tr><td>

Service Management location agent\[sn\_esm\_location\_agent\]

</td><td>

A service management location agent is an agent for a business location.

</td><td>

-   sn\_lookup\_verify\_user
-   assignment\_workbench
-   knowledge
-   agent\_workspace\_user
-   actsub\_user
-   template\_editor
-   chat\_admin
-   cmdb\_read
-   agent\_schedule\_user
-   interaction\_agent
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_customerservice.csm\_workspace\_user
-   sn\_shn.editor
-   email\_composer
-   template\_editor\_global

</td></tr><tr><td>

Location support agent\[sn\_bus\_loc.svc\_location\_support\_agent\]

</td><td>

A location support agent is a service organization member who acts as a fulfiller and can perform the following tasks:-   View all CSM entities.
-   Create and resolve cases.
-   Access the CSM Configurable Workspace.
-   Use business location 360 to view details of internal and external business locations that they support, sold products, location members, install base items, and available services.

**Note:** The role of location support agent is not supported for external business locations since case fulfillment isn't enabled for these locations.

</td><td>

-   sn\_esm\_location\_agent
-   sn\_csm\_case\_types.service\_definition\_viewer

</td></tr></tbody>
</table>**Note:** If contributor users, like relationship contributors, account contributors, or consumer contributors associated with business locations, have a location contributor \(sn\_customerservice.service\_organization\_contributor\) role, they can access the business locations.

## Procedure

-   You can assign roles to users using the Service Model Foundation guided setup.

-   You can also assign roles to users using the ServiceNow AI Platform user administration feature: [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


