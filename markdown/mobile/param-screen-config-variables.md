---
title: Configure input form screen variables and attributes
description: Use screen variables to collect information from the user automatically or define default information. Variables can include information like user IDs and GPS coordinates.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form screen variables and attributes

Use screen variables to collect information from the user automatically or define default information. Variables can include information like user IDs and GPS coordinates.

## Before you begin

You must create an input form screen before you create variables and attributes. For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select the input form screen for which you want to configure variables.

4.  Scroll down to the Variables section of the form, and select **New** to create a variable.

    The Variable form appears.

5.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your variable|
    |Variable type|
    |Database field|Data from a field. This field uses the **FieldName** attribute. After configuring the **Variable placement** section, see Step 6 to configure the attribute.|
    |Date|Current date. This variable does not take an attribute. After configuring the **Variable placement** section, see Step 8 to finish the variable configuration.|
    |Constant|A static value set by the administrator using the **ConstantValue** attribute. After configuring the **Variable placement** section, see Step 6 to configure the attribute.|
    |GPS Coordinates|Longitude and latitude of the user. This variable does not take an attribute. After configuring the **Variable placement** section, see Step 8 to finish the variable configuration.|
    |Offline Mode|Input is available when the mobile app is offline. This variable does not take an attribute. After configuring the **Variable placement** section, see Step 8 to finish the variable configuration.|
    |User|Sys\_id of the user. This variable does not take an attribute. After configuring the **Variable placement** section, see Step 8 to finish the variable configuration.|
    |ParentContext|Context information that is carried from a parent record into an action. Uses the **ContextField** attribute. After configuring **Variable placement**, see Step 7 to configure the variable and attribute.|
    |Scripted|Script that auto-fills inputs. Uses the **Script** attribute. After configuring the **Variable placement** section, see Step 7 to configure the variable and attribute.|
    |Variable placement|
    |Input form screen|Select the input form screen where the variable appears.|
    |Input form section|Select the input form section where the variable appears. If the input form screen does not contain sections, this field is not available.|

6.  If you selected **Database field** or **Constant** as your variable type, the Variable attributes section appears.

    In the Variable attributes section, select **New** to configure the variable attribute. Depending on the variable type you set in Step 5, select the attribute properties.

<table id="table_if5_ppt_gtb"><thead><tr><th>

Attribute name

</th><th>

Properties

</th></tr></thead><tbody><tr><td>

FieldName

</td><td>

Set the following information:-   **Table**: The table you want to use.
-   **Value**: The name of the field in that table.
 Use this attribute if you have selected the **Database field** variable type.

 See Step 8 to finish the variable configuration.

</td></tr><tr><td>

ConstantValue

</td><td>

Enter the static data defined by the administrator. Use this attribute if you have selected the **Constant** variable type.

 See Step 8 to finish the variable configuration.

</td></tr></tbody>
</table>7.  If you want to configure ParentContext or Scripted variable types, then do the following:

    1.  Save the input form screen by selecting **Save**.

    2.  Navigate back to the input form screen node in the left navigation menu.

    3.  On the input form screen form, select the options menu icon ![Options menu icon.](../image/mab-option-menu.png) in the upper right corner of the form in Mobile App Builder, and select **Open in platform**.

    4.  Select the Variables tab.

    5.  Under Name, select the name you entered for the variable in Step 5.

    6.  Select one of the following Variable Types.

        |Variable Type|Description|
        |-------------|-----------|
        |ParentContext|Context information that is carried from a parent record into an action. This type uses the **ContextField** attribute. For example, use this variable when an employee goes out on a service call and they must log associated expenses like mileage.|
        |Scripted|Script that auto-fills inputs. This type uses the **Script** attribute. For example, you can pre-fill a building number based on an end user's profile when making a reservation.|

    7.  In the Attributes section under Name, double-click **Insert a new row…** and enter the name of your variable attribute as listed in the following table.

        **Important:** Enter the Attribute Name exactly as it is listed in the table. The name is case-sensitive.

<table id="table_zlh_nwv_qtb"><thead><tr><th>

Attribute Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ContextField

</td><td>

Enter this attribute name for ParentContext variables.**Note:** Enter the attribute name exactly. It is case-sensitive.

</td></tr><tr><td>

Script

</td><td>

Enter this attribute name for Scripted variables.**Note:** Enter the attribute name exactly. It is case-sensitive.

</td></tr></tbody>
</table>    8.  After entering the attribute name, select the check \(![Check icon.](../image/green-check-mark.png)\) to save the attribute.

    9.  Double-click the field under Value and add the appropriate value for the attribute you are configuring as described in the following table.

        |Attribute Name|Description|
        |--------------|-----------|
        |ContextField|Enter the field name from the parent screen whose contents you want to populate the input form screen field.|
        |Script|Paste the JavaScript code that auto-fills the input form screen field. For example, you can pre-fill a building number based on an end user's profile when making a reservation.|

    10. Select the check icon \(![Check icon.](../image/green-check-mark.png)\) to save attribute.

    11. Select **Update**.

    12. Navigate back to Mobile App Builder by selecting that browser tab.

8.  In Mobile App Builder, select **Save**.

    **Important:** If you performed optional Step 7, you already saved the record in Mobile App Builder so you don't need to save it again.


## What to do next

After you have created your input form screen variables, you can map these variables to input form screen inputs or action items. For details on this process, see [Configure an action item](sg-studio-create-action-item.md).

