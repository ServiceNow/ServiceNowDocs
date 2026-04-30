---
title: Configure data sources
description: Configure data sources to map UI elements to specific database fields using element identifiers, enabling the retrieval and display of data on input form screens. This mapping verifies that each UI element accurately reflects the corresponding data field within a record.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 1
breadcrumb: [Data sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure data sources

Configure data sources to map UI elements to specific database fields using element identifiers, enabling the retrieval and display of data on input form screens. This mapping verifies that each UI element accurately reflects the corresponding data field within a record.

## Before you begin

Role required: admin

## About this task

To create a data source, you establish uniquely named element identifiers and select the table you want to filter, such as an incident or change request table. The data source provides a framework for mapping fields from the selected table to element identifiers in the user interface. For example, you might map the short\_description field to an element identifier named short\_description. This mapping ensures that the data from a specified field is correctly displayed in the user interface.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **All mobile records** from the menu.

4.  From the **Record type** field, select **Data source \[sys\_sg\_data\_source\]** and then select **New**.

5.  Add a name for your data source in the **Name** field.

6.  Add any additional information about this data source in the **Description** field.

7.  Edit the script in the **Data source script** field as required.

    For examples of data source script, see [Data source script examples](../reference/data-source-script-examples.md).

8.  Select **Save**.


