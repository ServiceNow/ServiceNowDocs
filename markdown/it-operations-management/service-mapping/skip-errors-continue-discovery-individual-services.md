---
title: Skip errors to continue discovering an application service
description: If you know what configuration items \(CIs\) and connections make up your service instance, you can enable Service Mapping to continue discovery of the service instance even if there are some errors. You can skip errors to troubleshoot later so you can complete mapping most of the service instance, even if some CIs are missing.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Fix errors in individual application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Skip errors to continue discovering an application service

If you know what configuration items \(CIs\) and connections make up your service instance, you can enable Service Mapping to continue discovery of the service instance even if there are some errors. You can skip errors to troubleshoot later so you can complete mapping most of the service instance, even if some CIs are missing.

## Before you begin

Familiarize yourself with the structure of the application service to know which CIs make up the next tier after the problematic CI. If necessary, consult the application service owner to collect necessary information.

Role required: service\_mapping\_admin or admin

## About this task

Normally, discovery of an application service stops when Service Mapping fails to identify a CI. In this case, the map shows a warning icon instead of the undiscovered CI. There are no CIs or connections going out of the undiscovered CI.

![An application service map showing an undiscovered CI.](../image/MapUndiscoveredCI.png "Undiscovered CI on the map")

You can overcome the obstacle of the undiscovered CI and restart discovery from the CIs belonging to the next tier after the problematic CI. To do so, add a CI manually if you know what the undiscovered CI is and what the incoming connection of the next tier CI is. Service Mapping uses incoming connections to access a CI for discovery. These connections are referred to as endpoints.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Ensure that the map opens in Edit mode.

    ![When you click Edit, the Discovery Messages section appears.](../image/MapEditDiscoveryMessages.png)

3.  Ensure that the map is not in the Host View.

4.  Click the arrow next to the undiscovered CI and select **Skip and Resume**.

5.  Define attributes of the CI you want to manually place instead of the undiscovered CI.

<table id="table_sbr_zjr_31b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI Type

</td><td>

Select the CI type \(CI class\) for the CI you are adding. Every CI belongs to a CI type which contains a set of attributes configured for this kind of CI, for example, **cmdb\_ci\_appl** for applications.

</td></tr><tr><td>

CI Name

</td><td>

Select the CI from the list of CIs of the selected CI type.**Note:** To eliminate the possibility of delayed results when searching for a specific CI, make your search as specific as possible. A search with \*&lt;name&gt; might take a long time and return a large data set.

</td></tr></tbody>
</table>    **Note:**

    If the CI type does not appear in the list, Service Mapping does not allow adding CIs of this type manually. For example, you cannot add an application cluster or an endpoint manually.

6.  Configure attributes of the entry point from which Service Mapping continues discovery by selecting the entry point type and [entering relevant fields](../reference/r_EntryPointsforBizSvcDef.md).

    If the required entry point type does not appear in the Select Entry Point Type list, create it as described in [Create entry point types for Service Mapping](t_CreateEntryPoint.md).

7.  Click **Submit**.

    The map shows the manually added CI instead of the undiscovered CI. Service Mapping starts discovery for CIs of the next tiers. When the discovery process finishes, the map shows all discovered CIs below the manually added CI.

    ![Result of skip and resume](../image/MapSkipNResumeResult.png)


## What to do next

To discover the problematic CI automatically:

1.  Perform necessary troubleshooting to enable Service Mapping to discover the problematic CI. For example, you may need to customize the relevant pattern, provide missing credentials or fine-tune traffic-based discovery.
2.  Navigate to the relevant service instance map.
3.  Click **Run discovery**.
4.  After the discovery process finishes, verify that Service Mapping discovered the CI. If Service Mapping discovered the CI, the map shows the actual CI without the Warning icon \(![The Warning icon](../image/MapWarningIcon.png)\).

**Parent Topic:**[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

**Related topics**  


[Fix errors in individual application services using discovery messages](fix-errors-by-discovery-messages.md)

[Resolve pattern-related mapping errors](t_TBSMapProcess.md)

[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

[Enable traffic-based discovery for CI types or specific CIs](t_CreateATrafficBasedDiscoveryRule.md)

[Prerequisites for performing top-down discovery using Service Mapping](../reference/prerequisites-service-mapping.md)

