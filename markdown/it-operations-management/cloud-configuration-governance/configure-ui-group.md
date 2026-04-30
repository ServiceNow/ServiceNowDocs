---
title: Create a variable set for Cloud Provisioning and Governance
description: Reduce the number of steps required to create and manage multiple catalog items and order guides by creating variable sets. With variable sets, you don't have to create variables individually for each catalog item.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a variable set for Cloud Provisioning and Governance

Reduce the number of steps required to create and manage multiple catalog items and order guides by creating variable sets. With variable sets, you don't have to create variables individually for each catalog item.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## About this task

Create a collection of structured variables that can be reused across multiple catalog items and order guides using variable sets.

A new variable set will be relevant to add when there are specific request form variables needed for running actions such as a post-provisioning action or for collecting additional information such as custom tags.

You can modify the variable set and the changes are reflected across all the catalog items that are associated with the variable set. Variable sets also allow you to define catalog client scripts and UI policies that are applicable to the variables in the set.

When you generate a catalog item, two variable sets, **General Info** and **Provision**, are automatically created. Create as many variable sets as needed.

## Procedure

1.  Open a cloud catalog item and in the **Variable Sets** tab, click **New**.

    The Variable Set screen appears.

2.  Fill in the form details \(as shown in the table\).

<table id="table_rd1_4sf_pfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Unique name for the variable set

</td></tr><tr><td>

Internal Name

</td><td>

A \(unique\) variable set name for internal use. **Note:** If this field is empty, its value is auto-populated based on the **Title** field for all variable types except break, container split, and container end.

</td></tr><tr><td>

Layout

</td><td>

Layout display selections from: **1 Column Wide**, **2 Columns Wide alternating sides**, or **2 Columns Wide, one side, then the other**.

</td></tr><tr><td>

Order

</td><td>

Order number for the variable set.

</td></tr><tr><td>

Description

</td><td>

Description for the variable set.

</td></tr></tbody>
</table>3.  Click **Submit**.

    The new variable set is created and appears in the **Variable Sets** tab. Open the new variable set and click **New** in the **Cloud Variables** tab to create variables for the set.


