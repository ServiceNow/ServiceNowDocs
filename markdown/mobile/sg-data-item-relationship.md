---
title: Configure a relationship data item for an embedded list
description: Configure relationship data items so you can control the information that appears in embedded lists within a record screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a relationship data item for an embedded list

Configure relationship data items so you can control the information that appears in embedded lists within a record screen.

## Before you begin

Role required: admin

## About this task

A relationship data item is required to create an embedded list. Embedded lists are lists that can be embedded within a record screen. For more information on embedded lists in mobile, see [Embedded lists for a record screen](../concept/sg-embedded-list.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Data** category from the menu, and then select **New**.

4.  Select the **Relationship data item** icon, and then select **Continue**.

5.  Complete the following fields as needed.

<table id="table_cbg_pzm_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties section:**

</td></tr><tr><td>

Name

</td><td>

A title for the data item. You can have multiple data items with the same name. Make sure that this name is unique so that you can find it easily.

</td></tr><tr><td>

Description

</td><td>

Optional additional details about the data item.

</td></tr><tr><td colspan="2">

**Data section:**

</td></tr><tr><td>

Table

</td><td>

The table you want the data item to pull information from. This table is the table of records that is embedded as list on the parent record screen.**Note:** Custom tables are not available by default. You can change this behavior by modifying the **subscription.custom\_table.enforce\_entitlement** system property. For details on making this change, see [Allow or restrict access to custom tables in mobile data items](sg-allow-custom-tables.md).

</td></tr><tr><td>

Group by

</td><td>

Groups query results based on the selected field from the menu.

</td></tr><tr><td>

Table related to

</td><td>

Table that the records in this data item are related to. For example, for a list of Task SLA records embedded into a task record screen, the **Tables related to**value would be the `Task` table.

</td></tr><tr><td>

Relationship

</td><td>

Relationship between the table selected in the **Table** field and the table selected in the **Table related to** field.

</td></tr><tr><td>

Condition type

</td><td>

Determines what type of condition your data item uses. Select from: -   **Declarative**

Use a declarative condition to create conditions for the data item using the condition builder.

-   **Scripted**

Use a script to determine the conditions of your data item. A text window to enter a script appears below this field when you select this option.

-   **Append Encoded Query**

Use this option only when creating data items for your chart screens. For details on that data item type, see [Configure an encoded query data item for chart screens](sg-relative-url-data-item.md).

</td></tr><tr><td>

Condition

</td><td>

Set of conditions for the data item to conform to. You can create conditions using the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).**Note:** This field is only available when you select `Declarative` in the **Condition type** field.

</td></tr><tr><td>

Sort by

</td><td>

Lets you adds fields to the form that allow you to configure how to sort the list. In the condition builder, select the field you want the list to be sorted by. For example, select `Caller`. Then select `ascending` or `descending` to determine the order of the list.**Note:** This field is only available when you select `Declarative` in the **Condition type** field.

</td></tr><tr><td>

Parameters

</td><td>

**Note:** The Parameters field must not be used for relationship data items.

</td></tr></tbody>
</table>6.  If you have selected **Scripted** in the **Condition type** field, you must create a script in the **Query Condition Script** field.

    Your scripted condition must return a query string, which the instance uses to filter the data item. Use the `input` variable to access information from the current record.

    ```
    (function getQueryString(input) {
    	var queryString = '';
    	if(input.company) {
    		  queryString += "company="+input.company;
    	 }
    	if(input.location) {
    	  queryString += "^location="+input.location;
    	 }
            queryString += "^EQ^ORDERBYDESCsys_updated_on";
    	 return queryString; 
     })(input);
    ```

    This example uses the `input` variable and filters the data item for records matching the current records company and location. It then appends the text `^EQ^ORDERBYDESCsys_updated_on` to the query, which sorts the data item records by the **Updated on** field.

    **Note:** The `input` variable provides mobile scripts access to values that are passed in the SubmittedForm or the ParameterData objects.

7.  Select **Save**.


## What to do next

After creating a relationship data item, create a list screen using this newly created data item. For more information, see [List screen configuration](sg-configure-list-screen.md).

