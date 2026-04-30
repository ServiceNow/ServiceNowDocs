---
title: Logical connections
description: Design and assign a logical connection in the Telecommunications Network Inventory application. By using the Design and Assign function, you can fulfill the logical connection design request of a customer.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Design and assign your network services, Explore, Telecommunications Network Inventory]
---

# Logical connections

Design and assign a logical connection in the Telecommunications Network Inventory application. By using the Design and Assign function, you can fulfill the logical connection design request of a customer.

The Design and Assign function provides the activities and tasks that an agent can perform to create a logical connection. Depending on the design request, the agent can design a logical connection and assign the related network inventories to that connection.

## Design and Assign function layout and features

The following example shows the Design and Assign function layout for a logical connection.

![View of Design and Assign function layout.](../image/design-assign-paybook-layout.png "Design and Assign function layout and features")

<table id="table_crd_4hd_ndc"><thead><tr><th>

Callout

</th><th>

Feature

</th><th>

 

</th></tr></thead><tbody><tr><td>

1

</td><td>

Activity picker

</td><td>

The activity picker displays the list of activities to design and assign a logical connection. Each activity has an indicator that shows the activity state:-   ![Activity In progress Icon](../image/icon-activity-progress.png) - Activity is work in progress.
-   ![Activity Complete Icon](../image/icon-activity-complete.png) - Activity is completed.
-   ![Activity Pending Icon](../image/icon-activity-pending.png) - Pending activities.
-   ![Activity Skipped Icon](../image/icon-activity-skip.png) - Activity is skipped.

Select an activity to view the details in the activity viewer.

</td></tr><tr><td>

2

</td><td>

Activity viewer

</td><td>

The activity viewer displays the selected activity. Activity viewer is the main work area where an agent performs the work necessary to complete the current activity.You can collapse the activity viewer panel.

</td></tr><tr><td>

3

</td><td>

Activity cards

</td><td>

Activity cards display the details about the current activity in the activity viewer. Depending on the type of activity, the activity cards can display information such as field information to set up an end point.Agents use the cards to complete the work for each activity, such as adding end points or setting attributes.

</td></tr><tr><td>

4

</td><td>

Network diagram

</td><td>

Network diagram graphically displays a circuit of the logical connection elements. After you complete each activity, the network diagram updates and displays the data. You get a clear visualization of your design.You can expand the network diagram by collapsing the activity picker and activity details panels.

You can expand the pills in the diagram to see all underlying connection elements. Hover over each pill show the full name of that connection element.

</td></tr></tbody>
</table>## Design and Assign workflow for logical connection

![Infographic showing the workflow diagram of design and assign playbook for logical connection. To learn more, see following text.](../image/MMASSET0020713-design-assign-playbook-logical-connection.png "Design and Assign playbook workflow for logical connection")

The Design and Assign function for a logical connection has the following workflow.

1.  Create a change request and add necessary details about your design.
2.  Provide connection details which influence the design such as logical connection model, bandwidth, and domain.
3.  Select end points such as network sites and interfaces where the connection starts and terminates.
4.  Select connection elements between the endpoints.
5.  Select a protection path to define the redundancy path for your logical connection.
6.  Select a number element such as VLAN or LAG.
7.  Select an IP address.
8.  Review the design and submit for approval.

By completing these steps, a logical connection record is generated with the associated Configuration Items \(CI\).

To learn more about the steps to design and assign a logical connection, see [Create a logical connection record using the Design and Assign function](../task/create-logical-connection-record-design-assign-playbook.md).

## Access

You can access the Design and Assign function for a logical connection in the Telecommunications Network Inventory Workspace as follows:

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Select the design and assign icon \(![Design and Assign Icon.](../image/icon-design-assign.png)\) to open the Design request overview window.
3.  Select **New** &gt; **Create Logical Connection** or select any change request from the list.

**Related topics**  


[Design and assign your network services](design-assign-playbook.md)

[Telecommunications Network Inventory subflows](subflow.md)

