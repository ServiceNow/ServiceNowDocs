---
title: Enterprise Architecture Workspace access roles
description: The following roles help you to configure and use the Enterprise Architecture Workspace application. After access has been granted to a role, all the groups or users assigned to the role are granted access. Roles can contain other roles, and any access granted to a role is granted to any other role that includes it.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-17"
reading_time_minutes: 14
keywords: [access roles, permissions, role capabilities, enterprise architect, application portfolio, business architecture, technology portfolio, data certification, modeling, AI systems]
breadcrumb: [Install Enterprise Architecture Workspace, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Enterprise Architecture Workspace access roles

The following roles help you to configure and use the Enterprise Architecture Workspace application. After access has been granted to a role, all the groups or users assigned to the role are granted access. Roles can contain other roles, and any access granted to a role is granted to any other role that includes it.

## Enterprise Architecture Workspace roles

The following roles are available in Enterprise Architecture Workspace. After access is granted to a role, all users and groups assigned to that role inherit the permissions. Roles can contain other roles, and any access granted to a role is also granted to any role that includes it.

|Role|Description|Typical persona|
|----|-----------|---------------|
|sn\_apm.apm\_admin|Full administrative access to configure and manage Enterprise Architecture Workspace settings, including Setup page configuration for all functional areas. Includes all permissions of sn\_apm.apm\_analyst.|EA administrator, IT architect lead|
|sn\_apm.apm\_analyst|Create and manage key portfolio records such as business applications and digital integrations. Approve or reject requests when assigned to the Enterprise Architect group. Includes all permissions of sn\_apm.apm\_user.|Enterprise architect, solution architect|
|sn\_apm.apm\_user|Create and update portfolio data across business architecture, information portfolio, technology portfolio, modeling, and data certification. Includes all permissions of sn\_apm.apm\_read.|Application owner, business analyst, portfolio manager|
|sn\_apm.apm\_read|Read-only access to all pages and records in Enterprise Architecture Workspace. Cannot create or update data. For more information, see [Business stakeholder role for Enterprise Architecture Workspace](eaw-business-stakeholder-role.md).|Business stakeholder, executive, auditor|

Users with Enterprise Architecture Workspace roles and certain platform roles, such as ITIL and other CMDB related roles, may be able to create or edit Business Application records by default.

**Note:** The global admin role continues to function through role inheritance. However, Enterprise Architecture now uses feature-specific granular admin roles. Use sn\_apm.apm\_admin instead of admin for application-level administration wherever possible. For more information, see [Granular admin role changes in Enterprise Architecture](eaw-gran-admin-role-changes.md).

## Enterprise Architect group

The Enterprise Architect group is a platform user group that acts as a governance layer on top of the standard role hierarchy. It is configured intentionally to separate approval authority from general role access: users with the sn\_apm.apm\_analyst role can perform approvals and governance actions only when they are also members of this group. Assigning the role alone is not sufficient for these actions.

To add or modify members of the Enterprise Architect group, navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Services Approval Group** &gt; **Enterprise Architect Group**.

The following table lists the capabilities that require membership in the Enterprise Architect group.

<table id="table_ea_group"><thead><tr><th>

Functional area

</th><th>

Role also required

</th><th>

Capabilities unlocked by group membership

</th></tr></thead><tbody><tr><td>

Technology Reference Model \(TRM\)

</td><td>

sn\_apm.apm\_analyst

</td><td>

-   Approve or reject TRM product requests
-   Approve or reject TRM product lifecycle requests
-   Create TRM product lifecycles
-   View and update pending TRM requests

</td></tr><tr><td>

Enterprise modeling and visualization

</td><td>

sn\_apm.apm\_analyst

</td><td>

-   Approve or reject modeling diagram requests
-   View shape library configurations, entity configurations, and modeling configuration and relationship definitions

</td></tr></tbody>
</table>## Installation and plugin activation

Plugin activation requires the global admin role.

<table id="table_section_install"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Activate the EA Workspace plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate the Technology Portfolio Management \(TPM\) plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate the Technology Reference Model \(TRM\) plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate the Read only roles for Enterprise Architecture plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr></tbody>
</table>## Setup page

The Setup page provides configuration options for all functional areas in the workspace.

<table id="table_section_setup"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Configure application categories, category groups, and families

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure application and capability indicators

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure scoring profiles and attach profile indicators

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure TRM phases and TRM categories

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure information data domains

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure architectural artifact categories

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure demand actions

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure modeling settings, including shape libraries, entities, relationships, and diagram actions

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure total cost of ownership \(TCO\) sources, source cost types, and cost types; set TCO dashboard properties

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure Publishing Center for TRM catalog publishing; modify TRM catalog publishing configurations; associate service portals with a TRM catalog knowledge base

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Add and edit certification policies from the Setup page \(legacy CMDB-based policies\)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires certification\_admin

</td></tr></tbody>
</table>## Business architecture

Business architecture covers business capabilities, business units, departments, goals, value streams, value stream stages, business processes, and demands in the Portfolio List view.

<table id="table_section_biz_arch"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Add and edit business capabilities and sub-capabilities

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit business units

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit departments; add users to departments

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit goals; add quantitative and qualitative targets; create sub-goals

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit value streams; add application models to value streams

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit value stream stages; associate business processes with value stream stages; add or remove business capabilities from value stream stages

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit business processes

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit demands

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create demands from the Business Portfolio view and Application Rationalization views

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Export business portfolio data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View all business architecture records

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Application portfolio

The application portfolio covers business applications, application services, digital integrations, digital interfaces, and product capabilities.

<table id="table_section_app_portfolio"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Add new business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit digital integrations; associate artifacts and information objects with digital integrations

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit digital interfaces; manage Agile Development components, information objects, and credentials; relate a digital interface to an API

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Update business application details

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Associate and unassign business capabilities, product capabilities, architectural artifacts, information objects, and TRM products with business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create diagrams and unified maps from a business application

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View the business application roadmap

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit application services

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit product capabilities; view all product capabilities

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View and manage AI systems and AI portfolio items associated with business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Run the job to generate model IDs for business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View all business applications, application services, digital integrations, digital interfaces, and associated records

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Information portfolio

The information portfolio covers data domains, information objects, architectural artifacts, and architectural decision records \(ADRs\).

<table id="table_section_info_portfolio"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Add and edit data domains and information objects

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create and edit architectural artifacts; add versions, related entities, and associated records

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Share architectural artifacts with users and groups; manage access permissions for architectural artifacts

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Request approval for an artifact version; download and delete architectural artifact versions

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create and edit architectural decision records \(ADRs\); add pages, subpages, and versions to ADRs

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Tag users and records in an ADR document; request approval for an ADR

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Associate architectural artifacts with business applications, capabilities, business processes, digital integrations, and TRM products

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View all data domains, information objects, architectural artifacts, artifact versions, and ADRs

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Technology Portfolio Management \(TPM\)

Technology Portfolio Management tracks software and hardware lifecycle data for business applications and application services.

<table id="table_section_tpm"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Activate the TPM plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Update the system property to gather software from CMDB

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Update TPM lifecycle data for a business application or application service

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View technology lifecycle data and technology risk information

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View technology portfolio audit risk details and update verification status

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Run the job to populate TPM lifecycle data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Run the scheduled job to update TPM data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Run the scheduled job to generate TPM risk; restart the TPM scheduled job

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View TPM logs; run the job to populate TPM lifecycle identifiers

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View technology portfolio data, lifecycle timelines, and risk information

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Technology Reference Model \(TRM\)

The Technology Reference Model provides a structured catalog of approved technologies and their lifecycle phases.

<table id="table_section_trm"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Activate the TRM plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Approve or reject TRM product requests

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

Must be in the Enterprise Architect group

</td></tr><tr><td>

Approve or reject TRM product lifecycle requests; create TRM product lifecycles

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

Must be in the Enterprise Architect group

</td></tr><tr><td>

View and update pending TRM requests

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

Must be in the Enterprise Architect group

</td></tr><tr><td>

View all TRM products, grouped by category or individually

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View all TRM phases and categories

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Request a new TRM product; request a TRM product lifecycle change

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create TRM product lifecycle requests

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Associate architectural artifacts with TRM products

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View, create, add, and remove business capabilities and business applications associated with TRM products

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View TRM technical debt; run the job to generate TRM technical debts

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Export TRM product catalog data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View TRM products, categories, phases, technical debt, and lifecycle timelines

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Enterprise modeling and visualization

Enterprise modeling and visualization lets users create, manage, and publish architecture diagrams.

<table id="table_section_modeling"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Approve or reject modeling diagram requests

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

Must be in the Enterprise Architect group

</td></tr><tr><td>

View shape library configurations, entity configurations, modeling configuration, and relationship definitions

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

Must be in the Enterprise Architect group

</td></tr><tr><td>

Create empty diagrams and synchronize them with the ServiceNow database

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create business capability maps \(BC maps\), business application maps \(BA maps\), and business process maps \(BP maps\)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create ArchiMate diagrams, AWS architecture diagrams, and CSDM diagrams

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add, remove, group, ungroup, expand, collapse, and delete shapes

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add related records to shapes; add labels to connector lines

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Reorder shapes in a category; show or hide the Shapes panel; toggle between grid and list view; filter shapes

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Save a diagram as new; duplicate a diagram

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Submit a diagram for approval; synchronize a diagram and individual shapes

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Share a diagram; download a diagram; add or edit diagram version details; delete a diagram

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create and manage custom shape libraries, custom shape elements, and custom shape actions; store images in the database for custom shapes

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Modify BPMN diagrams

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View diagrams and diagram details

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Application rationalization

Application rationalization helps users assess and manage business applications through bubble chart and list views.

<table id="table_section_app_rat"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Analyze business applications in the bubble chart view by capability

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create demands from the bubble chart view and list view

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Set the planned disposition of a business application

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add and edit business application lifecycle data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Edit business application details from the bubble chart and list views

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Edit demands and projects associated with a business application

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Update the system property to change the number of bubbles displayed

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Apply filters on the application rationalization view

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Export application rationalization list data

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View application rationalization data in bubble chart and list views

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Data certification

Data certification provides a governance mechanism to promote that architecture data is accurate and complete.

<table id="table_section_data_cert"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Create data certification policies using the certification policy wizard

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires system admin, CMDB admin, and sn\_apm.apm\_analyst

</td></tr><tr><td>

Publish draft certification policies

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Run data certification policies

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate and deactivate certification policies; delete certification policies

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Track certification progress across policies

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Review and certify data certification tasks assigned to them

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

User must be assigned a certification task

</td></tr><tr><td>

Fail records that do not meet certification standards

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

User must be assigned a certification task

</td></tr><tr><td>

Reassign certification tasks to other users or groups; request reassignment

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

User must be assigned a certification task

</td></tr><tr><td>

Submit completed certification reviews

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

User must be assigned a certification task

</td></tr><tr><td>

View certification policies and certification status

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Dashboards

Dashboards provide visibility into application health, assessment scores, and portfolio performance.

<table id="table_section_dashboards"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

View and monitor the Applications Assessment dashboard

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View and monitor the Application 360 dashboard

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View the workspace home dashboard and portfolio overview and health section

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Apply filters on the portfolio overview and health view

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View dashboards

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Total Cost of Ownership \(TCO\)

Total Cost of Ownership tracks and manages direct and indirect costs associated with business applications.

<table id="table_section_tco"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Activate the App TCO plugin

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Create TCO sources, TCO source cost types, and TCO cost types

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Set properties for TCO dashboards

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View all TCO records for business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

create TCO records

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View TCO records

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Publishing Center

The Publishing Center lets administrators publish TRM catalog data to a knowledge base for consumption through a service portal.

<table id="table_section_publishing"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Create and modify TRM catalog publishing configurations

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Configure TRM data to publish; manage article configurations

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Associate portals with a TRM catalog knowledge base

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Enable automatic synchronization of published catalogs

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Publish and republish TRM catalogs to the knowledge base

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Retire and archive published TRM catalogs; view publishing run logs

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_apm.apm\_admin and knowledge\_admin

</td></tr><tr><td>

Access published TRM catalog content through the service portal

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## Architecture Analyzer

The Architecture Analyzer lets users explore and visualize relationships between architectural entities on an interactive canvas.

<table id="table_section_arch_analyzer"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

create explorations on the Architecture Analyzer canvas

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add entities to the canvas by selecting entity type and specific record

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add upstream and downstream related entities to a selected entity on the canvas

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Show or hide the left navigation pane and the Add to canvas panel

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Clear all entities from the canvas

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Download an exploration canvas as an image

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Rename an exploration; delete an exploration

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View existing explorations

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## AI systems — AI Control Tower integration

The AI systems integration surfaces AI governance data from AI Control Tower directly on business application records. Viewing full AI system records in AI Control Tower requires roles from the AI Control Tower application in addition to EA Workspace roles.

<table id="table_section_ai_systems"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

View the AI systems tab on a business application record

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View AI system details including lifecycle phase, state, lifecycle status, and risk classification

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Add an existing AI Control Tower AI system to a business application

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Remove an AI system association from a business application

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Open and view the full AI system record in the AI Control Tower workspace

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_ai\_governance.ai\_governance\_workspace\_user \(AI Control Tower role\)

</td></tr><tr><td>

View full AI system governance details in AI Control Tower, including related models, datasets, prompts, approval history, and lifecycle tasks

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_aig.ai\_steward or sn\_aig.ai\_asset\_owner \(AI Control Tower roles\)

</td></tr><tr><td>

Manage AI system associations with business applications from the AI Control Tower side

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Requires sn\_aig.ai\_steward or sn\_aig.ai\_asset\_owner \(AI Control Tower roles\)

</td></tr><tr><td>

View the AI systems tab on a business application record

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>## My Entities

My Entities provides a personalized view of the records you own or manage, across all portfolio types.

<table id="table_section_my_entities"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

sn\_apm.apm\_admin

</th><th align="center">

sn\_apm.apm\_analyst

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

View and manage your business capabilities, business processes, and business applications

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View and manage your application services, information objects, and architectural artifacts

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View and manage your TRM products, digital integrations, and digital interfaces

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View your assigned entities

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../image/eaw-image/icon-check-mark-green.png)

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Install Enterprise Architecture Workspace](../../task/install-ea-workspace.md)

**Related topics**  


[Business stakeholder role for Enterprise Architecture Workspace](eaw-business-stakeholder-role.md)

[Granular admin role changes in Enterprise Architecture](eaw-gran-admin-role-changes.md)

