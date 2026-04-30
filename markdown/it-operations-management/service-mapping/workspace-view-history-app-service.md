---
title: View the change history of application services in legacy Agent Workspace
description: View changes made to a service instance and to the individual configuration items \(CIs\) comprising the service in Agent Workspace. You can also compare the service status before and after a certain change or problem. The change history is useful for maintenance, planning, or troubleshooting procedures.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Application service analysis and maintenance using legacy Agent Workspace, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View the change history of application services in legacy Agent Workspace

View changes made to a service instance and to the individual configuration items \(CIs\) comprising the service in Agent Workspace. You can also compare the service status before and after a certain change or problem. The change history is useful for maintenance, planning, or troubleshooting procedures.

## Before you begin

Role required: admin, service\_mapping\_admin, service\_mapping\_user, app\_service\_admin, or app\_service\_user

## About this task

Details about changes to a service instance and to its CIs are stored in the CMDB. Typically, these changes reflect adding or removing CIs from a service instance, upgrading or updating CIs, or modifying CI configuration files. The system gathers this data by querying CMDB tables and then creating the change history view. In deployments where Service Mapping is activated, the type of change information Service Mapping queries depends on discovery patterns that Service Mapping uses to discover CIs.

Changes to the application service appear on the history timeline.

![The history scale shows changes to the application service.](../image/ws-map-history-pointers.png "The history scale shows changes to the application service")

Specify two points in time for which to compare the two versions of an application service. You can use the change marks on the timeline to specify points in time that are before and after a change for which you want to see details. For example, if you know that the application service started to fail at a certain time, you can compare two versions of the application service, one before and one after the problem started. This comparison lets you see the summary of changes that possibly led to the problems.

The default timeline range is the recent week. The upper limit of the time range is the moment when you opened the map in the Change History view. If the application service was created less than a week ago, the time range starts from the time of service creation.

The time range cannot contain more than 1 thousand changes. If there are more changes within the selected range, the history scale automatically adjusts to display 1 thousand changes.

To view validation status of changes and changes to related items, like tracked configuration files, use the classic Service Mapping UI. For more information, see [View the change history of application services in classic Service Mapping](t_ViewCIChanges.md) and [Compare two versions of an application service in classic Service Mapping](t_CompareBS.md).

## Procedure

1.  In Agent Workspace, click the **Lists** icon on the left pane.

2.  Navigate to **All** &gt; **Services** &gt; **All Services**.

    The list of services displays services in Operational status.

3.  Click the name of the relevant service instance.

    The service tab opens showing service details on the Details tab.

4.  Click **Service Map**.

    The Service Map tab opens displaying the map of this application service.

5.  Click **Change History Map**.

    The History Map tab displays the map in the history view. By default, the time range is a week.

6.  Compare the application service before and after a change, by performing the following steps:

    1.  Change the time range on the timeline by clicking the **Zoom in** or **Zoom out** buttons next to the timeline.

        Alternatively, point at the timeline and scroll.

        The map shows changes to CIs. CIs are marked as added, updated, or deleted.

        The **Properties History** pane shows the comparison summary of changes to this application service. Click **Change history** ![Change history button](../image/change-history-button.png) to view change record cards for this application service.

        ![test](../image/workspace-history-change-button.gif)

    2.  Focus on changes on the map using one of the following methods:

        -   To highlight the CI responsible for the change record and to show the change record card, click the change mark on the timeline. You can highlight multiple CIs by clicking the mark for multiple changes.

            ![test](../image/ws-map-history-select-mark-test.png)

        -   To highlight the CI responsible for the change in the map, click the change record card in the Change history pane.

            ![Select change card to highlight the CI responsible for this change in the map.](../image/ws-map-history-select-change.png)

        -   To display the related change record card in the Change history pane, click the CI on the map.

            ![Select CI to view corresponding change record in the Change history pane](../image/ws-map-history-select-CI.png)


**Parent Topic:**[Application service analysis and maintenance using legacy Agent Workspace](../concept/service-analysis-maintenance-legacy-workspace.md)

