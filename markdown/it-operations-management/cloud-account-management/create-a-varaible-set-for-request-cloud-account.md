---
title: Create a variable set for Request cloud account catalog
description: Customize the Request cloud account catalog by creating or editing variable sets. A variable set groups related variables into a single, reusable collection. Select only the necessary variables for specific cloud account requests to ensure a streamlined and uniform process.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 1
breadcrumb: [Setting up Cloud Account Management in Cloud Workspace, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a variable set for Request cloud account catalog

Customize the Request cloud account catalog by creating or editing variable sets. A variable set groups related variables into a single, reusable collection. Select only the necessary variables for specific cloud account requests to ensure a streamlined and uniform process.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Workspace**.

2.  Enter `sc_cat_item.LIST` in the navigation filter.

3.  In the sc\_cat\_item.LIST table, search for and click the **Request Cloud Account** property.

4.  Click the **Variable Sets** tab and click **New**.

    The Variable Set screen appears.

5.  Fill in the form details \(as shown in the table\).

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
</table>6.  Click **Submit**.

    The new variable set is created and appears in the **Variable Sets** tab. Open the new variable set and click **New** in the **Cloud Variables** tab to create variables for the set.


