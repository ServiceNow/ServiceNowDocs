---
title: Roles installed with Care Team Work Management
description: The following roles are installed with Care Team Work Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Roles installed with Care Team Work Management

The following roles are installed with Care Team Work Management.

<table id="table_sqb_gvl_1gc"><tbody><tr><td>

Role

</td><td>

Persona

</td><td>

Roles structure

</td><td>

Description

</td></tr><tr><td>

**sn\_cto.loc\_contributor**

</td><td>

Care Team Location Contributor

</td><td>

Contains: sn\_task\_plan.viewer

</td><td>

Can request care team operation cases and read results of smart assessments.

</td></tr><tr><td>

**sn\_cto.loc\_support\_agent**

</td><td>

Care Team Location Support Agent

</td><td>

Contains:

 sn\_hco.loc\_support\_agent

 wm\_read \(if Field Service Management is installed\)

</td><td>

Views/resolves all cases under assignment group and tracks and fulfills cases.

</td></tr><tr><td>

**sn\_cto.care\_team\_agent**

</td><td>

Care Team Agent

</td><td>

Contains:

 sn\_cto.loc\_support\_agent

 sn\_task\_plan.viewer

 wm\_basic

 sn\_hco.care\_team\_membe

</td><td>

Works on care team tasks and smart assessments.

</td></tr><tr><td>

**sn\_cto.care\_team\_agent\_manager**

</td><td>

Care Team Agent Manager

</td><td>

Contains:

 sn\_cto.care\_team\_agent

 sn\_task\_plan.creator

 sn\_customerservice.svc\_location\_manager

 sn\_hco.care\_team\_manager

</td><td>

Configures addition/removal of care team members, task plan templates, and smart questionnaire templates.

</td></tr><tr><td>

**sn\_cto.admin**

</td><td>

Care Team Work Management Admin

</td><td>

Contains:

 sn\_hco.admin

 sn\_cto.care\_team\_agent\_manager

 sn\_task\_plan.creator

</td><td>

Configures organizations and team structure and has all privileges of agent manager.

</td></tr><tr><td>

**sn\_hco\_orc.plan\_author**

</td><td>

Operational Leader

</td><td>

Contains:

 sn\_task\_plan.creator

 sn\_fsm\_planned\_wm.planned\_work\_admin

 sn\_case\_creation.org\_editor

</td><td>

Authors templates and schedules.

</td></tr><tr><td>

**sn\_hco\_orc.loc\_support\_agent**

</td><td>

Support Agent

</td><td>

 

</td><td>

Creates and fulfill the Healthcare orchestration tasks. Can create healthcare orchestration cases.

</td></tr><tr><td>

**sn\_hco\_orc.loc\_support\_agent\_manager**

</td><td>

Support Agent Department Manager

</td><td>

 

</td><td>

Tracks and manages all the tasks and cases for support departments.

</td></tr><tr><td>

sn\_hco\_orc.admin

</td><td>

Healthcare Orchestration Admin

</td><td>

Contains:

 sn\_hco.admin

</td><td>

Manages the Healthcare orchestration roles and duties.

</td></tr></tbody>
</table>