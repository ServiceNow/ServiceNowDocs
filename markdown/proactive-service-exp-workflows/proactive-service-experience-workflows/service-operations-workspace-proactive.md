---
title: Proactive Service Experience Workflows and Incident Management within the Service Operations Workspace
description: You can use the Service Operations Workspace application to get an overview of how a network agent can prioritize tasks and resolve incidents.
locale: en-US
release: xanadu
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Explore, Proactive Service Experience Workflows]
---

# Proactive Service Experience Workflows and Incident Management within the Service Operations Workspace

You can use the Service Operations Workspace application to get an overview of how a network agent can prioritize tasks and resolve incidents.

## Viewing the Service Operations Workspace

From the **Workspaces** menu, select **Service Operations Workspace** and select the **Home** icon. From the landing page, a network agent can analyze incidents and view cases and upcoming tasks. To view:

-   **Lists**: Select the **Lists** tab in the Service Operations Workspace. From the Lists tab, a network agent can analyze the individual lists of incidents and tasks and then take the appropriate action.

    The following example shows the List tab.

    ![List view of all incidents, and tasks, and planned incidents.](../image/list-tab-sow-proactive.png "List tab")

-   Records: Open any task record to navigate to its record view as shown in the following example.

    ![Record view page of Service Operations Workspace.](../image/record-view-proactive.png "Record view")


## Example

The Proactive Service Experience Workflows application is automatically triggered when an incident is created within the system by an alert flow. A technical support can manually create this alert in the Service Operations Workspace. It can also be generated from an external fault management system using the TMF 621 integration.

The following example demonstrates how Proactive Service Experience Workflows is used to resolve an external network-initiated incident. In this example,

1.  An external fault management system using TMF 621 integration sends an alert that triggers the creation of an incident record with the following values:
    -   Short Description and Description: Vmanage\_10001 failed to restart after a change was implemented.
    -   Configuration Item: Vmanage\_10001 \(SD-WAN CI Class\)
    -   Category: SD-WAN
    -   Sub Category: Protocol Failure
    -   Affected Customers: 5
2.  A technical support engineer opens the incident record inside the Service Operations Workspace and sees the list of impacted services and accounts in the **Overview** section.
3.  The technical support engineer triages the issues by reviewing the latest changes in the Agent Assist that triggered the outage.
4.  The technical support engineer then restarts the SD-WAN controller and selects **Generate Proactive Cases** in the Cases section. One major case and five child cases are generated and notifications are sent to the primary contacts for the affected accounts.
5.  As a major case was created, the technical support engineer notifies the major issue manager of a potentially serious outage. The Major Issue Manager manages the major case record and communication with both technical teams and affected customers.
6.  The Technical Support Engineer \(TSE\) realizes the device can't be rebooted and might have failed altogether. The TSE changes the Sub Category field to device failure and selects the **Escalate UI** action and enters a work note
7.  The next level L2 Support team receives the incident and updates the record status.
8.  The L2 Technical Support Engineer tries to troubleshoot the issues on the SD-WAN controller and successfully restarts the configuration item. Four out of the five the affected accounts report the issue is resolved, but the fifth account is still experiencing some problems.
9.  To diagnose further issues with the fifth account, the L2 Technical Support Engineer performs the following steps:
    -   Selects the check box next to the case record on the Overview page.
    -   Selects the **Notify UI** action to send a message via additional comments to the contact person on the case record.
10. The contact person receives the additional comment and performs some extra steps. When the service is restored, the contact updates the status in the CSM portal.
11. Seeing the additional comments in the incident record, the L2 Technical Support Engineer changes the State field to **Resolved**.

    The resolution information is copied down to each case record, while the Major Issue Manager resolves the major case record and any associated cases.


**Parent Topic:**[Exploring the Proactive Service Experience Workflows architecture](../concept/explore-assurance-workflows.md)

