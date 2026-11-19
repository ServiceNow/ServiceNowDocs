---
title: Post Incident Report tab in the Major Incident workbench
description: The Post Incident Report tab shows the cause of the major incident and the actions that teams took to resolve it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/mi-workbench-pir-tab.html
release: brazil
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Post Incident Report tab in the Major Incident workbench

The **Post Incident Report** tab shows the cause of the major incident and the actions that teams took to resolve it.

The teams can assess the incident response and resolution process and determine follow-up action items. The post-incident report records the actions performed, the reasons for them, and the findings.

**Note:** The major incident manager can edit a report when the incident is in the **Resolved** state.

\[Omitted image "mim-pir-tab.png"\] Alt text: Post Incident Report tab showing the Overview, Findings, Resolution, and Timeline sections

The post-incident report includes the following sections, where a major incident manager provides the required information:

-   **Overview**: Summary of the incident.
-   **Findings**: Information on what caused the major incident and any lessons learned in the process.
-   **Resolution**: Steps taken to resolve the issue. The major incident manager can also add or edit related problem or change information by selecting **Add** or **Manage**, respectively.
-   **Timeline**: Activity feeds of the incident and its related incident communication plans and incident communication tasks. You can update the timeline with the latest activity by selecting **Regenerate Timeline**.

    **Note:** The information that you provide for **Overview**, **Findings**, and **Timeline** is updated in the Post Incident Report section of the Incident form.


You must have any of the following roles to work on different features on the **PIR** tab:

-   For PIR review: sn\_incident\_read or sn\_incident\_write
-   For PIR update, generate, download, publish or edit co-contributor: major\_incident\_manager, sn\_incident\_write \(report author, assigned to the incident or added as co-contributors\) or admin

After you resolve a major incident, publish the PIR and share it with stakeholders within the time defined in the SLA. To configure the SLA, set the value in positive number of hours in the **PIR publish hours** \(**sn\_sow\_inc.pir.publish.hours**\) system property. This property enables you to set how long after resolution, a post incident report must be published, and drives the PIR banner on the incident record.

After the SLA is configured, the following type of banners are displayed based on the SLA elapsed or time remaining:

-   Information banner - Displays the information "Publish post incident report by &lt;date&gt;&lt;time&gt;" message when less than 70 percentage of the SLA has elapsed since major incident resolution.
-   Warning banner - Displays the caution message with remaining time "Caution! PIR SLA &lt;n&gt; is approaching. Publish post incident report by &lt;date&gt;&lt;time&gt;." when 70 to 100 percentage of the SLA has elapsed since major incident resolution.
-   Critical banner - Displays "SLA Breached! Publish post incident report as soon as possible." message when the no time is remaining and SLA is breached.

If you activate the Continual Improvement Management \(CIM\) plugin \(com.sn\_cim\), the Related Improvement Records section is displayed in the report. This section displays the Inbound CIM Integrations records.

When you select **View Complete Report**, the information that the major incident manager entered is compiled, and you can download the report as a PDF file by selecting **Download Report PDF**.

The following links appear in the Incident form under the Related Links section:

-   **Regenerate PIR Timeline**: This link appears when the incident is in the **Resolved** state and the user has the major\_incident\_manager role.
-   **Preview PIR**: This link appears when the incident is in the **Resolved** or **Closed** state and the user has the itil role.

**Note:** On the downloaded report, under **Incident Response Timeline**, the time displayed in the timing type **Time to Identify** is calculated in the following ways:

-   If you propose the incident as a major incident: The time is measured from the first related alert. If no alert exists or the Event Management plugin is inactive, the time is measured from the incident creation. The end point is when the incident is first proposed as a major incident.
-   If you create a major incident directly: The time is measured from the first related alert. If no alert exists or the Event Management plugin is inactive, the time is measured from the incident creation. The end point is when the incident is promoted to a major incident.

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Summary tab in the Major Incident workbench]()

[Communicate tab in the Major Incident workbench]()

[Collaborate tab in the Major Incident workbench]()

[Associate a new post-incident report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management/asso-new-post-incident-report.md)

