---
title: Create a default template
description: Create a default template in the Telecommunications Network Inventory application to capture the default attribute definition for a specific configuration item \(CI\) class.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create inventory template for network asset instantiation, Use, Telecommunications Network Inventory]
---

# Create a default template

Create a default template in the Telecommunications Network Inventory application to capture the default attribute definition for a specific configuration item \(CI\) class.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, and sn\_ni\_core.inventory\_template\_manager

## About this task

Default templates capture the default attribute values for a configuration item \(CI\) class. A template defines the set of attribute values for any resource \(equipment, card, and so on\). When this default template is associated with an inventory template, it adds these attribute values to the resource that is instantiated using that template.

When you use the **Template** field to select the table that stores the CI class information, you can select specific attributes and set the default values for each attribute. When you create a default template, it creates a default template record in the Templates \[sn\_ni\_core\_default\_template\] table. To learn more about the default templates, see [Network inventory templates](../concept/using-templates-tni.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Click the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Network Inventory Templates** &gt; **Default Templates**.

3.  Click **New**.

4.  On the form, fill in the general information to create a default template.

    To learn more about the fields, see [Default Template form](../reference/tni-default-template-form.md).

5.  Click **Save**.

6.  To schedule the form, click **Schedule** and fill in the Scheduled Entity Generation form.

    **Note:** Scheduling is only available in the classic environment.

    To learn more about the fields, see [Scheduled Entity Generation form](../reference/scheduled-entity-generation-form.md).


**Parent Topic:**[Create inventory template for network asset instantiation](../concept/preparing-inv-templates-network-asset-generation.md)

