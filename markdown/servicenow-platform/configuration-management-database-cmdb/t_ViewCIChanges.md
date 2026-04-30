---
title: View the change history of application services in classic Service Mapping
description: You can view the changes made to an application service as a whole and to the individual configuration items \(CIs\) comprising the service. Change history is useful for maintenance, planning, or troubleshooting procedures.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View the change history of application services in classic Service Mapping

You can view the changes made to an application service as a whole and to the individual configuration items \(CIs\) comprising the service. Change history is useful for maintenance, planning, or troubleshooting procedures.

## Before you begin

Role required: admin, service\_mapping\_admin, service\_mapping\_user, app\_service\_admin, or app\_service\_user

## About this task

Details about changes to a service instance and to its CIs are stored in the CMDB. Typically, these changes reflect adding or removing CIs from a service instance, upgrading or updating CIs, or modifying CI configuration files. The system gathers this data by querying CMDB tables and then creating the change history view. In deployments where Service Mapping is activated, the type of change information Service Mapping queries depends on discovery patterns that Service Mapping uses to discover CIs.

Changes to configuration files are associated with CIs to which these files belong. Maps show configuration file changes as changes to related CIs.

While you can see change records for a specific CI in the context of application services, you can also see detailed history of a specific CI separate from its service instance as described in [History Timeline](https://www.servicenow.com/docs/access?context=c_HistoryTimeline&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

If the ServiceNow AI Platform is configured to validate changes, all changes are evaluated and rendered as valid or not. If a change is valid, its change record on the service instance map is marked as approved. For more information about configuring the platform for change validation, see [Managing proposed changes](../../../Chunk961610506.md#).

Changes to the service instance appear on the history timeline.

![The history scale shows changes to the service instance.](../image/MapHistoryPointers.png)

The type of change mark depends on the nature of changes that it represents:

-   **Light gray balloon \(![Light grey balloon icon](../image/ChangeHistoryBalloonsLightGray.png)\)**

    Unapproved change that does not influence the service instance behavior. For example, a change in a network path or adding a node to a cluster.

-   **Dark gray balloon \(![Dark gray balloon icon](../image/ChangeHistoryBalloonsDarkGray.png)\)**

    Unapproved change that changes the service instance behavior.

-   **Green balloon \(![Green balloon icon](../image/ChangeHistoryBalloonsGreen.png)\)**

    An approved change in deployments where the ServiceNow AI Platform is configured to validate changes.

-   **Double balloon \(![Green balloon icon](../image/ChangeHistoryBalloonsDouble.png)\)**

    Multiple separate changes that happened a short time from each other.


You can mark times on the history scale by creating baselines to quickly return to the marked view.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Review change records created for this service instance on the **Changes** tab at the bottom of the page.

    If Service Mapping is deployed, then in Edit mode, the Discovery Messages section appears below the map.

3.  On the history timeline, set the time range of changes that you want to view.

<table id="choicetable_dnx_mtk_51b"><thead><tr><th align="left" id="d403851e301">

Option

</th><th align="left" id="d403851e304">

Action

</th></tr></thead><tbody><tr><td id="d403851e310">

**To set the time range of the history timeline**

</td><td>

Click the hour, day, week, or month icons.![Click Hours, Days, Weeks, or Months to set the time range of the history scale.](../image/MapHistoryTimeRangeIcons.png)

</td></tr><tr><td id="d403851e325">

**To increase or decrease the time range**

</td><td>

Click the zoom in and zoom out icons.![Click Zoom in and Zoom out to change the time range.](../image/MapHistoryPlusMinusIcons.png)

</td></tr><tr><td id="d403851e340">

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

4.  To mark a time on the time scale, set a baseline:

    1.  Click the **Compare** icon.

        ![The Compare icon on the Map page.](../image/MapHistoryCompareIcon.png)

    2.  Navigate to the time you want to mark as a baseline on the history scale.

    3.  Click **Set baseline**.

        ![Click Set baseline.](../image/MapHistoryBaselineSet.png)

    4.  Enter the name of the baseline and click **OK**.

        The new baseline appears as a button above the history scale and as a blue flag on the history scale.

        ![The Baseline button and flag.](../image/MapHistoryBaselineFlag.png)

5.  View the change history.

<table id="choicetable_ky8_b2k_s5"><thead><tr><th align="left" id="d403851e477">

Option

</th><th align="left" id="d403851e480">

Action

</th></tr></thead><tbody><tr><td id="d403851e486">

**To see the CI responsible for a change record**

</td><td>

Select a change record on the **Changes** tab.The related CI is marked yellow in the map.

 ![View the CI responsible for a change record.](../image/MapChangesTabSelectRecord.png)

</td></tr><tr><td id="d403851e508">

**To see only change records related to a CI**

</td><td>

Select the required CI or the connection on the map.The **Changes** tab displays only change records related to the selected CI or connection.

 ![View only change records related to a CI.](../image/MapChangesTabSelectCI.png)

</td></tr><tr><td id="d403851e530">

**To see the configuration file at the selected moment in the past**

</td><td>

1.  Set the time on the history scale.
2.  In the **Properties** pane, scroll to **Tracked Configuration Files**, and click the file name.

The new tab opens displaying the content of the tracked configuration file at the selected time.

</td></tr><tr><td id="d403851e556">

**To see the network at the selected moment in the past**

</td><td>

1.  Set the time on the history scale.
2.  Right-click the connection and select **Show network path**.

The new tab opens displaying the network or storage path map for the time you selected.

 **Note:** You cannot view the network path for connections marked as boundaries to this service instance.

</td></tr></tbody>
</table>6.  To exit the history view and see the current status of the service instance, click the current icon.

    ![The graphic shows the current icon for exiting the history view.](../image/MapHistoryCurrentIcon.png)


**Related topics**  


[View an application service map in base system](../../configuration-management/task/app-service-map-base-system.md)

[Compare two versions of an application service in classic Service Mapping](t_CompareBS.md)

[Modify tracking changes in configuration files](https://www.servicenow.com/docs/access?context=track-configuration-files&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

[Fine-tune tracking changes for the change history](https://www.servicenow.com/docs/access?context=exclude-changes-from-change-history&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

