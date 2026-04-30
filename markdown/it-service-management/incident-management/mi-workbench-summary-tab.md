---
title: Major Incident workbench — Summary tab
description: The Summary tab provides a unified view of information in the form of a card layout. The information on impacted services, affected CIs, active outages, locations that are impacted, and child incidents helps to keep you informed about related records associated with an incident.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Manage major incidents, Incident Management, IT Service Management]
---

# Major Incident workbench — Summary tab

The **Summary** tab provides a unified view of information in the form of a card layout. The information on impacted services, affected CIs, active outages, locations that are impacted, and child incidents helps to keep you informed about related records associated with an incident.

## Summary tab

![Summary tab](../image/mim-summary-tab.png "View of the summary tab")

You can add, create, or edit each of the components. You can also view, post, or filter the latest activity on the major incident.

The tab also provides a quantitative summary of the active and completed tasks, as well as users or groups who are involved in resolving the major incident. The communication tasks are sorted in ascending order based on the order value.

The **Time remaining** column provides information regarding the time when the communication task is due.

-   If you do not perform the communication task within the set time, the value changes to **Overdue**.
-   If you activate the On-call Scheduling plugin \(com.snc.on\_call\_rotation\): The user who is on-call for the respective group and the group name appear in the summary.

The Groups section displays On-Call information, including the On-Call Escalation Tracking icon \(![On-Call Escalation Tracking icon](../image/icon-esc-tracking-oncall.png)\) that indicates the active status of the escalation. Green indicates an active escalation, and black indicates a finished escalation. Click the icon to view the On-Call Escalation Tracking pop-up.

Activate the Event Management plugin \(com.glideapp.itom.snac\) to add an **Alert** card under the **Summary** tab that keeps you up-to-date on the number of alerts for each incident. The count is the total of all primary and secondary alerts for the incident.

**Parent Topic:**[Major incident workbench UI elements](mi-workbench-ui-elements.md)

**Related topics**  


[Major Incident workbench — the Post Incident Report tab](mi-workbench-pir-tab.md)

[The Communicate tab in the Major Incident workbench](mi-workbench-communicate-tab.md)

[Major Incident workbench — the Collaborate tab](mi-workbench-collaborate-tab.md)

