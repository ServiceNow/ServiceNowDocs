---
title: Move a Platform Analytics dashboard with an update set
description: Dashboard tabs aren’t automatically transferred in update sets. You can add a dashboard's components to update sets from a dashboard record using the Unload Dashboard function. The Unload Dashboard function unloads the entire dashboard with related content.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-01-27"
reading_time_minutes: 2
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Move a Platform Analytics dashboard with an update set

Dashboard tabs aren’t automatically transferred in update sets. You can add a dashboard's components to update sets from a dashboard record using the **Unload Dashboard** function. The **Unload Dashboard** function unloads the entire dashboard with related content.

## Before you begin

Role required: admin

## About this task

This procedure describes moving the structure of an in-line dashboard to an update set. The dashboard structure includes the dashboard itself, tabs, the related security configuration, and dashboard-specific settings such as header color and borders. Moving technical dashboards with update sets is not supported.

This procedure adds saved data visualizations and filters to the update set. Other content is not moved. You can add dashboard content to the update set using default platform functionality.

**Important:** Make sure that the dashboard content is either in the same update set as the dashboard record or is already present in the target instance. Errors result if the moved dashboard points to content that doesn’t exist on the target instance.

Additional steps may be necessary if you are moving a dashboard in a scoped application. For more information, see [Update set id 'global' is different than update set scope id](../concept/troubleshooting-dashboard-update-set.md#).

**Tip:** If you have difficulty with this procedure, contact Customer Service and Support.

## Procedure

1.  Create a new update set and activate it.

2.  In the source instance, navigate to `par_dashboard_list.do`.

3.  Select the dashboard that you want to unload to an update set.

4.  Select the Additional actions icon \(![Additional actions icon](../image/icon-context-p.png)\) and select **Unload Dashboard**.

    Only perform this step after the dashboard is ready to unload, meaning that you’ve added all content to the tabs.

    The record for a dashboard in the par\_dashboard table is always updated. This update to par\_dashboard should always be included in the update set when transferring it to another instance. This also updates the sys\_updated\_on field even if no other fields are modified, such as when only widgets are changed.

5.  When you’re ready to move the update set, mark the update set as complete.

6.  On the target instance, move the update using standard update set functionality.

    For more information, see [Retrieve an update set](https://www.servicenow.com/docs/access?context=t_RetrieveAnUpdateSet&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

    On the Remote Instance page, the **Retrieved Update Sets** related list shows all retrieved update sets. Select the update set to see if there are errors. Errors are shown on the **Retrieved Update Set** form in a related list called **Update Set Preview Problems**.


## Result

The dashboard and its tabs are moved to the target instance.

