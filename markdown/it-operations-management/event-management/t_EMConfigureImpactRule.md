---
title: Adjust impact rules for a CI
description: Configure impact rules to customize the impact calculation for discovery services and manual services. The impact rules update the overall alert and show the impact on related CIs. When you change impact rules, the updates apply to alert severity in places such as the Event Management dashboard and Operator Workspace.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Adjust impact rules for a CI

Configure impact rules to customize the impact calculation for discovery services and manual services. The impact rules update the overall alert and show the impact on related CIs. When you change impact rules, the updates apply to alert severity in places such as the Event Management dashboard and Operator Workspace.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can view and adjust the impact rules of CIs from the application service map of a service.

**Note:** Event Management Dashboard is not supported for new instances in the Paris release. However, instances upgraded from a release prior to Orlando that use Event Management Dashboard can continue to do so.

## Procedure

1.  Open the application service map from either the Event Management dashboard or the Application service list.

<table id="choicetable_mbd_wfk_35"><tbody><tr><td id="d527206e131">

**From the Event Management dashboard**

</td><td>

1.  Navigate to **Event Management** &gt; **Dashboard**.
2.  Double-click the tile of the application services.


</td></tr><tr><td id="d527206e161">

**From the Application Service list**

</td><td>

1.  Navigate to **Event Management** &gt; **Services** &gt; **Application Services**.
2.  Click **View Map** next to the application services.


</td></tr></tbody>
</table>2.  On the application service map, click a CI.

3.  Below the map, click the **Impact** tab and then adjust the impact rules accordingly.

<table id="table_AlertRuleForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the impact rule.-   **Application Cluster Member**: Determines how application cluster members affect the overall impact of the cluster. For example, if a three-member cluster requires **90% Influence** to set the severity for the entire cluster to **Major**, each member has **30% Influence** \(90% divided by 3\). The severity of the entire cluster can only change to **Major** when all three members have a severity of **Major**.

**Note:** To configure a manual cluster, see [Configure a manual cluster](configure-manual-cluster.md)

-   **Application Impact**: Determines how impact is applied to a specific CI, the overall application service, or parent/child entities within an application service. For the Application Impact rule, you can choose from the following Impact options: **Application Service** or **Parent**.
    -   If no CI is selected, the alert rule applies to the entire application service.
    -   If you select a specific CI, you can define whether the rule applies to the service or its parent.
-   **CI Parent in Application**: Sets impact only on the parent entity.
-   **Inclusion**: Determines the impact on entities with a Contains relationship. This rule is read-only.
-   **Infrastructure Dependencies**: Determines the definition of impact propagation for CIs in infrastructure relationships.
-   **Network Path**: Determines how impact applies to parent or child entities that are part of a traditional network.
-   **OS Cluster Member**: Determines how host cluster members affect the overall cluster status based on a percentage or number of cluster members. For example, if a three-host cluster requires **60% Influence** to set the severity of **Major**, each member has **20% Influence** \(60% divided by 3\). The severity of the entire cluster can only change to **Major** when two or more cluster members have a severity of **Major**. The entire cluster is also considered to be down.
-   **Storage Path**: Determines how impact applies to parent or child entities that are part of a storage network.


</td></tr><tr><td>

Impact On

</td><td>

The valid type of service for this impact rule.-   **Application Service**: The impact rule applies to a application service.
-   **Parent**: The impact rule applies to the parent CI.


</td></tr><tr><td>

Influence

</td><td>

The value to allow the impact rule to set on the parent. Set a value on the parent. This field works with the **Influence Units** field.

</td></tr><tr><td>

Influence Units

</td><td>

The unit of measurement to show impact on the parent. Set the highest value on the parent CI. Set lower values on each child CI. When alerts occur for several child CIs, Event Management calculates the sum of the **Influence Units** of each affected child. If the sum exceeds the parent **Influence Units** value, the parent receives the highest severity in the set. This field works with the **Influence** field.-   **Percent**: When the percentage exceeds the **Influence** value, apply the impact on the parent.
-   **Number**: When the number exceeds the **Influence** value, apply the impact on the parent.

For example, you can set the parent **Influence Units** to **100%** and the child CIs to these values:

    -   Child 1: 34%
    -   Child 2: 34%
    -   Child 3: 34%
    -   Child 4: 70%
When alerts for Child 3 and Child 5 have the Critical severity, the severity of the parent is set to Critical because the sum is greater than 100% \(34% + 70% = 104%\).

</td></tr><tr><td>

Impact when Critical

</td><td>

The alternative impact to use when the calculated severity is Critical. If the column to the right of **Impact when Critical** has a higher severity, update all right-most columns with the same or a lower severity as **Impact when Critical**. To make sure the topology and impact tree accurately show impact, always update each column accordingly.-   **Critical**: Red \(highest severity\).
-   **Major**: Orange.
-   **Minor**: Yellow.
-   **Warning**: Blue \(lowest severity\).


</td></tr><tr><td>

Impact when Major

</td><td>

The alternative impact to use when the calculated severity is **Major**. If the column to the right of **Impact when Major** has a higher severity, update all right-most columns the same or a lower severity as **Impact when Major**. To make sure the topology and impact tree accurately show impact, always update each column accordingly.-   **Critical**: Red \(highest severity\).
-   **Major**: Orange.
-   **Minor**: Yellow.
-   **Warning**: Blue \(lowest severity\).


</td></tr><tr><td>

Impact when Minor

</td><td>

The alternative impact to use when the calculated severity is **Minor**. Controls the field values to the right of this field. If the **Impact when Warning** column has a higher severity, use the **Impact when Minor** value for both fields. To make sure the topology and impact tree accurately show impact, always update each column accordingly.-   **Critical**: Red \(highest severity\).
-   **Major**: Orange.
-   **Minor**: Yellow.
-   **Warning**: Blue \(lowest severity\).


</td></tr><tr><td>

Impact when Warning

</td><td>

The alternative impact to use when the calculated severity is **Warning**. To make sure the topology and impact tree accurately show impact, make sure that the columns to the left have higher severities.-   **Critical**: Red \(highest severity\).
-   **Major**: Orange.
-   **Minor**: Yellow.
-   **Warning**: Blue \(lowest severity\).


</td></tr></tbody>
</table>
## What to do next

Review the changes on the impact tree. For example, if you changed a number or percentage influence for child CIs, review the impact tree updates accordingly.

