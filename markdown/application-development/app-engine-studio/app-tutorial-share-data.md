---
title: Share data between tables
description: Share data between tables to avoid data duplication.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Building a data model, App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Share data between tables

Share data between tables to avoid data duplication.

## Before you begin

Role required: admin, sn\_app\_eng\_studio.user, or delegated developer

Select the following link to download the material needed for this step in the app creation tutorial.

[App creation tutorial airport spreadsheet](https://downloads.docs.servicenow.com/resource/enus/tutorial/app-tutorial-airports.xlsx)

## About this task

The final phase in building the data model for the employee travel request application is to link the travel request table to a separate table that stores airport data. Doing so enables employees to choose which airports they want to use when they complete employee travel requests.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Create a data table](app-tutorial-create-table.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Configure a data table](app-tutorial-configure-table.md)

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Share data between tables](app-tutorial-share-data.md)

</td></tr></tbody>
</table>Storing data in multiple tables enables you to keep your data organized and modular. When you want to share data between tables you can create reference fields, which pull records from one table into another without duplicating the data.

Download the airport spreadsheet and follow along with the tutorial to create references fields between the employee travel request and airport tables.

Fourth video in the app creation tutorial series. 

|Timestamp|Section|
|---------|-------|
|0:03|Create a table to store the data that you want to reference.|
|0:26|Configure the table.|
|1:05|Open your existing table.|
|1:13|Add new fields to the existing table.|
|1:19|Set the field type to **Reference** and select the table that you want to pull data from.|
|1:36|Save your changes.|
|1:38|Add the new reference fields to your table in **Form** view.|
|1:59|Customize the form layout.|
|2:10|Save your changes.|

## Procedure

1.  Create a new table to store airport information.

    In our tutorial, we create a new table from a spreadsheet that stores airport information. To follow along with the tutorial, [download the airport spreadsheet](https://downloads.docs.servicenow.com/resource/enus/tutorial/app-tutorial-airports.xlsx). Then use the procedures in [Import a spreadsheet](spreadsheet-importing-spreadsheet.md) and [Create new table from spreadsheet import](spreadsheet-create-new-table.md) to create a new table from the airport spreadsheet.

2.  Customize the table so that it displays the information that you want to reference.

    1.  Select the airport table from your application dashboard in App Engine Studio.

    2.  On the table landing page, select the More actions icon \(![More actions icon](../../../administer/ui-builder/image/three-dot-icon.png)\) next to **Data** in the top ribbon, then select **Fields**.

        ![Choose theFields data view to add and configure fields in your table.](../image/app-tutorial-connect-tables-data-fields.png)

    3.  On the **Fields** page, in the **Name** field, toggle on the **Display** switch \(![Toggle on.](../../../administer/form-builder/image/toggle-on.png)\) to enable other tables to reference airport names.

        **Important:** You can select only one field to be referenced by other tables. If you attempt to select multiple fields, Table Builder keeps only one of your selections when you save your changes.

    4.  Select **Save**.

3.  Navigate to your application dashboard in App Engine Studio.

4.  Select the employee travel request table, where you’ll create the reference fields that pull data from the airport table.

5.  On the table landing page, select the More actions icon \(![More actions icon](../../../administer/ui-builder/image/three-dot-icon.png)\) next to **Data**, then select **Fields**.

6.  Create the reference fields.

    In our tutorial, we create two reference fields to collect airport choices for employee travel requests.

    1.  On the **Fields** page, select **+ Add a field in the table**.

    2.  In the **Column label** field, enter `Travel From`.

        The **Column name** field auto-populates based on the label that you entered.

    3.  In the **Type** column, select **Reference**, then select the airport table from the list.

        In our tutorial, we create another reference field to capture where the employee is traveling to. We label this field `Travel To`.

7.  Select **Save**.

8.  Add the reference fields to the form view of the table.

    1.  Select **Forms** in the top ribbon.

    2.  Enter the label of the reference field in the **Search** bar.

        In our tutorial, the reference fields are labeled `Travel From` and `Travel To`.

        ![You can search for fields to add to your table in the search bar in the Add form elements panel.](../image/app-tutorial-search-add-form-elements.png)

    3.  Drag the reference fields from the **Add form elements** panel to the **Default view** panel.

9.  Repeat the process in steps 6–8 to add as many reference fields as you need.

10. Select **Save**.


## Result

The data model for the employee travel request application is complete.

## What to do next

Continue building the employee travel request application by proceeding to the next step in the app creation tutorial: [Creating user experiences](../concept/app-tutorial-experience-layer.md).

