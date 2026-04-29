---
title: Create a catalog lookup definition
description: Create a catalog data lookup definition record.The columns of a data lookup table contain both matcher and setter field data. Each data lookup is a query that searches for a row containing values that match the matcher fields.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service catalog data lookup, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a catalog lookup definition

Create a catalog data lookup definition record.

## Before you begin

Role required: admin or catalog\_admin

## About this task

**Note:** The Run on Insert and Run on Update options are not supported for catalog data lookups. Other options operate the same as for normal data lookup.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Data Lookup Definitions**.

2.  Click **New**.

3.  Select **Catalog Data Lookup Rule**.

4.  Enter a Name.

5.  In Applies to, select catalog item or variable set.

6.  In Catalog item/Variable set, select a specific item or set.

7.  Select a **Matcher Table**.

8.  Select other options, as required.

9.  Right-click the form header and click **Save**.

10. From the Catalog Matcher Variable Definitions related list, click **New**.

11. Fill in the fields, as appropriate.

<table id="table_pvt_231_dbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name to identify the definition record.

</td></tr><tr><td>

Applies to

</td><td>

Select what the data lookup rule applies to: a catalog item or a variable set.

</td></tr><tr><td>

Catalog item/Variable Set

</td><td>

Select the catalog item or variable set to which the data lookup rule applies.

</td></tr><tr><td>

Matcher Table

</td><td>

Any table within the current scope containing the lookup values.

**Note:** The list shows only tables and database views that are in the same scope as the catalog data lookup definition.

</td></tr><tr><td>

Active

</td><td>

Select this check box to run this catalog data lookup rule. Clear the check box to ignore this catalog data lookup rule.

</td></tr><tr><td>

Run on form change

</td><td>

Select this check box to automatically look up values whenever a user changes a variable value on a catalog item or form. This option is the only supported method for catalog data lookup rules.

 **Note:** This option does not include changes automatically made by other data lookup rules, such as the priority lookup rules.

</td></tr></tbody>
</table>12. Click **Submit**.

13. From the Catalog Setter Variable Definitions related list, click **New**.

14. Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Data Lookup|Displays the name of the parent data lookup definitions record.|
    |Source variable field|Select the variable from the source item or variable set that the data lookup updates.|
    |Matcher table field|Select the field from the matcher table that provides the new value for the update.|
    |Always replace|Select this check box to replace any existing value with a value from the data lookup. Clear this check box to ignore the update if the field has an existing value.|

15. Click **Submit**.

16. Click **Update**.


**Parent Topic:**[Service catalog data lookup](../concept/c_ServiceCatalogDataLookup.md)

## Add a data lookup value

The columns of a data lookup table contain both matcher and setter field data. Each data lookup is a query that searches for a row containing values that match the matcher fields.

### Before you begin

Role required: catalog\_lookup\_admin

### About this task

The data lookup then returns the value listed in the setter fields.

For example, you can define the matching settings for bronze, silver, and gold offerings as described previously.

### Procedure

1.  In the navigation filter, enter the name of the new custom lookup table.

2.  Configure the list and create appropriate fields for the lookup table.

3.  From the table list, click **New** and enter appropriate matcher and setter field values.

    For example:

    ![Service Catalog lookup 1.](../image/ServiceCatalogLookup1.png "Service Catalog lookup 1")

    **Note:** Each row in a data lookup table must be unique.


