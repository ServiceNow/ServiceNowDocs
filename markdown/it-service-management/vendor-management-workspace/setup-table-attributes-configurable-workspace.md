---
title: Set up table attributes in Vendor Management Workspace
description: Configure attributes for a table to compare them with top-performing vendors.
locale: en-US
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up Vendor Success Indicators in Vendor Management Workspace, Configure, Vendor Management Workspace, IT Service Management]
---

# Set up table attributes in Vendor Management Workspace

Configure attributes for a table to compare them with top-performing vendors.

## Before you begin

Role required: sn\_vlm.vendor\_admin

## About this task

The fields for a selected table display all supported string and numeric data types. The allowed data types are defined in the **sn\_app\_ml\_insights.attr\_datatype\_inclusion\_list** system property. For more information, see [Properties installed with Vendor Success Indicators](../reference/installed-w-vendor-manager-configurable-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Success Indicators** &gt; **Attributes**.

2.  Click **New**.

3.  In the **Name** field, enter a unique name for the evaluating attribute.

4.  In the **Type** field, select **Table**.

5.  Set up the field attributes.

<table id="choicetable_tvq_1b2_lnb"><thead><tr><th align="left" id="d45698e123">

To configure attributes for

</th><th align="left" id="d45698e126">

Do this

</th></tr></thead><tbody><tr><td id="d45698e132">

**The Company \[core\_company\] table**

</td><td>

In the **Configuration** section, select Company \[core\_company\] from the Table list. This table is the same as the base evaluating table.-   For configuring a field that has a string datatype:
    1.  From the **Field Name** list, select the string datatype, for example, Country. A pop-up shows the number of distinct values available for this field. You can categorize these values based on how you want to evaluate your vendors.

**Note:** Set the number of string datatype values you want to allow before you categorize them using the **sn\_app\_ml\_insights.attr\_category\_string\_value\_limit** system property. For more information, see [Properties installed with Vendor Success Indicators](../reference/installed-w-vendor-manager-configurable-workspace.md).

    2.  Right-click the form header and click **Save**.
    3.  In the Success Indicator Attribute Categories related list, click **New**.
        1.  In the **Category** field, enter the name to group a set of attribute values.
        2.  In the **Field Value** field, move the desired fields to the **Selected** list.
        3.  Click **Submit**.

**Note:** Repeat this step to add each category for the selected field.

    4.  Click **Update**. The attribute is added to the **Success Indicator Attribute** list.
-   For configuring a field that has a numeric datatype:
    1.  From the **Field name** list, select the numeric datatype, for example Relationship Start Date.
    2.  Click **Submit**.

**Note:** The **Upper Threshold \(Age in Days\)**, **Lower Threshold \(Age in Days\)**, and **Direction** fields are populated automatically. If you select a numeric field type with a date value, the application calculates the number of days between the threshold values and represents them as age.

</td></tr><tr><td id="d45698e246">

**Any table other than the Company \[core\_company\] table**

</td><td>

1.  In the **Configuration** section, select any table other than Company \[core\_company\] from the Table list.
2.  From the **Field Name** list, select a field.
3.  From the **Collection Type** field, select one of the following:

    -   Field Value: Calculates the actual value for the selected field.

**Note:** If the selected field is a numeric type, the **Upper Threshold**, **Lower Threshold**, and **Direction** fields are populated automatically.

    -   Record Count: Counts the number of records with valid values that match the conditions defined in the **Normalization Script** field.
The application sets the relationship between the base evaluating table and the table used for selecting the attribute using the **sourceIDField** and **encodedQuery** fields.

4.  Click **Submit**.


</td></tr></tbody>
</table>
## Example

Example 1: In the example configuration shown in the following image:

-   The table used for configuring the vendor success attributes is the same as the base table, Company \[core\_company\].
-   The field name selected, which is Country, is a string data type.

The pop-up message shows that the attribute Country has nine distinct values.

The nine values for Country are Germany, Ireland, Switzerland, Israel, Japan, South Korea, Canada, U.S., and USA. You have the option of configuring the attributes for Country by grouping them into categories such as EMEA, APAC, and AMS.

![Success Indicator String Type](../image/success-indicator-string-type.png)

Example 2: In the example configuration shown in the following image:

-   The table used for configuring the vendor success attributes is not the same as the base table, Company \[core\_company\].
-   The field selected for setting attributes has the numeric data type, **sourceId**. ![Success Indicator - Numeric Type](../image/success-indicator-numeric-type.png)

