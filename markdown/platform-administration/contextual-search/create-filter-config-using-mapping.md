---
title: Create a filter configuration using mapping
description: Create filter conditions using mapping that you can associate with a table configuration. The search result displays result that meets the filter conditions.
locale: en-US
release: xanadu
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Filter configuration for contextual search, Configuring contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a filter configuration using mapping

Create filter conditions using mapping that you can associate with a table configuration. The search result displays result that meets the filter conditions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Open a table configuration record on which to create the filter.

3.  In the Filter Configurations related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_upn_24t_dhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource configuration

</td><td>

Lookup icon ![Lookup icon to select a search context](../image/look-up-icon.png) to select a resource such as Knowledge Articles.

</td></tr><tr><td>

Table configuration

</td><td>

\[Read-only field\]. Table for which you are applying the filter configuration.

</td></tr><tr><td>

Scripted filter

</td><td>

Option to define the filter using a script.**Note:** Clear this option since you want to create a filter configuration using mapping.

</td></tr><tr><td>

Active

</td><td>

Option to activate the filter configuration.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The Table Configurations form appears.

6.  In the Filter Configuration related list, click the filter that you have created.

7.  In the Filter Conditions related list, click **New**.

    ![Filter conditions](../image/cxs-filter-conditions.png)

8.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Short description|Brief summary of the filter condition.|
    |Query table|\[Read-only\] Table from which the filter condition is queried.|
    |Current form|\[Read-only\] Form for which you created the filter conditions.|
    |Field to compare|Value of the field is compared with the value of the **Compare to** field.|
    |Operator|Operation that should be performed on the **Field to compare** and **Compare to** field.|
    |Compare to|Value of the field is compared against the value of **Field to compare**.|
    |Compare|Comparison of the field can be based on the actual value stored on the database or the value that is displayed on the interface. The available values are: **Value** and **Display Value**.|
    |Include if blank|Option to include a condition when the value of the **Compare to** field is blank.|
    |Active|Option to activate the filter configuration.|

9.  Click **Submit**.


**Parent Topic:**[Filter configuration for contextual search](../concept/filter-configuration-for-cxs.md)

