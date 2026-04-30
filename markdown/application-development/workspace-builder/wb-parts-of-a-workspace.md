---
title: Parts of a workspace in Workspace Builder
description: Every workspace has parts that enable workspace users to complete their tasks.
locale: en-US
release: zurich
product: Workspace Builder
classification: workspace-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Parts of a workspace in Workspace Builder

Every workspace has parts that enable workspace users to complete their tasks.

Build your workspace by including the following pages and elements.

<table id="table_zs3_tzv_15b"><thead><tr><th>

Component

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Home

</td><td>

Landing page for the workspace, which contains a dashboard and appears to users when first accessing the workspace. **Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

 For more information on configuring the home page, see [Customize a workspace home page in Workspace Builder](../../app-engine-studio/task/edit-workspace-home-page.md).

 For information on configuring the basic settings for a workspace, see [Configure workspace settings in Workspace Builder](../../app-engine-studio/task/configure-workspace-settings.md).

</td></tr><tr><td>

List

</td><td>

List pages for records from the specified tables, which help users to find individual records in a workspace. **Note:** If you remove the list page/route, you must use UI Builder to edit the workspace, not Workspace Builder.

 You can create a list category and then add filtered lists for each list category. Filtered lists apply unique conditions, ensuring that only the filtered subset of records appears.

 For more information on adding and editing lists in Workspace Builder, see [Create lists for a workspace in Workspace Builder](../../app-engine-studio/task/add-workspace-list.md).

</td></tr><tr><td>

Analytics

</td><td>

The customizable Analytics Center enables users to track and analyze records and usage with dashboards, data visualizations, and insights on your instance. **Note:** If Analytics Center page/route doesn't exist for a workspace, Workspace Builder is still available, but the Analytics Center tab doesn't appear in the workspace.

 For more information on enabling the Analytics Center for a workspace, see [Enable analytics for a workspace in Workspace Builder](../../app-engine-studio/task/configure-analytics-workspace.md).

</td></tr><tr><td>

Record pages

</td><td>

Pages in a table that give users useful information to work on a task, issue, or incident. Useful information can include priority, state, activity, and so on.Create and customize record pages by using containers and components in different sections of the layout. You can also add a Playbook Experience to a record page.

 For more information, see [Add a record page for a workspace in Workspace Builder](../../app-engine-studio/task/configure-record-page-workspace.md).

</td></tr></tbody>
</table>**Note:** Your workspace must have a home page and lists for you to edit it in Workspace Builder. If they aren't present, you must edit the workspace in UI Builder.

**Parent Topic:**[Exploring Workspace Builder](exploring-workspace-builder.md)

