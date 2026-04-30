---
title: Configure a standard data item
description: Configure a standard data item to query data for your screens that do not require parameter input.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a standard data item

Configure a standard data item to query data for your screens that do not require parameter input.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the Data category, and then select **New**.

4.  Select Data item and then select **Continue**.

5.  In the Data Items tab, click **Create New**.

6.  Complete the following fields as needed.

<table id="table_cbg_pzm_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Properties section:**

</td><td>

 

</td></tr><tr><td>

Name

</td><td>

A title for the data item. You can have multiple data items with the same name. Make sure that this name is unique so that you can find it easily.

</td></tr><tr><td>

Description

</td><td>

Optional additional details about the data item.

</td></tr><tr><td>

**Data section:**

</td><td>

 

</td></tr><tr><td>

Table

</td><td>

The table you want the data item to pull information from.**Note:** Custom tables are not available by default. You can change this behavior by modifying the **subscription.custom\_table.enforce\_entitlement** system property. For details on making this change, see [Allow or restrict access to custom tables in mobile data items](sg-allow-custom-tables.md).

</td></tr><tr><td>

Group by

</td><td>

Groups query results based on the selected field from the menu.

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

</td></tr></tbody>
</table>7.  If you have selected **Scripted** in the **Condition type** field, you must create a script in the **Query Condition Script** field.

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

8.  Select **Save**.


## What to do next

Associate a data item with a screen. For more information, see [Mobile screen types](../concept/sg-mobile-applet.md).

**Related topics**  


[Configure a parametrized data item](sg-config-parametrized-data-item.md)

[Configure a group by data item](sg-create-group-data-item.md)

