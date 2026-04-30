---
title: Define the network service instance details
description: Create an application service instance using the Telecommunications Network Inventory application. You can create service instances to model different types of network functions.Created topics for STRY55389656 - DOC1072742
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing your network functions, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Define the network service instance details

Create an application service instance using the Telecommunications Network Inventory application. You can create service instances to model different types of network functions.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.telco\_inventory\_catalog\_manager.

## About this task

When you create a network service instance record, it creates a corresponding configuration item \(CI\) record in the Network Service Instance \[cmdb\_ci\_network\_service\_instance\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then select **Services** &gt; **Service Instance**.

3.  Select **New**.

4.  On the Service Instance form, fill in the fields.

    To learn more about fields, see [Service Instance form](../reference/application-service-instance-form.md).

5.  To create the Telecommunications Network Inventory attributes for the Service Instance form, select **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Service Instance form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.


**Parent Topic:**[Managing your network functions](../concept/services.md)

