---
title: Create variable sets in Service Exchange for remote record producers
description: Create variable sets for a remote record producer in Service Exchange for Providers application.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using variable sets with Remote Record Producers, Remote record producers in Service Exchange, Create remote catalogs in Service Exchange for providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Create variable sets in Service Exchange for remote record producers

Create variable sets for a remote record producer in Service Exchange for Providers application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Click a record producer that you want to create variables for.

3.  Click the **Variable Sets** tab in the Related List and then click **New**.

4.  Select one of the following:

    -   Single-Row Variable Set: Creates a variable set with variables that are grouped together. Type field is set to `Single Row`.
    -   Multi-Row Variable Set: Creates a variable set with multiple rows that captures variable data in a grid layout. Type field is set to `Multi Row`.
5.  Fill in the fields on the form.

<table id="table_c2q_s1c_xq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of a variable set.

</td></tr><tr><td>

Internal name

</td><td>

Variable set name for internal use. If this field is left blank, it is auto-populated based on the Title field.

</td></tr><tr><td>

Order

</td><td>

Order number for the variable set.

</td></tr><tr><td>

Type

</td><td>

Type of the variable set. Possible choices are:-   Single Row
-   Multi Row


</td></tr><tr><td>

Application

</td><td>

Applications that can use this variable set.

</td></tr><tr><td>

Display title

</td><td>

If selected, adds a title and an expandable header to the right of the variable set.

</td></tr><tr><td>

Variable Set attributes

</td><td>

Attributes for configuring a multi-row variable set. Use the **max\_rows** attribute to set a limit to the number of rows that you can add to a multi-row variable set. For example, specify `max_rows=1` as the field value.

</td></tr><tr><td>

Layout

</td><td>

The layout display. Set to **1 Column Wide** or **2 Columns Wide, alternating sides** or **2 Columns Wide, one side, then the other**.

</td></tr><tr><td>

Description

</td><td>

Description of the variable set.

</td></tr></tbody>
</table>6.  Right-click and select **Save**.

7.  Create the variables to use in that set.

    1.  In the Variables related list, click **New**.

    2.  Follow the steps listed in [Create variables for remote record producers in Service Exchange for Providers](service-bridge-v2-assign-variables-ser-defn.md) to create variables.

        **Note:** For a multi-row variable set:

        -   The included variables are displayed as columns of a table.
        -   The column order is the order of variables defined in the variable set.
8.  Click **Submit**.

    Repeat the above steps to create additional variable sets for the same remote record producer.

    For more information on variable sets and the layout, see [Variable set layout](https://www.servicenow.com/docs/access?context=c_DefineVariableSetLayout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


