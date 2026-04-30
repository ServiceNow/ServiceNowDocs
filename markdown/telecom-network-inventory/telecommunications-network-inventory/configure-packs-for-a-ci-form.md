---
title: Configure an attribute pack table against a configuration item
description: Configure an attribute pack table against a configuration item \(CI\) with filter conditions in the Telecommunications Network Inventory application. As you configure the pack table, you can use the packs for creating a CI record.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Attribute pack table, Configure, Telecommunications Network Inventory]
---

# Configure an attribute pack table against a configuration item

Configure an attribute pack table against a configuration item \(CI\) with filter conditions in the Telecommunications Network Inventory application. As you configure the pack table, you can use the packs for creating a CI record.

## Before you begin

-   Make sure that the Attribute Pack plugin is installed with the Telecommunications Network Inventory application.
-   Create a pack table with a set of attributes. To learn more, see [Create attribute pack table](create-pack-table.md).

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

To use a pack table in the inventory forms, you must configure it against a CI with filter conditions. If the CI is related to another CI, you must set the filter conditions to map the pack table against the related CI.

## Procedure

1.  Navigate to **All** &gt; **Administration** &gt; **Pack Config**.

2.  Select **New**.

3.  On the **Details** tab, fill in the fields.

<table id="table_dpw_dy4_dyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the pack configuration.

</td></tr><tr><td>

Active

</td><td>

Option to enable the pack table in a CI record.

</td></tr><tr><td>

Configuration Item

</td><td>

CI table that you want to map.

</td></tr><tr><td>

Filter

</td><td>

Filter condition attributes to customize how your pack table is filtered so that you can use it in the CI form. Select **Set conditions** and enter the field operator and value for the filter condition.

</td></tr><tr><td>

Pack Table

</td><td>

Pack table that you want to map against the CI.

</td></tr><tr><td>

Has Related Configuration Item

</td><td>

Option to add related CI. When you select this check box, the following fields appear.-   **Related Configuration Item**

Related CI table that you want to map.

-   **Related Filter**

Filter condition attributes to customize how your pack table is filtered so that you can use them in the related CI form. Select **Set conditions** and enter the field operator and value for the filter condition.

**Note:** If the filter condition for the CI isn’t met, the system doesn't check filter conditions for the related CI. If the filter conditions of CI and related CI are met, the system maps the pack table against the related CI.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The pack table is mapped against the CI and is displayed in the Pack Config list.

## What to do next

Use the pack tables in the CI record. To learn more, see [Attribute pack in CI records](use-telecommunication-network-inventry-pack.md).

**Parent Topic:**[Attribute pack table](../concept/configuring-pack-table.md)

**Related topics**  


[Create attribute pack table](create-pack-table.md)

