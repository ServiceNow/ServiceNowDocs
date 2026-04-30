---
title: View Major Security Incident trend charts
description: View the major security incident impact progress metrics visualized as bar graphs and charts.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View Major Security Incident trend charts

View the major security incident impact progress metrics visualized as bar graphs and charts.

In addition to the incident timeline and progress trend chart visualizations, the **Overview** tab provides relevant impact metrics to manage the changing scope of the incident, including rollup of affected assets, users, locations, and team resources.

The counts displayed in the visualization components are based on active tasks on linked Security Incident Response \(SIR\) incidents. As tasks are opened and closed, these counts change in terms of the nature and volume of remaining activity planned for the major security incident to represent the trends shown in the trend chart visualization components.

![View the impact metrics of the major security incident](../image/overview-tab-msim.png "MSIM Overview tab impact metrics")

Refer to the following table for the UI actions that you can perform from the **Overview** section:

<table id="table_o5x_ryq_vrb"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Time**

</td><td>

Displays the period in total number of days from when the major security incident is active.The time is calculated based on the **Detection Date** entered in the **Details** tab of the workspace.

The Detection Date is often captured initially when the major security incident was first created or proposed. Whenever, this date is modified the time is automatically calculated, refreshed, and displayed in the format days: hours: minutes, for example 20D: 13H: 58M.

**Estimated resolution date**: The date by when the incident resolution date is estimated to resolve. This date is often captured initially when the major security incident was first created or promoted.

The date is updated and refreshed based on the estimated date provided in the **Details** tab of the workspace.

If the estimated date is not provided in the Details section, then this section displays ‘hyphen’ without any date value.

</td></tr><tr><td>

**Active Team**

</td><td>

Displays the different response teams and team members from each team who are actively working on the major security incident and its related tasks.**Active Team** trend: Displays the trend chart of each team and its team members who are actively working on the major security incident and related tasks on regular interval.

**Note:** View the assigned active groups from the **Details** tab of the workspace.

</td></tr><tr><td>

**Linked SIR incidents**

</td><td>

**By incident state**: View the distribution of linked security incidents based on a incident state such as Analysis, Contain, Eradicate, Recover, or Review.**Trends by incident state**: Further indicates the trend view of how the number of linked incidents are progressing based on incident state.

Selecting each incident state link allows you to navigate and view the linked security incident details directly on the **Linked SI/VI** tab of the workspace.

This section is updated and refreshed automatically whenever changes occur to the underlying incidents.

</td></tr><tr><td>

**SIR Tasks**

</td><td>

Displays active task totals that are linked to the MSI record via SIR incidents.-   **By task state**: View the incident response tasks based on the incident state such as Draft, Assigned, Work in progress, Closed Complete. This distribution chart allows for a further distribution breakdown by assignment groups. Selecting each task state allows you to view a filtered list by incident task state on the **Tasks** tab of the workspace. The filtered view allows you to view and update individual task details.
-   **In progress tasks by incident state label**: Displays active tasks and groups based on incident state label that must be applied in the Task Organizer components. These default labels have values such as Analysis, Contain, Eradicate, Recover, or Review to indicate the nature of the task involved.
-   **Overdue**: Displays the security incident response tasks, which are active and had exceeded the due date.

You can view the details of all the overdue tasks by selecting the total Overdue count and having it auto navigate to the Tasks tab.

-   **Trends by task state**: View the progress trend of both work in progress and closed response tasks over the incident duration.

**Note:** The trend chart graph retrieves the latest data based on the scheduled job. You can configure or modify the data retrieval time interval as required.

</td></tr><tr><td>

**MSI Tasks**

</td><td>

Displays active tasks in total, which were created directly on the MSI record \(and these aren’t linked response tasks\):**By task state:** View the major security incident created tasks, assigned tasks and its related information.

Selecting each task state allows you to view a filtered list by incident task state on the **Tasks** tab of the workspace. The filtered view will allow for viewing and updating individual task details.

</td></tr><tr><td>

**External Collaboration**

</td><td>

Displays collaboration activities in total for all the labelled collaboration activities from the Collaboration Activity Stream:-   **By incident state label:**View the incident collaboration activities data that are coordinated with Microsoft Teams and Microsoft SharePoint files and folders and are labeled using incident state labels such as Analysis, Contain, Eradicate, or Recover from the **Collaboration** tab of the workspace.
-   **Trends by activity type**: View the trend chart for the number of Microsoft Teams and Microsoft SharePoint files and folders activities over the incident duration.

</td></tr></tbody>
</table>**Parent Topic:**[Using Major Security Incident Management](../../security-incident-response/concept/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

[Using MSI List view in the MSIM workspace](../../security-incident-response/task/list-view-in-msim.md)

[View Major Security Incident impact metrics](viewing-trend-charts-and-progress-of-msi.md)

[Update Major Security Incident details](msim-details-tab.md)

[Link additional records to Major Security Incident](../task/linking-additional-records-to-major-security-incidents.md)

[Unlink records from Major Security Incident](../task/unlinking-msi-records.md)

[Manage tasks in a Major Security Incident](tasks-tab.md)

[Track collaboration activity via MSIM workspace](collab-tab.md#)

[Create and distribute MSIM Status Reports](../task/creating-and-distributing-major-security-incident-status-reports.md)

