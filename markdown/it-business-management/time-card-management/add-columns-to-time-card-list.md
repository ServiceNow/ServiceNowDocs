---
title: Add columns to the logged time card list
description: Add columns in the logged time card list on the Time Sheet Portal to show additional information that you might require to log your time cards.
locale: en-US
release: xanadu
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Time Sheet Portal, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add columns to the logged time card list

Add columns in the logged time card list on the Time Sheet Portal to show additional information that you might require to log your time cards.

## Before you begin

Role required: admin or sp\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widget Instances**.

2.  Search the Widget column for **Time Card Portal Main Container** and open the record.

3.  On the Instance form, update the code by providing values for the following column configurations in the **Additional options, JSON format** field.

<table id="table_omw_fk1_zhb"><thead><tr><th>

Column configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Name of the column in a table.

</td></tr><tr><td>

label

</td><td>

Column name to display in the logged time card list on the Time Sheet Portal.

 The configuration is mandatory if you are adding a column of a table other than the Time Card \[time\_card\] table.

</td></tr><tr><td>

width\_in\_percent

</td><td>

Column width in percentage in the logged time card list.

</td></tr></tbody>
</table>    **Note:** To add more than one column, separate each column configuration with a comma. The columns are added in the same order as you add them in the code.

4.  Click **Update**.


## Example

The following sample code adds the **category** column of the Time Card \[time\_card\] table with the column name **Category** and width of 10% in the logged time card list on the Time Sheet Portal.

```
{
  "tm_grid_options": {
    "displayValue": "Time card grid options",
    "value": {
      "header_fields": [
        {name:"category",label:'Category', width_in_percent: 10}
      ]
    }
  }
}
```

**Parent Topic:**[Time Sheet Portal](../concept/worker-portal.md)

