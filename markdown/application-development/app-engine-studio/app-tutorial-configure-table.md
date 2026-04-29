---
title: Configure a data table
description: Configure a table to capture the necessary data for your application.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Building a data model, App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure a data table

Configure a table to capture the necessary data for your application.

## Before you begin

Role required: admin, sn\_app\_eng\_studio.user, or delegated developer

## About this task

The second phase in building the data model for the employee travel request application is to configure the table so that it collects the necessary data for employee travel requests, such as location, dates of travel, and estimated airfare.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Create a data table](app-tutorial-create-table.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Configure a data table](app-tutorial-configure-table.md)

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Close alert icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Share data between tables](app-tutorial-share-data.md)

</td></tr></tbody>
</table>This procedure covers the second part of the task demonstrated in the tutorial video. The first part of the procedure is outlined in the previous topic [Create a data table](app-tutorial-create-table.md).

Follow along to configure a table to store the necessary data for the employee travel request application.

Tutorial video that demonstrates how to create and configure a data table to capture the necessary data for your application. 

|Timestamp|Section|
|---------|-------|
|0:48|Begin editing your table.|
|0:54|Add and configure fields in your table.|
|2:32|Change the data form layout.|
|2:39|Save your changes.|

## Procedure

1.  Ensure that the employee travel request table is open.

    -   To open a table from your instance home page, navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**. Then select your application and select the table that you want to configure.
    -   To open a table that you have just created, select **Edit table**.
    When your table is open, it appears in the canvas space.

    ![When your table is open in the canvas, you can see the table name and configuration sections.](../image/app-tutorial-table-open.png)

2.  Select **Forms** in the top ribbon to change your view to **Forms** view.

    ![The table landing page contains different views in the top ribbon. The Forms view enables you to create your table as a form.](../image/app-tutorial-forms-view.png)

    **Forms** view enables you to create your table as a form. You can choose other views depending on the type of data that your table stores.

3.  Remove any unnecessary fields from your table by hovering over the field, then selecting the delete field icon \(![Delete form element.](../../../administer/form-builder/image/fb-delete-icon.png)\).

    **Note:** When you create a table from an extended table, the table comes with preconfigured fields. You can choose to keep or remove any preconfigured fields in your own table.

    In our tutorial, we remove the following fields:

    -   **Priority**
    -   **Configuration item**
    -   **Parent**
    -   **Assigned to**
4.  Select **Save**.

5.  Create new fields for your table.

    We must create several fields to collect details about employees' travel requests.

    1.  Select **+ Add a field in the table** in the **Add form elements** panel.

    2.  In the **Column label** field, enter `Departure Date`.

        **Tip:** The **Column name** field auto-populates based on the column label that you enter.

    3.  In the **Type** field, select **Date**.

    4.  To set additional properties for the field, select **Advanced settings**.

        We don’t set additional properties for the fields in our tutorial. For more information about field types and advanced settings, see [Field configuration in Table Builder](../../../administer/form-builder/reference/field-parameters.md).

    5.  Select **Add**.

    6.  Select **Add another one** to create additional fields.

    7.  Repeat the process in steps a-f to add as many fields as you need.

        We add more fields to collect additional information about employees' travel requests. The following table outlines the additional fields that we add to our table:

        |Column label|Type|
        |------------|----|
        |`Return Date`|Date|
        |`Estimated Airfare`|Decimal|
        |`Reason for Travel`|String|

    8.  When you have added all of the new fields that you need, select **Done**.

        The fields that you have added will appear in the **Add form elements** panel.

    9.  To add the fields to your form, select the fields, then drag them into the **Default view** panel with your existing fields.

        **Tip:** To add multiple fields to your table at once, hover over the field, select the check mark in each field, then drag the fields into the **Default view** panel.

        ![Select the fields that you want to add to the table by selecting the check mark next to each field. Then drag the selected fields into the Default view panel.](../image/app-tutorial-table-add-field.gif)

6.  Select **Save**.

7.  Add pre-existing fields to your table.

    1.  Search for the fields that you want to add by entering the names of the fields in the search bar.

        ![The search bar in the Add form elements panel enables you to search for available fields that you can add to your form.](../image/app-tutorial-search-add-form-elements.png)

        In our tutorial, we add the following fields to our table:

        -   `Approval`
        -   `Opened by`
    2.  Select the field in the **Add form elements** panel, then drag the field into the **Default view** panel.

8.  Change the layout of the form.

    1.  Select your table in the **Default view** panel.

        When selected, your table appears with a blue border.

        ![When you select a table in the Default view panel, the table appears with a blue border around it.](../image/app-tutorial-table-selected.png)

    2.  In the **Section** customization panel, select **One column**, then select **Two columns** to arrange the form fields evenly into a two-column layout.

        **Tip:** For more information about the customization options available in the **Section** panel, see [Customize your form layout in Table Builder](../../../administer/form-builder/task/customize-form-layout.md).

9.  Arrange the table fields into the order that you want them to appear by moving the fields.

    In our tutorial, we arrange the fields into the following order:

    1.  Number
    2.  Opened by
    3.  Departure Date
    4.  Return Date
    5.  Reason for Travel
    6.  Estimated Airfare
    7.  Approval
    8.  Status
10. Select **Save**.

11. Select **Preview** to review how your form appears.


## Result

Your table is configured to capture the necessary data for employee travel requests.

## What to do next

To complete the data model for the employee travel request application, we must connect the travel request table to a separate table that stores airport data. Proceed to the next step: [Share data between tables](app-tutorial-share-data.md).

