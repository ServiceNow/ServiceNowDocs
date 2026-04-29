---
title: Create custom data lookups
description: Creating custom data lookups involves adding a lookup value, creating the definition, and activating data lookup.Create a custom table to store lookup data.The columns of a data lookup table contain both matcher and setter field data.Data lookup requires a definition record that specifies how to set one or more field values when specified conditions are met.You can create a module for data lookup so it appears in the instance application navigator.If the custom data lookup definition rules are not behaving as expected, check for certain conditions.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Data lookup and record matching support, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create custom data lookups

Creating custom data lookups involves adding a lookup value, creating the definition, and activating data lookup.

## Create a custom data lookup table

Create a custom table to store lookup data.

The custom table must extend the Data Lookup Matcher Rules `[dl_matcher]` table. For example, this custom lookup table stores information about VIP callers and incident assignments.

|Field|Sample value|
|-----|------------|
|Label|VIP Caller Lookup|
|Table name|u\_vip\_caller\_lookup|
|Extends base table|dl\_matcher|
|Create new module|True|
|Add module to menu|System Policy|

## Add a data lookup value to the data lookup table

The columns of a data lookup table contain both matcher and setter field data.

### About this task

Each data lookup is a query that searches for a row containing values that match the matcher fields. The data lookup then returns the value listed in the setter fields. For example, this Priority Data Lookup \[dl\_u\_priority\] table lists the combinations of impact and urgency \(matcher fields\) that produce a particular priority value \(setter field\).

|Matcher fields|Setter field|
|--------------|------------|
|Impact|Urgency|Priority|
|1 - High|1 - High|1 - Critical|
|1 - High|2 - Medium|2 - High|
|1 - High|3 - Low|3 - Moderate|
|2 - Medium|1 - High|2 - High|
|2 - Medium|2 - Medium|3 - Moderate|
|2 - Medium|3 - Low|4 - Low|
|3 - Low|1 - High|3 - Moderate|
|3 - Low|2 - Medium|4 - Low|
|3 - Low|3 - Low|5 - Planning|

### Procedure

1.  In the navigation filter, enter the name of the new custom lookup table.

    For example, u\_vip\_caller\_lookup.list.

2.  Configure the list and create new fields.

    For this example, create the new fields in the following table.

    |Name|Type|Field length or Table to reference|
    |----|----|----------------------------------|
    |Caller|Reference|User \[sys\_user\]|
    |Priority|Integer| |
    |Assignment Group|Reference|Group \[sys\_user\_group\]|

    For more information, see [Configuring lists on the ServiceNow AI Platform](../../list-administration/concept/c_ListConfiguration.md).

3.  From the table list, click **New** and enter appropriate matcher and setter field values.

    For example:

    |Matcher field|Setter fields|
    |-------------|-------------|
    |Caller|Priority|Assignment Group|
    |Beth Anglin|2|VIP Issues|
    |Fred Luddy|1|VIP Issues|

    ![Custom lookup values](../image/CustomLookupValues.png)

    **Note:** Each row in a data lookup table must be unique.


## Create a data lookup definition record

Data lookup requires a definition record that specifies how to set one or more field values when specified conditions are met.

### Before you begin

Role required: Admin

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Data Lookup Definitions**.

2.  Select **New**.

3.  Select **Data Lookup Rule**.

4.  Complete the Data Lookup Rule form using the following table.

<table id="table_qcb_2jk_t1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name to identify the definition record.

</td></tr><tr><td>

Source Table

</td><td>

Select the table containing the fields you want to automatically update with lookup values. Data Lookup Definitions are not inherited by extension tables. For example, a Data Lookup Definition on the Task table cannot match values on the Incident incident table.

</td></tr><tr><td>

Matcher Table

</td><td>

Select the table containing the lookup values. This table should always start with a u\_ prefix. This table can be any table within the current scope containing the lookup values.**Note:** The list shows only tables and database views that are in the same scope as the catalog data lookup definition.

</td></tr><tr><td>

Active

</td><td>

Select this check box to run this data lookup rule. Clear the check box to ignore this data lookup rule.

</td></tr><tr><td>

Run on form change

</td><td>

Select this check box to automatically look up values whenever a user or onChange client script changes a field value on a source table form.

 **Note:** This does not include changes automatically made by other data lookup rules, such as the Priority Lookup Rules.

</td></tr><tr><td>

Run on insert

</td><td>

Select this check box to automatically look up values whenever a user creates a new record.

</td></tr><tr><td>

Run on update

</td><td>

Select this check box to automatically look up values whenever a user saves or updates a record.

</td></tr></tbody>
</table>5.  Right-click the form header and select **Save**.

6.  From the **Matcher Field Definitions** related list, click **New**.

7.  Complete the Matcher Field Definitions using the following table.

    A data lookup only occurs on fields with matcher field definitions. The data lookup uses the values of the source table fields to look up one or more values from the matcher table. Note that data lookup does not work with **Journal** type fields.

<table id="table_avq_1qq_wq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Lookup

</td><td>

Displays the name of the parent data lookup definition record.

</td></tr><tr><td>

Source table field

</td><td>

Select the field from the source table that contains the data to match.

</td></tr><tr><td>

Matcher table field

</td><td>

Select the field from the matcher table that contains the data to match. This table can be any table within the current scope containing the lookup values.

</td></tr><tr><td>

Exact lookup match

</td><td>

Select this check box to require the matcher table to contain a matching row for every possible combination of values \(including blank values\). Clearing this check box means that any blank values in the matcher table match any value. For example, suppose the Priority field is blank in the matcher table. When this check box is selected, there is a match only when the Priority value is blank in the source table row. When this check box is cleared, the blank matcher field value matches any value in the source table field.

 **Note:** If the lookup does not require an exact match, matcher table rows containing blank values are treated as wild cards, matching all values.

</td></tr></tbody>
</table>8.  Select **Submit**.

9.  From the **Setter Field Definitions** related list, click **New**.

10. Complete the Setter Field Definitions form using the following table.

    |Field|Description|
    |-----|-----------|
    |Data Lookup|Displays the name of the parent data lookup definitions record.|
    |Source table field|Select the field from the source table that the data lookup updates.|
    |Matcher table field|Select the field from the matcher table that provides the new value for the update.|
    |Always replace|Select this check box to replace any existing value with a value from the data lookup. Clear this check box to ignore the update if the field has an existing value.|

11. Select **Submit**.

12. Select **Update**.

    For example, the following data lookup definition assigns incidents to the VIP Issues group based on the **Caller** field. In addition, the incidents are set to critical or high priority based on the caller.

    ![Data lookup definition](../image/DataLookupDefinition.png)


## Create a data lookup module

You can create a module for data lookup so it appears in the instance application navigator.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**, then select an application to add the module to.

2.  In the Modules related list, click **New**.

3.  Configure a module for the data lookup table you created using the following properties.

    |Property|Required value|
    |--------|--------------|
    |Table|Select the data lookup table you created in Step 2. For example u\_vip\_caller\_lookup.|
    |Link type|List of Records|

4.  Click **Submit**.


## Troubleshooting data lookup

If the custom data lookup definition rules are not behaving as expected, check for certain conditions.

-   Verify that the data lookup definition is set to run on the appropriate events.
-   Verify that the matcher field is not read-only. Because users cannot change read-only fields, user interactions cannot trigger an on form change event for read-only fields.
-   Verify a client script is not changing a field value. Client scripts can trigger **Run on form change** events even on read-only fields.
-   Verify that the data in the matcher table is correct.
-   If the lookup requires an exact match, verify that there is a matcher table row for each possible combination \(including blank values\). The lookup fails if cannot find a matching value.
-   Verify that you have not created a recursive rule, such as:

    If Field A = 1, then Field B =2. If Field B = 2, then Field A = 2.


