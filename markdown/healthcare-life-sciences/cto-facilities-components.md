---
title: Components installed with Care Team Operations for Facilities
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Facilities plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Facilities

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Facilities plugin.

|Table name|Description|
|----------|-----------|
|Healthcare Facilities case \[sn\_cto\_facilities\_case\]|Abstract case type that provides a foundation to extend from when building your own operational request types.|

<table id="table_pkv_ccx_zfc"><thead><tr><th>

Role \[name\]

</th><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cto\_facilities.admin

</td><td>

Admin

</td><td>

Configures organizations and team structure for Care Team Operations for Facilities.

</td></tr><tr><td>

sn\_cto\_facilities.viewer

</td><td>

Case viewer

</td><td>

Can view Healthcare Facilities cases and all HCLS foundation data.

</td></tr><tr><td>

sn\_cto\_facilities.loc\_support\_agent

</td><td>

Facilities support agent

</td><td>

Can view/resolve all cases under their assignment group, track cases, and fulfill cases.

</td></tr><tr><td>

sn\_cto\_facilities.loc\_contributor

</td><td>

Location contributor role

</td><td>

Can report cases, respond to cases, track cases at the business location, and view cases under their team. **Note:** This role is automatically inherited into the Care Team Member role when the Care Team Operations for Facilities plugin is installed.

</td></tr><tr><td>

sn\_cto\_facilities.loc\_manager

</td><td>

Facilities services support department manager

</td><td>

Monitors the tasks within their organizations.

</td></tr></tbody>
</table>|Plugin name|Description|
|-----------|-----------|
|Care Team Portal\(com.sn\_cto\_sp \)|Provides a portal experience for Care Team Operations for Facilities users to create requests for supporting departments, manage teams, and gain visibility into submitted requests.|
|Healthcare Operations Core\[com.sn\_hco\]|Healthcare Operations Core provides clinicians with an uniform interface to report and track issues related to their day-to-day operations. This helps hospitals eliminate inefficient manual processes, reduce patient safety risks and increase patient satisfaction through timely resolution of issues and completion of important tasks.|

|Script include \[API name\]|Description|
|---------------------------|-----------|
|FacilitiesCase \[sn\_cto\_facilities.FacilitiesCase\]|Service-layer logic for creating and managing Healthcare Facilities cases.|
|FacilitiesCaseAJAX \[sn\_cto\_facilities.FacilitiesCaseAJAX\]|Handles asynchronous server-side requests for the Healthcare Facilities case form.|
|FacilitiesCaseActionUtil \[sn\_cto\_facilities.FacilitiesCaseActionUtil\]| |
|FacilitiesCaseDAO \[sn\_cto\_facilities.FacilitiesCaseDAO\]|Data access layer for the Healthcare Facilities Case \[sn\_cto\_facilities\_case\] table.|
|FacilitiesConstants \[sn\_cto\_facilities.FacilitiesConstants\]|Defines application-wide constants for Care Team Operations for Facilities.|

Care Team Operations for Facilities supports the following integrations when the corresponding plugins are active:

-   **Mobile** — Care Team Operations for Facilities is available on mobile devices when the Care Team Mobile plugin \(com.sn\_cto\_mobile\) is active.
-   **Semantic search** — AI-powered semantic search is available when the semantic search plugin \(com.glide.ais.semantic\_search\) is active.

