---
title: CMDB groups
description: A CMDB group is a collection of CIs that lets you apply CI actions collectively to all the CIs that are members in the group.Depending on the group type, you can populate a CMDB group by manually adding individual CIs, selecting saved CMDB queries, or building encoded queries in the CMDB group itself. The resulting CIs from each query are added as members to the group.Display CI Lifecycle Management operational state and CI actions that apply to the CIs that are members of a CMDB group.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB groups

A CMDB group is a collection of CIs that lets you apply CI actions collectively to all the CIs that are members in the group.

For example, a CMDB CI Lifecycle Management API can use a CMDB group scriptable API to retrieve the group's list of CIs, and then apply a CI Lifecycle Management action collectively to all the CIs. You can also use a CMDB group with the [Dynamic CI Group](../task/populate-app-service-dynamic-group.md) service population method, to populate an application service.

## Group type

A CMDB group is configured with a group type.

-   If a CMDB group type is set to Health, then the CIs in the group can be monitored by CMDB Health, and the aggregated health is reported for the group as a whole in the CMDB group view dashboard. For example, you can monitor health only for CIs in a specific location.
-   If a CMDB group is set to CMDB Workspace, then that group appears in the [Management view](cmdb-workspace-mangmnt-view.md)in the [CMDB Workspace](cmdb-workspace.md).

## Create and populate a CMDB group

Depending on the group type, you can populate a CMDB group by manually adding individual CIs, selecting saved CMDB queries, or building encoded queries in the CMDB group itself. The resulting CIs from each query are added as members to the group.

### Before you begin

Roles required:

-   To view CMDB groups - itil
-   To use a CMDB queries - cmdb\_query\_builder on top of itil
-   To manually add CIs - itil or asset

Also, to populate a CMDB group using a CMDB query, a saved CMDB query must exist.

### About this task

The system property **glide.cmdb.group.max\_ci\_limit** determines the maximum number of CIs that a CMDB group can contain \(by default 10,000\). Once the specified limit is reached, CIs can't be added to the group unless you increase the value of that property.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Groups**.

2.  In the CMDB Groups pane, select **New**.

3.  Fill out the form, right-select the title bar and select **Save**.

<table id="table_lr4_xkc_4z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Name

</td><td>

A unique name for the group.

</td></tr><tr><td>

Group type

</td><td>

-   Default: Basic group type which can be populated by manually adding CIs, saved queries, and encoded queries.
-   Health: Sets CMDB Health to monitor the health of the group CIs and aggregate health results for the group as a whole.

Can be populated only by encoded queries.

**Note:** Dynamic filters are not supported when populating this type of CMDB groups.

-   CMDB Workspace: Custom class group which appears in the CI Overview panel in [CMDB Workspace store app](cmdb-workspace.md).

Can be populated only by encoded queries.

</td></tr></tbody>
</table>4.  To use saved CMDB queries:

    1.  Select **CMDB Group Contains Saved Queries** and then select **Add Query**.

    2.  Select a query from the **Query Builder Saved Query** list.

    3.  Select **Submit**.

    The returned results consists of the CIs from all the classes that are referenced in the saved query. Those CIs become members of the CMDB group.

5.  To manually add CIs:

    1.  Select **CMDB Group Contains Configuration Items** and then select **Edit Manual CI**.

    2.  Add filters.

    3.  Select CIs in the **Configuration Item** list and select the '**+'** icon at the bottom.

    4.  In the **Group members** list, select the CIs to add to the group.

    5.  Select **Save** or **Save and Exit**.

    6.  In the **Save Confirmation** dialog box, select **OK**.

    7.  Select **Submit**.

6.  To use encoded queries:

    1.  Select **CMDB Group Contains Encoded Queries** and then select **New**.

    2.  Fill out the CMDB Group Contains Encoded Query form with the query conditions that filter the CIs to be included in the group.

        **Note:** Dynamic filters aren't supported for CMDB health-type groups, even though it's possible to add them in a condition clause.

<table id="table_dht_rq2_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Class

</td><td>

Class for which the encoded query applies to.

</td></tr><tr><td>

CI Overview Condition

</td><td>

Filter that is used in the calculation for the CI Overview chart in [CMDB Workspace](cmdb-workspace.md). Applies only if the **sn\_cmdb\_ws.ci\_overview.enable\_simple\_condition** system property is set to **true** \(**false** by default\). Improves performance by yielding less results when there is a large amount of data in an environment that hasn't migrated to CSDM.

This condition isn't used when selecting **Show All CI**.

</td></tr><tr><td>

Condition

</td><td>

Filters the CIs that are included in the group. Used if **CI Overview Condition** isn't applicable.

</td></tr></tbody>
</table>    3.  Select **Submit**.


### What to do next

Select **Show All CI** to show all CIs from all the result columns of the query. However, only CIs from CMDB tables are shown.

## Show CI Lifecycle Management details for CMDB group CIs

Display CI Lifecycle Management operational state and CI actions that apply to the CIs that are members of a CMDB group.

### Before you begin

Role required: none

### About this task

If the CMDB group is based on a CMDB query, then the query runs in real-time and displays the resulting CIs. If the query does not complete successfully due to timing out or for other reasons, then appropriate error messages are displayed.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Groups**.

2.  On the **CMDB Groups** page, click a CMDB group.

3.  Click **Show All CI**.

    |Field|Description|
    |-----|-----------|
    |Configuration Item|CI group member.|
    |Class|Class of CI group member.|
    |Operational Status|CI Lifecycle Management operational state of the CI such as 'Repair in Progress' or 'Operational'. Possible operational states are defined in the choice list of the **Operational status** field in the cmdb\_ci table.|
    |Actions|CI Lifecycle Management actions that apply to the CI such as 'Cloning' and 'Provision'. Possible actions are defined in the CMDB CI Actions \[statemgmt\_cmdb\_actions\] table.|


