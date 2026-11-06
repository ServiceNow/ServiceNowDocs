---
title: View major incident information on the Incident form
description: View major incident details on the Major Incident and Post Incident Report tabs, which appear on the Incident form when an incident enters the major incident life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/view-major-info.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# View major incident information on the Incident form

View major incident details on the Major Incident and Post Incident Report tabs, which appear on the Incident form when an incident enters the major incident life cycle.

## Before you begin

Role required: itil, sn\_incident\_read, or admin

The incident must be in the major incident life cycle.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Select the incident that is in the major incident life cycle.

3.  Select the **Major Incident** tab.

<table id="table_nkm_t4r_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Major incident state

</td><td>

A major incident state can be one of the following:-   **Proposed**: The initial state when a major incident candidate is created or proposed.
-   **Accepted**: The state when a major incident manager directly creates a major incident or promotes a candidate to a major incident.
-   **Rejected**: The major incident candidate is rejected by a major incident manager.
-   **Canceled**: The major incident is demoted by a major incident manager.


</td></tr><tr><td>

Proposed by

</td><td>

User who proposed the incident as a major incident candidate.

</td></tr><tr><td>

Proposed

</td><td>

Date and time when the incident was proposed as a major incident candidate.

</td></tr><tr><td>

Promoted by

</td><td>

User who promoted the incident to a major incident.

</td></tr><tr><td>

Promoted

</td><td>

Date and time when the incident was promoted to a major incident.

</td></tr><tr><td>

Business impact

</td><td>

Business impact of the issue identified in the major incident.

</td></tr><tr><td>

Probable cause

</td><td>

Probable cause of the issue identified in the major incident.

</td></tr></tbody>
</table>4.  Select the **Post Incident Report** tab.

    If post incident report information is already filled in on the major incident workbench, it appears in the following fields:

    |Field|Description|
    |-----|-----------|
    |Overview|Summary of the incident.|
    |Findings|Information on what caused the major incident and any lessons learned in the process.|
    |Timeline|Activity feeds of the incident and of its related incident communication plan and communication tasks.|


**Parent Topic:**[Working on major incident management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/work-on-mim.md)

