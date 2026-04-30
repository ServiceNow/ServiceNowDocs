---
title: Create or edit an EVAM view definition
description: Create or edit an Entity View Action Mapper \(EVAM\) view definition in the AI Search Admin console to customize how your AI Search results are displayed in the portal or workspace.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Customizing the result-card interface in AI Search by using EVAM, Using AI SearchAdmin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create or edit an EVAM view definition

Create or edit an Entity View Action Mapper \(EVAM\) view definition in the AI Search Admin console to customize how your AI Search results are displayed in the portal or workspace.

## Before you begin

Role required: admin or ais\_admin

## About this task

An EVAM is a data source type tool that helps standardize how data is displayed in lists and cards. An EVAM enables users to combine data from multiple sources, configure views for each source, and navigate through large data sets. By creating or editing an EVAM definition, you can combine the conditions, fields, and declarative actions with an associated view template to customize the result-card interface to your needs.

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the application card that you want to create or edit the EVAM configurations for.

3.  On the sidebar tab, select **Result-card Interface**.

    The result-card Interface shows the EVAM definition if it’s already configured. You can modify the existing EVAM definition or if you’re configuring your application for the first time, you can add a new EVAM definition. For more information, see step 4.

    ![Result-card interface of the search application in the AI Search Admin console where you can change the EVAM definition if needed.](../image/evam-definition-ais.png)

4.  Update an existing EVAM definition or add a new definition.

    -   To update the existing EVAM definition for the result-card interface, select **Change**.
    -   To add a new EVAM definition and configure the result-card interface for the first time, select **Choose**.
    1.  Create or update an EVAM definition for the result-card interface.

        ![Choose result card interface dialog box in the AI Search Admin console, where you can either select an existing result card interface or create a new interface for the search application.](../image/result-crad-interface-for-evam-definitin.png)

<table id="table_rq1_hrd_1dc"><thead><tr><th>

Option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Select from the existing result-card interfaces for your search application

</td><td>

1.  Select **Use an existing result-card interface**.
2.  From the Result card interface list, select an option.


</td></tr><tr><td>

Add a new result-card interface for your search application

</td><td>

1.  Select **Create new interface**.
2.  In the **Configuration name** field, enter the name.


</td></tr></tbody>
</table>    2.  Select **Save**.

5.  From the Select a bundle to edit list, select an EVAM configuration bundle.

    You can link more bundles to the selected EVAM definition by selecting **Advanced configuration**. For more information, see [Create an EVAM definition](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    The list of view configurations that are associated with the selected bundle are displayed.

6.  Manage the EVAM view configuration.

<table id="choicetable_s32_yx1_cdc"><thead><tr><th align="left" id="d374945e252">

Option

</th><th align="left" id="d374945e255">

Procedure

</th></tr></thead><tbody><tr><td id="d374945e261">

**Create an EVAM view configuration**

</td><td>

1.  Select **Create New**.
2.  In the Create new view config dialog box, review the auto-populated values, and then select **Create**.


</td></tr><tr><td id="d374945e285">

**Edit the existing EVAM view configuration**

</td><td>

1.  From the View configs list, identify an EVAM view configuration that you want to edit.
2.  Select the More Actions icon \(![](../../localization-framework/image/more-actions-icon.png)\) and then select **Edit**.


</td></tr></tbody>
</table>7.  On the form, fill in the fields.

    For a description of the field values, see [Edit view config form](../reference/ais-edit-view-config-form.md).

8.  In the Preview Card section, review the auto-generated JSON to verify the edits that you made to the view configuration.

    The following example shows the Edit view config form that helps you review the layout of your result-card interface in the Preview Card section.

    ![Edit view config form showing the preview card.](../image/edit-view-config1.png "Edit view config form")

9.  Select **Save**.


## Result

Changes made to search result EVAM cards take effect immediately in AI Search applications.

## What to do next

After creating a view configuration, you must activate it. For more information, see [Activate or deactivate an EVAM view configuration](enable-evam-config-ais-admin-console.md).

**Parent Topic:**[Customizing the result-card interface in AI Search by using EVAM](../concept/ais-admin-console-managing-evam.md)

