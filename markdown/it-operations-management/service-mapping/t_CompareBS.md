---
title: Compare two versions of an application service in classic Service Mapping
description: You can see a summary of application service changes at a glance by comparing two versions of an application service. This feature is useful for checking the application service status before and after a certain change or problem.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Compare two versions of an application service in classic Service Mapping

You can see a summary of application service changes at a glance by comparing two versions of an application service. This feature is useful for checking the application service status before and after a certain change or problem.

## Before you begin

Role required: sn\_cmdb\_admin, admin, app\_service\_admin, app\_service\_user, service\_mapping\_admin, or service\_mapping\_user

## About this task

Specify two points in time for which to compare the two versions of an application service. You can use the change indicators on the timeline to specify one point in time that is before and another that is after a change for which to see the details. For example, if you know that the application service started to fail at a certain time, you can compare two versions of the application service, one before and one after the problem started. This comparison lets you see the summary of changes that possibly led to the problems.

Service Mapping, if deployed, tracks and shows all changes to a CI including configuration files associated with a CI. When you compare two versions of an application service, you can see changes made to configuration files as changes to CIs. You can also compare two versions of a configuration file to see the actual changes in the files, during the time range specified for the comparison.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  If needed, click **Edit** to ensure that the map is in Edit mode.

    If Service Mapping is deployed, then in Edit mode, the Discovery Messages section appears below the map.

3.  On the history timeline, set the time range of changes that you want to view.

<table id="choicetable_dnx_mtk_51b"><thead><tr><th align="left" id="d489292e186">

Option

</th><th align="left" id="d489292e189">

Action

</th></tr></thead><tbody><tr><td id="d489292e195">

**To set the time range of the history timeline**

</td><td>

Click the hour, day, week, or month icons.![Click Hours, Days, Weeks, or Months to set the time range of the history scale.](../image/MapHistoryTimeRangeIcons.png)

</td></tr><tr><td id="d489292e210">

**To increase or decrease the time range**

</td><td>

Click the zoom in and zoom out icons.![Click Zoom in and Zoom out to change the time range.](../image/MapHistoryPlusMinusIcons.png)

</td></tr><tr><td id="d489292e225">

**To change the upper limit on your history range**

</td><td>

Click the history scale.![Click the history scale to mark the time which serves as the upper limit.](../image/MapHistoryMarkedPoint.png)

 The time that serves as the upper limit appears above the history timeline.

 **Note:**

You cannot set the lower limit on your history range to a time before this service instance was created. This time is marked with the **IT Service Created** event on the history timeline.

![The IT Service Created pointer on the History timeline.](../image/MapHistoryBSCreatedPointer.png)

</td></tr></tbody>
</table>    The map shows the history view of the service instance for the time you selected.

    **Note:** The **Change** tab shows all change records, even the ones which are filtered out of the history view.

4.  Click the **Compare** icon.

    ![The Compare icon on the Map page.](../image/MapHistoryCompareIcon.png)

5.  Set **Compare point 1** and **Compare point 2** as the two points in time for the comparison.

    You can drag the pointers on the history scale to set corresponding time points.

    ![Drag pointers to set time points.](../image/MapHistoryComparePointers.png)

    If the history scale does not include the time set for comparison, then its corresponding pointer appears next to the compare point in yellow:

    ![A yellow pointer](../image/MapHistoryComparePointersYellow.png)

    **Note:** If there are no changes to the service during the time interval specified by **Compare point 1** and **Compare point 2**, then no change details are displayed.

6.  Click **Compare**.

    The comparison view opens in a separate tab.

7.  Select a marked CI to see the relevant change record on the **Changes** tab.

    ![Selecting a changed CI on the comparison map marks the relevant change on the Changes tab.](../image/MapHistoryComparisonResult.png)

8.  If Service Mapping is deployed, you can compare two versions of a configuration file that appears on the map as Updated:

    1.  Select the CI that is associated with the updated configuration file.

    2.  In the **Properties** pane, click the link to the updated file.

        ![Click the link to see file comparison.](../image/MapHistoryComparisonFileTrack.png)

        The **Tracked Configuration Files Version Compare** tab opens showing two versions of the configuration file side by side.

    3.  Review actual changes.

        Highlight colors indicate the type of change:

        -   Purple — Updated line
        -   Pink — New line
        -   Gray — Deleted line
    4.  Navigate between the changes using the Next difference icon ![](../../discovery/image/next-difference-icon.png) and the Previous difference icon ![](../../discovery/image/previous-difference-icon.png).

    5.  Close the **Tracked Configuration Files Version Compare** tab when finished.

9.  Close the comparison view when finished.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Compare versions of CI configuration files](compare-configuration-files.md)

[View the change history of application services in classic Service Mapping](t_ViewCIChanges.md)

[Compare versions of CI configuration files](compare-configuration-files.md)

