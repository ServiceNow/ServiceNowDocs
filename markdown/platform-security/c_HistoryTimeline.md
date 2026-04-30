---
title: History Timeline
description: You can view a timeline of changes for a CI and for its related records, relationships, baselines, and proposed changes for the CI. Timelines are available for CIs in the Configuration Item \[cmdb\_ci\] table or a descendant of this table, if auditing is enabled for the tables.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Knowing about History sets, Auditing, Platform Security]
---

# History Timeline

You can view a timeline of changes for a CI and for its related records, relationships, baselines, and proposed changes for the CI. Timelines are available for CIs in the Configuration Item \[cmdb\_ci\] table or a descendant of this table, if auditing is enabled for the tables.

Role required: The ACL for this view is based on the roles defined in the **glide.history.role** system property, which by default is set to `itil`. Also, the user must have read access to the History Set \[sys\_history\_set\] table, which by default is granted to admin.

You can open a timeline when you view the history of a CI. You can specify the time period, time range, and properties that are displayed in the timeline. You can view either what has changed in a particular change set, or view the entire CI to better troubleshoot any issues. You can also display a timeline of changes to the CI's related records, and export and compare snapshots of the CI at any point in time.

CI changes are represented by bubbles in different shapes and colors along the timeline. The shape of each bubble represents a different type of change and the color of each bubble specifies whether the change is valid or invalid. CI baselines are represented by black circles that you can hover over to display more details. Click the **?** icon to display bubble shape and color definitions, and point to a bubble to display details about the change set.

A change to a relationship is considered valid only if it was applied through change management. If the change was applied via the Proposed Changes framework, it is valid. For additional validation steps, see [Create or edit a planned validation script](https://www.servicenow.com/docs/access?context=c_ProposedChanges&version=xanadu&pubname=xanadu-servicenow-platform&section=t_CreatePlanChngValidScript&ft:locale=en-US).

![](../image/TimelineDashboard.png "History Timeline view")

![](../image/TimelineBubbles.png "Timeline bubbles")

**Note:** Proposed changes that do not have a planned start date are placed at future points of time.

## Timeline navigator

Use the handles on both ends of the timeline navigator to extend or to shorten the time period that is shown.

You can scroll to a different period of time by clicking on the bottom part of the timeline navigator and then dragging the navigator to the left or right.

## Zoom

By default, the timeline for the last month is shown. Next to the **Zoom** label above the timeline, you can select another time interval. You can select intervals from a minute to the entire period of data.

If there are many changes of the CI during the time period, the bubbles displayed might get too crowded. You can zoom in or out to spread the bubbles in either method:

-   Change the time interval on the timeline. As you shorten the time interval, you zoom in, and as you lengthen the time interval, you zoom out.
-   Select the section of the timeline that you want to zoom into.

## Property filter

You can filter the bubbles that are displayed. By default, all bubbles are displayed, representing changes to all of the CI's properties. You can limit the view to display only the bubbles in which selected properties have changed and exclude bubbles in which only unselected properties changed.

The **Detail** and **Summary** views highlight properties within your filter scope that have changed. The changed properties are highlighted in light blue.

In the **Summary** view, you can choose to include all the properties of the CI, or only properties that have changed. If you choose to display all properties in the summary view, then changed properties are listed before unchanged properties.

## Summary view

The **Summary** view displays snapshots of the CI's represented by each bubble. Each snapshot displays the changes to the CI's fields and relationships according to the change set. It displays old and new values before and after the change, and any relationships that were added or deleted.

Use the **&gt;** and **&lt;** buttons on both sides of the snapshot display to scroll through the next and previous change set records in a chronological order.

## Detail view

The **Detail** view displays snapshots of the CI that correspond with the bubbles. Each snapshot includes the fields that are within the property filter scope, displaying the properties that have changed with a light blue background. Click on a bubble to display its corresponding snapshot of the CI. The data that is displayed is read-only.

Use the **&gt;** and **&lt;** buttons on both sides to scroll through the next and previous change set records in a chronological order.

