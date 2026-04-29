---
title: Platform Analytics experience dashboard categories
description: Dashboard categories enable searching and filtering dashboards using general terms assigned to multiple dashboards.Dashboard categories users to filter the dashboards in the dashboard overview on terms or phrases describing the dashboard as provided by its creator or the analytics\_categories\_admin.Categories enable users to filter dashboards in the Dashboard library. You can assign one or more categories to each dashboard
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics experience dashboard categories

Dashboard categories enable searching and filtering dashboards using general terms assigned to multiple dashboards.

**Note:** Core UI dashboard groups are migrated into categories.

Users with the platform\_analytics\_admin or analytics\_categories\_admin can create, edit, and remove dashboard categories. Users can then apply one or more categories to dashboards they create and can filter the dashboards in the Dashboards library by category.

When there are enough categories, you can search for categories in the dashboard overview. Otherwise, all categories that have been assigned to dashboards are visible under **Filter by categories**. Categories that have not been assigned in the dashboard's Information panel do not appear in the overview.

Navigate to analytics\_category.list to view all categories.

## Create dashboard categories

Dashboard categories users to filter the dashboards in the dashboard overview on terms or phrases describing the dashboard as provided by its creator or the analytics\_categories\_admin.

### Before you begin

Role required: analytics\_categories\_admin

### Procedure

1.  Select the Application scope icon \(![Application scope icon](../../../administer/virtual-agent/images/icon-scope.png)\) and choose the scope the category should apply to.

    The default application scope is Global.

2.  Navigate to **All** &gt; **Usage and Governance** &gt; **Analytics Categories**.

    You can also select **Create new category** in the Details window of a dashboard in Edit mode to open the Category New record form.

    ![Dashboard category section of dashboard information panel](../image/db-create-new-category.png)

3.  Select **New**.

4.  Provide a name for the category.

5.  Select **Submit**.


### Result

The category is available to apply to dashboards in the Info panel, and to search on in the Dashboards library.

## Assign dashboard categories

Categories enable users to filter dashboards in the Dashboard library. You can assign one or more categories to each dashboard

### Before you begin

Role required: Any user who can create a dashboard can assign an existing category to it. Only users with the analytics\_categories\_admin role can create categories. Only the owner of the dashboard or users with the analytics\_categories\_admin and dashboard\_admin roles can assign categories to an existing dashboard.

Assign dashboard categories on the dashboard's info panel.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select the dashboard you want to apply a category to.

3.  Select the Edit button \(![Edit button](../image/edit-button.png)\) to put the dashboard into Edit mode.

4.  Select the Info button \(![Info button](../../par-for-workspace/image/icon-info.png)\) to open the dashboard's Information panel and choose the categories you want to apply.

    Users with the analytics\_categories\_admin role also have the option to create a new category.

5.  Select **Exit editing mode** to apply the categories to the dashboard.


### Result

-   Dashboard cards in the library indicate which categories are applied.
-   Users can find the dashboard by filtering on the assigned categories.

