---
title: Legacy - Add an application file to an application
description: Studio allows application developers to add new application files by type.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Add an application file to an application

Studio allows application developers to add new application files by type.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

This procedure requires creating a scoped application.

Role required: admin

## About this task

You can add application files to update the features of a custom application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  From the **Develop** tab, click the **Edit** button next to the application you want to modify.

    The system opens the application in the Studio.

3.  From the content frame, click **Create Application File**.

    You can also use a Studio keyboard shortcut.

<table id="table_ServiceNowStudioCreateNew"><thead><tr><th>

Keyboard combination

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Windows: Control+Shift+C

 Mac: Command+Shift+C

</td><td>

**Create New**. Create an application file.

</td></tr></tbody>
</table>    Studio opens the Create New Application File pop-up window.

    ![The Create New Application File pop-up window contains three elements: filter application file types, a list of application file types, and a content frame.](../image/CreateNewApplicationFile.png)

    **Note:** Not all application file types will display in Studio. Some types of application files needs to created outside Studio, such as dashboards, even though they extend sys\_metadata table.

4.  Find the application file type you want to create.

<table id="choicetable_fgn_dj2_2s"><tbody><tr><td id="d111241e237">

**Search by application file name**

</td><td>

In the **Filter** entry field, enter the name of the application file.

</td></tr><tr><td id="d111241e249">

**Search by category**

</td><td>

From the left pane, select a category name.

</td></tr></tbody>
</table>5.  From the results pane, select the application file type you want to create.

6.  Click **Create**.

    The system displays a blank form for the application file type in a new studio tab.


## What to do next

Enter the necessary fields for the particular application file type you selected.

**Parent Topic:**[Legacy - ServiceNow Studio](../concept/c_ServiceNowStudio.md)

**Related topics**  


[Application files](../concept/c_ApplicationFiles.md)

