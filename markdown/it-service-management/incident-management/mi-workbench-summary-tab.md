---
title: Summary tab in the Major Incident workbench
description: The Summary tab displays information about records related to an incident in a card layout, including impacted services, affected configuration items \(CIs\), active outages, impacted locations, and child incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/mi-workbench-summary-tab.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Summary tab in the Major Incident workbench

The **Summary** tab displays information about records related to an incident in a card layout, including impacted services, affected configuration items \(CIs\), active outages, impacted locations, and child incidents.

\[Omitted image "major-incident-workbench.png"\] Alt text: Summary tab of the major incident workbench with cards for related records

You can add, create, or edit each of the components. You can also view, post, or filter the latest activity on the major incident.

The tab also provides a quantitative summary of the active and completed tasks and of the users or groups involved in resolving the major incident. The communication tasks are sorted in ascending order based on the order value.

The **Time remaining** column shows when the communication task is due.

-   If you don't perform the communication task within the set time, the value changes to **Overdue**.
-   If you activate the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\), the summary displays each group name and the user who is on call for that group.

The Groups section displays on-call information, including the On-Call Escalation Tracking icon \[Omitted image "icon-esc-tracking-oncall.png"\] Alt text: that indicates the active status of the escalation. Green indicates an active escalation, and black indicates a finished escalation. Select the icon to view the On-Call Escalation Tracking pop-up.

Activate the Event Management plugin \(com.glideapp.itom.snac\) to add an **Alert** card to the **Summary** tab that shows the number of alerts for each incident. The count is the total of all primary and secondary alerts for the incident.

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Post Incident Report tab in the Major Incident workbench]()

[Communicate tab in the Major Incident workbench]()

[Collaborate tab in the Major Incident workbench]()

