---
title: Major Incident workbench — the Post Incident Report tab
description: The Post Incident Report tab helps you to understand the cause of the major incident, and the actions taken by the teams to resolve the incident.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Manage major incidents, Incident Management, IT Service Management]
---

# Major Incident workbench — the Post Incident Report tab

The **Post Incident Report** tab helps you to understand the cause of the major incident, and the actions taken by the teams to resolve the incident.

The teams can assess the incident response and resolution process and determine follow-up action items. The post incident report is required to record the actions performed, the reasons for doing them, and findings.

**Note:** The major incident manager can edit a report when the incident is in the **Resolved** state.

![Post incident report tab](../image/mim-pir-tab.png "View of the Post Incident Report tab")

The post incident report includes the following sections where a major incident manager can provide required information:

-   **Overview**: Summary of the incident.
-   **Findings**: Information on what caused the major incident and any lessons learned in the process.
-   **Resolution**: Information on the resolution steps taken to resolve the issue. The major incident manager can also add or edit any related Problem or Change information by clicking **Add** or **Manage** respectively.
-   **Timeline**: Information of all the activity feeds, not only of the incident but also of the incident communication plan and incident communication tasks related to the incident. You can update the timeline with the latest activity by clicking **Regenerate Timeline**.

    **Note:** The information that you provide for **Overview**, **Findings**, and **Timeline** gets updated in the Post Incident Report section on the Incident form.


If you activate the Continual Improvement Management \(CIM\) plugin \(com.sn\_cim\), the Related Improvement Records section is displayed in the report. This section displays the Inbound CIM Integrations records.

When you click **View Complete Report**, all the information entered by the major incident manager is compiled together and you can download the report in the .PDF format by clicking **Download Report PDF**.

The following links appear in the Incident form under the Related Links section:

-   **Regenerate PIR Timeline**: This link appears when incident is in the **Resolved** state and the user has the major\_incident\_manager role.
-   **Preview PIR**: This link appears when incident is in the **Resolved** or **Closed** state and the user has the itil role.

**Note:** On the downloaded report, under **Incident Response Timeline**, the time displayed in the timing type **Time to Identify** is calculated in the following ways:

-   If you propose the incident as a major incident: The time indicates the time from creation of the first related alert for this incident or creation of the incident \(in case there is no alert or the Event Management plugin is inactive\), whichever occurs first, until the time the incident is first proposed as a major incident.
-   If you create a major incident directly: The time indicates the time from creation of the first related alert for this incident or creation of the incident \(in case there is no alert or the Event Management plugin is inactive\), whichever occurs first, until the time the incident is promoted as a major incident.

**Parent Topic:**[Major incident workbench UI elements](mi-workbench-ui-elements.md)

**Related topics**  


[Major Incident workbench — Summary tab](mi-workbench-summary-tab.md)

[The Communicate tab in the Major Incident workbench](mi-workbench-communicate-tab.md)

[Major Incident workbench — the Collaborate tab](mi-workbench-collaborate-tab.md)

[Associate a new post incident report](../task/asso-new-post-incident-report.md)

