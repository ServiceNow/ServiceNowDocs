---
title: Major Incident workbench — Summary tab
description: The Summary tab provides a unified view of information in the form of a card layout. The information on impacted services, affected CIs, active outages, locations that are impacted, and child incidents helps to keep you informed about related records associated with an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/mi-workbench-summary-tab.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Manage major incidents, Incident Management, IT Service Management]
---

# Major Incident workbench — Summary tab

The **Summary** tab provides a unified view of information in the form of a card layout. The information on impacted services, affected CIs, active outages, locations that are impacted, and child incidents helps to keep you informed about related records associated with an incident.

## Summary tab

\[Omitted image "major-incident-workbench.png"\] Alt text: major incident workbench-summary tab

You can add, create, or edit each of the components. You can also view, post, or filter the latest activity on the major incident.

The **Summary** tab of the Major incident workbench contain cards in horizontal arrangement that displays the number of records associated with the major incident. Selecting each card guides you to the cards section which is available next to \(after\) the Latest Activity section in the workbench. The card contains the list of records that you can select individually to open in a separate tab. The card also enables you with additional options for specific records. The following cards are available:

-   Impacted services - Displays the primary business service and Configuration Items \(CI\) that are impacted. The card has the following options:
    -   Add - Adds impacted business service or CIs to the major incident record.
    -   Refresh - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Refresh** to refresh the list of business service or CIs associated with the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of business service filtered for the major incident record, in a separate tab.
-   Affected CIs - Displays the number of CIs that are affected. The card has the following options:
    -   Add - Adds affected CIs to the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of affected CIs filtered for the major incident record, in a separate tab.
-   Alerts - Displays alerts associated with the major incident record. You can select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of alerts filtered for the major incident record, in a separate tab.

    Activate the Event Management plugin \(com.glideapp.itom.snac\) to add an **Alert** card to the **Summary** tab that shows the number of alerts for each incident. The count is the total of all primary and secondary alerts for the incident. An alert is a notification for selected events that are considered to be important and require attention. Event Management generates alerts based on event rules. You can monitor and resolve alerts in ways that are based on alert impact calculations and alert configuration and property settings. For more information, see [Manage and monitor alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/c_EMAlert.md).

-   Outages - Displays the task outages associated with the major incident record. The card has the following options:
    -   Create - Create a task outage for the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of outages filtered for the major incident record, in a separate tab.
-   Affected locations - Displays the affected locations associated with the major incident record. The card has the following options:
    -   Add - Adds an affected location to the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of locations filtered for the major incident record, in a separate tab.
-   Child Incidents - Displays the child incidents associated with the major incident record. The card has the followings options:
    -   Create - Creates an incident record which is added as a child incident of the major incident record.
    -   Add - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Add** to add an existing incident record as a child incident of the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open the list of child incidents filtered for the major incident record, in a separate tab.
-   Incident Tasks - Displays the incident tasks associated with the major incident record. The card has the following options:
    -   Create - Creates an incident task which is added to the major incident record.
    -   Manage - Select the More actions icon \(\[Omitted image "dpr-icon-more-actions-v.png"\]\) and then select **Manage** to open list of incident tasks filtered for the major incident record, in a separate tab.

The tab also provides a quantitative summary of the active and completed tasks, as well as users or groups who are involved in resolving the major incident. The communication tasks are sorted in ascending order based on the order value.

The **Time remaining** column provides information regarding the time when the communication task is due.

-   If you do not perform the communication task within the set time, the value changes to **Overdue**.
-   If you activate the On-call Scheduling plugin \(com.snc.on\_call\_rotation\): The user who is on-call for the respective group and the group name appear in the summary.

The Groups section displays On-Call information, including the On-Call Escalation Tracking icon \(\[Omitted image "icon-esc-tracking-oncall.png"\] Alt text: On-Call Escalation Tracking icon\) that indicates the active status of the escalation. Green indicates an active escalation, and black indicates a finished escalation. Click the icon to view the On-Call Escalation Tracking pop-up.

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Post Incident Report tab]()

[The Communicate tab in the Major Incident workbench]()

[Major Incident workbench — the Collaborate tab]()

