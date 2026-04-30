---
title: Create an attribute pack table
description: Create an attribute pack table with the attributes that you define in the Telecommunications Network Inventory application so that you can use these attributes in the CI record.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring an attribute pack table, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create an attribute pack table

Create an attribute pack table with the attributes that you define in the Telecommunications Network Inventory application so that you can use these attributes in the CI record.

## Before you begin

-   Make sure that the Attribute Pack plugin is installed with the Telecommunications Network Inventory application.
-   Switch the Application scope to Attribute Pack.

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

Create an attribute pack table with attributes by extending the Pack Base \(sn\_attribute\_pack\_base\) table. You define and store the attributes in the Pack base table. You can enable read or write permission for all application scopes.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Label|Name of the pack table.|
    |Name|Auto-populated name that is based on the label name that you selected \(sn\_attribute\_pack\_&lt;label name&gt;\).|
    |Extends table|Pack \(sn\_attribute\_pack\_base\)|

4.  On the **Controls** tab, add the roles in the **User Role** field.

    You add the roles to grant the access to the pack table.

5.  Select **Save**.

6.  Add or delete attributes.

7.  Select **Submit**.


## Result

The pack table is created with a set of attributes.

## What to do next

To use the pack table in inventory forms, you must configure it to map with the inventory objects. To learn more, see [Configure an attribute pack table against a configuration item](configure-packs-for-a-ci-form.md).

**Parent Topic:**[Configuring an attribute pack table](../concept/configuring-pack-table.md)

**Related topics**  


[Configure an attribute pack table against a configuration item](configure-packs-for-a-ci-form.md)

