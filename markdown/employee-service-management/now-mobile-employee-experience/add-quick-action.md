---
title: Add a quick action in your mobile applications
description: Provide your users with a shortcut, which is also known as a quick action, to an item or action in your mobile apps. Quick actions appear on the applet launcher page.Provide easy access to an important item by creating a quick action. For example, you can create a quick action that opens a Service Catalog item.
locale: en-US
release: xanadu
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Now Mobile, Employee Service Management]
---

# Add a quick action in your mobile applications

Provide your users with a shortcut, which is also known as a quick action, to an item or action in your mobile apps. Quick actions appear on the applet launcher page.

## Before you begin

Role required: admin

## About this task

Demonstrates adding shortcuts, called quick actions, to applet launcher pages in the Now Mobile App.

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **Applet Launchers**.

2.  In the applet launchers \[sys\_sg\_applet\_launcher\] table, open the applet launcher record that you would like to add the catalog item to.

    For example, open the Homepage record to add the catalog item under the ![Plus icon](../image/more-items.png) icon on the home page.

3.  Select the **Body** tab.

4.  Add a record under the Quick Actions Menu Maps related list.

    If you're not able to insert a row, make sure that you're in the **ServiceNow Now Mobile App Screens and Applet Launcher** application scope.

5.  Add one of the quick actions from the following options.

    |Quick action|Description|
    |------------|-----------|
    |Report an Issue|Opens the **Create Incident** catalog item.|
    |Chat|Opens Agent Chat.|


## Result

Your users can open the quick action by selecting the ![Plus icon](../image/more-items.png) icon on the applet launcher page.

**Parent Topic:**[Configuring Now Mobile](../concept/setup-mobile-employee.md)

## Create a quick action in your mobile applications

Provide easy access to an important item by creating a quick action. For example, you can create a quick action that opens a Service Catalog item.

### Before you begin

Role required: admin

### Procedure

1.  Create a function for the quick action.

    1.  Navigate to **System Mobile** &gt; **Functions**.

        The Function \[sys\_sg\_button\] table opens.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_jzn_wnm_thb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the function record.

</td></tr><tr><td>

Description

</td><td>

Description to enable other users to easily understand the purpose of the function.

</td></tr><tr><td>

Type

</td><td>

Type of quick action that you want to create.

 To create a quick action that opens a Service Catalog item, select **URL**.

For more information about function types, see [Configure a smart button](https://www.servicenow.com/docs/access?context=sg-studio-config-smart-button&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

</td></tr><tr><td>

Context

</td><td>

Whether the function applies at the record or table level.-   Record: Action only applies at the record level. For example, updating a field.
-   Global: Action that only applies at the table level. For example, creating or deleting a record.
For this example, select **Global**.

</td></tr><tr><td>

Link Label

</td><td>

Label for the link. This value does not display in the user interface.

</td></tr><tr><td>

Link URL

</td><td>

Relative URL for the item that you want to open when the user clicks the function. For example, to open a Service Catalog item in the Now Mobile portal, enter `/mesp?id=sc_cat_item&sys_id=060f3afa3731300054b6a3549dbe5d3e`.

 This field only displays if the **Type** field is **URL**.

</td></tr><tr><td>

Relative URL

</td><td>

Option that is selected to determine whether the URL is relative. For this example, choose **Selected**.

 This field only displays if the **Type** field is **URL**.

</td></tr><tr><td class="sub-head" colspan="2">

Condition

</td></tr><tr><td>

Table

</td><td>

Table on which the condition runs.

</td></tr><tr><td>

Condition

</td><td>

Condition that should be met for the action to be successful. For a catalog item, enter `var item = new sn_sc.CatItem('3f1dd0320a0a0b99000a53f7604a2ef9'); answer = item.canView() && item.isVisibleServicePortal();` to display the quick action only when the end user has permissions to view the item.

</td></tr><tr><td>

Roles

</td><td>

Roles that you want to user to have to view the quick action.

</td></tr></tbody>
</table>2.  Add an instance of the function that you created to the page.

    1.  In the native UI, navigate to **Now Mobile App** &gt; **Applet Launchers**.

    2.  Open the applet launcher record that you would like to add the quick action to.

    3.  Select the **Body** tab.

    4.  Insert a new row in the Quick Actions Menu Maps related list.

        If you're not able to insert a row, make sure that you're in the **ServiceNow Now Mobile App Screens and Applet Launcher** application scope.

    5.  Click the magnifying glass to look up an item

        The Function Instances \[sys\_sg\_button\_instance\] table opens.

    6.  Click **New**.

    7.  On the form, fill in the fields.

<table id="table_kz4_kzj_vhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the function instance.

</td></tr><tr><td>

Description

</td><td>

Description to enable other users to easily understand the purpose of the function instance.

</td></tr><tr><td>

Parent

</td><td>

Page on which you are adding the quick action. For example, select **Applet Launcher: Homepage** to add the quick action to the home page. Select a value in the **Parent table** field first.

</td></tr><tr><td>

Application

</td><td>

Application scope.

</td></tr><tr><td>

Parent table

</td><td>

Table that contains the record type where the button appears. For this example, select **applet Launcher \[sys\_sg\_applet\_launcher\]** to add the quick action to an applet launcher page.

</td></tr><tr><td>

Function

</td><td>

Function record that you created earlier.

</td></tr><tr><td>

Label

</td><td>

Label to help the user understand what the quick action opens. For example, `Report an outage`.

</td></tr><tr><td>

Location

</td><td>

Location where the button appears in the UI. For this example, select **Quick Action**.

</td></tr><tr><td>

Icon

</td><td>

Icon to display next to the label. For more details on mobile icons, see [Mobile icons](https://www.servicenow.com/docs/access?context=sg-mobile-icon&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).**Note:** Not all listed icons work with quick actions. To see a list of compatible icons, filter your list where the **Icons** field contains `now-mobile-icons-buttons`.

 **Note:** The **Icons** field is not on the icon list by default. To add the **Icon** field to your list, right-click the list header and select **Configure** &gt; **List Layout**. Then, add the Icon field to the selected list. You should see the icon field on your reference field list.

</td></tr><tr><td>

Order

</td><td>

Number that indicates the order that the functions are listed. If there are multiple instances in the same location, the app displays them from the lowest to the highest.

</td></tr></tbody>
</table>    8.  Click **Submit**.

    9.  Save the applet launcher record.


### Result

Your users can open the quick action by selecting the ![Plus icon](../image/more-items.png) icon on the applet launcher page.

