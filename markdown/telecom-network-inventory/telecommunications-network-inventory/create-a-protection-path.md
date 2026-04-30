---
title: Create a protection path
description: Create a protection path for the logical connection in the Telecommunications Network Inventory application. You can use this protection path as an alternative route in case the primary path \(logical connection\) fails or experiences significant issues.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using the network diagram, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a protection path

Create a protection path for the logical connection in the Telecommunications Network Inventory application. You can use this protection path as an alternative route in case the primary path \(logical connection\) fails or experiences significant issues.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\).

3.  Go to **Inventory** &gt; **Logical Connections**.

4.  Open a record and then select **View connection**.

5.  Select the **Protection path** tab and then select **New**.

6.  On the form, fill the following fields.

    |Field|Description|
    |-----|-----------|
    |Parent|Parent CI where you want to add the protection path.|
    |Type|CI Relationship type. For protection path, the CI relationship type is **Redundancy Provided by::Redundancy provided for**.|
    |Child|Logical connection record that you want to add as a protection path.|


## What to do next

You can view the protection path in the network diagram. To learn more, see [View the details of a network diagram](show-a-ci-related-details-network-diagram.md).

**Parent Topic:**[Using the network diagram](../concept/using-network-diagram.md)

**Related topics**  


[View the details of a network diagram](show-a-ci-related-details-network-diagram.md)

[Download a network diagram](download-network-diagram.md)

