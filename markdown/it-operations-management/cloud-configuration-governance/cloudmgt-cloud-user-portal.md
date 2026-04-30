---
title: Cloud User Portal
description: The Cloud User Portal gives you immediate access to all day-to-day cloud activities.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud User Portal

The Cloud User Portal gives you immediate access to all day-to-day cloud activities.

## Cloud User Portal

Use the Cloud User Portal to perform the following actions:

-   Monitor your quota, costs, budget, life-cycle events, stack health, and requests.
-   Request stacks from the service catalog and track requests.
-   Request life-cycle operations for stacks and resources \(for example, stop, start, or deprovision\).
-   Create and track incidents.

## Using the 'Overview' page

![Cloud User Portal overview screen](../image/user-portal.png)

<table id="table_azj_4ft_bx"><tbody><tr><td>

Launch a Stack

</td><td>

Open the service catalog of items that you can request. You request an item and, when your request is approved, the system launches the stack. See [Launch a stack](../task/cloudmgt-launch-stack.md).

</td></tr><tr><td>

Manage Stacks

</td><td>

View the stacks assigned to you. See [Manage a stack](../task/cloudmgt-manage-stacks.md).

</td></tr><tr><td>

View Activities

</td><td>

View activities for your stacks and resources. Activities include stack requests, change requests, incidents, cloud events, and SSH keys. See [View Activities](cloudmgt-user-activities.md).

</td></tr><tr><td>

View Resources

</td><td>

Opens the Resource Details page to view details and status of a resource. See [Manage a resource](../task/cloudmgt-manage-resources.md).

</td></tr><tr><td>

Pending Requests

</td><td>

When you submit a request for a stack, the **Activities** page displays the progress and status of the stack request, and a **Pending Requests** link and count appears. Click the link to view a summary of pending stack requests. See [Track a stack request](../task/cloudmgt-track-stack-request.md).

</td></tr></tbody>
</table>**Important:** Starting with the Xanadu release, the Current Month Spend and Budget widgets are deprecated for non domain-separated instances.

<table id="table-boxes"><tbody><tr><td>

Views

</td><td>

A filter to view and manage your resources as well as the resources assigned to the group you belong to.

</td></tr><tr><td>

Current Month Spend

</td><td>

A chart that shows costs, by category, for your cloud resources.

</td></tr><tr><td>

Budget

</td><td>

A chart displaying an arc based on your consumption of budget allocated to you.

</td></tr><tr><td>

Quota

</td><td>

A graph shows your quota consumption for quota-defined resource types such as VM Count, vCPUs Count, Storage Volume Size, Network Count, and Stack Count. You can view the quota that you have consumed compared to your maximum allocated quota. See [Viewing resource quota limits](resource-quota.md).

</td></tr><tr><td>

Recent Stacks

</td><td>

Ten stacks that you most recently requested. Each entry shows the **Name**, **Catalog item** requested, **Cloud account** used to request the stack, and the order status of the requested stack. Click a **Name** to view stack details.

</td></tr><tr><td>

Stack Health

</td><td>

Shows the most recent 10 items: Incidents created for provisioned stacks or active stacks with a resource turned off. Also shows the resources which are down. Click an item to view stack details. Color codes for incident type: -   Red: Outage.
-   Orange: Performance issue or Something is broken.
-   Grey: Question or Request.

</td></tr></tbody>
</table>## Using the task bar

From the task bar, you can perform the following actions:

![The task bar on the 'Overview' page](../image/portal-taskbar.png)

<table id="table_sgg_1xg_3z"><tbody><tr><td>

Overview

</td><td>

Return to the home page of the Cloud User Portal.

</td></tr><tr><td>

Catalog

</td><td>

View the Service Catalog of items that you can request to launch stacks. When you select a **Service Category** \(VM, Compute, Network, Storage, and so on\), the **All Items** section lists the items in the selected category. Click **Launch** to request an item. See [Launch a stack](../task/cloudmgt-launch-stack.md).

</td></tr><tr><td>

Stacks

</td><td>

Lists all stacks that are assigned to you. Select a catalog item to view the stacks that the item launches. Click a stack to view details—all resources, resource properties, activities, and life cycle operations. See [Manage a stack](../task/cloudmgt-manage-stacks.md).

</td></tr><tr><td>

Resources

</td><td>

Lists individual resources of the provisioned stacks that are assigned to you, regardless of who requested the stack. See [Manage a resource](../task/cloudmgt-manage-resources.md).

</td></tr><tr><td>

Activities

</td><td>

Stack requests, change requests, cloud life cycle events \(if configured\), and incidents that are associated with your stacks and resources. SSH keys that you created or that were generated for you. See [View Activities](cloudmgt-user-activities.md).

</td></tr></tbody>
</table>