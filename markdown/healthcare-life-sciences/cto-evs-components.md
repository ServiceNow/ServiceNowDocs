---
title: Components installed with Care Team Operations for Environmental Services
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Environmental Services plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-21"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Environmental Services

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Environmental Services plugin.

|Table name|Description|
|----------|-----------|
|Healthcare EVS case \[sn\_cto\_evs\_case\]|Abstract case type that provides a foundation to extend from when building your own operational request types.|

<table id="table_xv4_wl2_1gc"><thead><tr><th>

Role name

</th><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cto\_evs.admin

</td><td>

Admin

</td><td>

Configures organizations and team structure for Care Team Operations for Environmental Services.Configures all application setup data for Care Team Operations for Environmental Services.

</td></tr><tr><td>

sn\_cto\_evs.viewer

</td><td>

Case viewer

</td><td>

Can view EVS cases and all HCLS foundation data.Views EVS cases and all HCLS foundation data.

</td></tr><tr><td>

sn\_cto\_evs.loc\_support\_agent

</td><td>

Environmental Services support agent

</td><td>

Can view/resolve all cases under their assignment group, track cases, and fulfill cases.Views and resolves EVS cases assigned to their teams.

</td></tr><tr><td>

sn\_cto\_evs.loc\_contributor

</td><td>

Location contributor roleLocation contributor

</td><td>

Can report cases, respond to cases, track cases at the business location, and view cases under their team.Creates EVS cases and reports, views, tracks, and responds to EVS cases.**Note:** This role is automatically inherited into the Care Team Member role when the Care Team Operations for Environmental Services plugin is installed.

</td></tr><tr><td>

sn\_cto\_evs.loc\_manager

</td><td>

Environmental services support department managerLocation manager

</td><td>

Monitors the tasks within their organizations.Views and resolves EVS cases assigned to their teams as a location manager.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|sn\_cto\_evs.EVSCase|Service script for EVS cases.|
|sn\_cto\_evs.EVSCaseDAO|Data access object \(DAO\) class for EVS cases.|
|sn\_cto\_evs.EVSCaseActionUtil|Utility class for EVS case actions.|
|sn\_cto\_evs.EVSCaseAJAX|AJAX handler for EVS case client-side interactions.|
|sn\_cto\_evs.EVSConstants|Constants used across EVS case scripts.|

|Integration|Description|
|-----------|-----------|
|Care Team Mobile \(`com.sn_cto_mobile`\)|Adds mobile screens, push notifications, and navigation support for EVS cases in the Care Team mobile app.|
|Semantic Search \(`com.glide.ais.semantic_search`\)|Enables AI-powered semantic search for EVS cases.|

