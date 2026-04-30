---
title: Trigger offline cache download
description: Trigger offline cache download is an optional button attribute \(sys\_sg\_button\_atribute\_name\) that will generate an offline cache after a successful completion of the assigned writeback action.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure offline mode properties for action functions, Offline mode, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Trigger offline cache download

**Trigger offline cache download** is an optional button attribute \(**sys\_sg\_button\_atribute\_name**\) that will generate an offline cache after a successful completion of the assigned writeback action.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu and then select the function to which you want to add this behavior.

4.  Ensure the **Type** field is set to **Action item**.

5.  In the **Button attributes** section, select an existing button attribute record or select **New** to create one.

6.  In the Button attribute form, complete the following fields.

<table id="table_gmp_dvn_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Button

</td><td>

Select the action that will trigger the offline cache download. Only buttons with their **Type** set to **Action item** can be associated with this attribute.

</td></tr><tr><td>

Name

</td><td>

The attribute name. Select **trigger\_offline\_cache\_download**.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following values:-   Enter `true` to enable the offline cache download.
-   Enter `false` to disable the offline cache download.
-   Leave the value blank to use the default value.
**Note:** By default, the **Trigger offline cache download** value is blank.

</td></tr></tbody>
</table>7.  Select **Save**.


**Parent Topic:**[Configure offline mode properties for action functions](config-offline-properties-action-funct.md)

