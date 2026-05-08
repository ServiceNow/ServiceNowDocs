---
title: Design and assign your network services
description: The Design and Assign function provides step-by-step guidance for designing a network service in the Telecommunications Network Inventory application. You can use the Design and Assign function to complete guided activities to design the network services and assign the network inventories.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Design and assign your network services

The Design and Assign function provides step-by-step guidance for designing a network service in the Telecommunications Network Inventory application. You can use the Design and Assign function to complete guided activities to design the network services and assign the network inventories.

## Introduction to design and assign function

The Design and Assign function is an end-to-end workflow that includes the necessary steps to design a network service against a design request. You can visualize a workflow in a task-oriented view and guides users through sequences of tasks to complete the design process. The Design and Assign function offers a structured approach for agents to deliver a network service. It provides agents with clear visibility into the steps to be executed, the network resources to be allocated at each step, and how everything is integrated together.

The Design and Assign framework breaks the design workflow into multiple activities. Each activity includes the steps necessary for an agent to complete that activity. Activities also include automated workflows, such as creation of change tasks for the next step when an activity is complete.

The Design and Assign function include:

-   An activity picker displays the activities.
-   A series of steps that you have to complete to achieve a particular goal for each activity.

## Design and Assign home page

The Design and Assign home page displays all change requests \(design requests\) that are in the Design in Progress state. Selecting a change request redirects to the corresponding Design and Assign function where you can visualize the workflow in a task-oriented view. You can also select the UI action to launch a Design and Assign function from the home page. For example, select **Create Logical Connection** to launch the Design and Assign function for a new logical connection.

The following is an example for the Design and Assign home page.

![Design and Assign home page with list of change requests.](../image/design-assign-homepage.png "Example of Design and Assign home page") ![]( "Example of Design and Assign home page")

Access the Design and Assign home page in the Telecommunications Network Inventory workspace as follows.

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Select the design and assign icon \(![Design and Assign Icon](../image/icon-design-assign.png)\).

To refresh the home page, select refresh icon \(![Refresh Icon.](../image/icon-refresh.png)\).

## Design and Assign function user roles

<table id="table_dgk_5sq_pdc"><thead><tr><th>

User role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network Planning Agent \[sn\_ni\_core.network\_planning\_agent\]

</td><td>

-   View the Design and Assign home page for assigned requests.
-   Create a logical connection design request.
-   Complete the activities according to sequence.
-   View the diagram and validate the design as activity progresses.
-   Review and complete the Design and Assign request.

</td></tr><tr><td>

Network Planning Manager \[sn\_ni\_core.network\_planning\_manager\]

</td><td>

-   View the Design and Assign home page for your and your team's assigned requests.
-   Create a logical connection design request.
-   Complete the activities according to sequence.
-   View the diagram and validate the design as activity progresses.
-   Review and complete the Design and Assign request.

</td></tr><tr><td>

Playbook admin \[playbook.admin\]

</td><td>

Uses the Workflow Studio application to author, configure, and monitor the Design and Assign function.

</td></tr></tbody>
</table>## Creating and configuring Design and Assign function for your network services

You can create the Design and Assign function for various types of network services such as designing a Gigabyte Passive Optical Network \(GPON\) Broadband service. You can use ServiceNow AI Platform capabilities and Workflow Studio application to create and configure the Design and Assign function. To learn more, see [Configuring Design and Assign function for your network services](configure-playbooks-design-assign-function.md).

## Using Design and Assign function

The inventory agents can use the guidance available with the Design and Assign function to complete the tasks and activities. These activities are needed to design your network service and assign the network resources.

A Design and Assign function includes multiple activities for an agent to complete. When using a Design and Assign function, agents can:

-   View the activities.
-   Select an activity and perform the work necessary to complete that activity.
-   Mark an activity as complete and move to the next activity.
-   Complete the activities necessary to design and assign an inventory record.

To learn more, see [Design and Assign function](using-playbooks-design-assign-inventory-record.md).

You can create a logical connection by using the Design and Assign function available in the Telecommunications Network Inventory application. To learn more, see [Logical connections](design-logical-connection-design-assign-playbook.md).

