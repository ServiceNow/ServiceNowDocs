---
title: Schedule a top-down discovery by Service Mapping
description: After Service Mapping discovers configuration items \(CIs\) belonging to your service instance for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs. For example, you may create custom discovery schedules to avoid redundant stress on the infrastructure.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Application service completion, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Schedule a top-down discovery by Service Mapping

After Service Mapping discovers configuration items \(CIs\) belonging to your service instance for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs. For example, you may create custom discovery schedules to avoid redundant stress on the infrastructure.

## Before you begin

Define your application services prior to defining discovery schedules for discovering CIs which are part of these services.

When creating a schedule for CI types or specific CIs, make sure that at least one application service containing the relevant CI is in the **operational** state.

Learn about different types of [top-down discovery schedules](../concept/top-down-discovery-schedules.md).

Role required: service\_mapping\_admin

## About this task

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Discovery Schedules**.

2.  To create a custom discovery schedule, click **New**.

    Or

    To customize the generic schedule for all application CIs, click **All Applications** or **Load Balancer Service**.

    ![The Discovery Schedule form for top-down discovery.](../image/sm-admin-discovery-schedule-new.png)

3.  In fresh install or reset instances, fill in the fields in the Discovery Schedule form.

<table id="table_gyn_scs_khb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

For a new specific schedule, enter a unique and descriptive name.

</td></tr><tr><td>

Discover

</td><td>

By default, the value for this field is `Service`, indicating that you are creating a top-down discovery schedule. You cannot change this value.

</td></tr><tr><td>

Discover by

</td><td>

The schedule types for specific top-down discovery:-   CI Type
-   Specific CI
-   Service Attributes
-   Service Group Attributes


</td></tr><tr><td>

CI type

</td><td>

This field is available when CI type is selected from Select Discovery. For a new CI type-based schedule, select the relevant application CI type from the list.

</td></tr><tr><td>

CI

</td><td>

This field is available when `Specific CI` is selected from **Discover by**. For a new schedule for a specific CI, select the relevant CI from the list.

</td></tr><tr><td>

Filter Services to Discover

</td><td>

This area contains the condition builder and is available when `Service Attributes` is selected from **Discover by**. Use the filter to create the filtering criteria for services. Service Mapping discovers only services that answer the defined criteria.

</td></tr><tr><td>

Filter Groups to Discover

</td><td>

This field contains the condition builder and is available when `Service Group Attributes` is selected from **Discover by**. Use the filter to create the filtering criteria for service groups. Service Mapping discovers only services belonging to the groups that answer the defined criteria.

</td></tr></tbody>
</table>4.  For a discovery schedule based on service attributes, click **View Selected Services** to preview the list of services that answer the filtering criteria you entered, and then select **Close**.

5.  For a discovery schedule based on service group attributes, click **View Selected Groups** to preview the list of groups that answer the filtering criteria you entered, and then select **Close**.

6.  Define the rediscovery frequency by selecting the relevant option from the **Run** list.

    See [Run options for discovery schedules](../../it-operations-management/reference/discovery-schedule-run-options.md).

7.  Click **Submit**.


-   **[Top-down discovery schedules](../concept/top-down-discovery-schedules.md)**  
Learn about schedules that trigger top-down discovery of application services.

**Parent Topic:**[Application service completion](../concept/advanced-business-service-definitions.md)

**Related topics**  


[Define criticality for application services](define-criticality-for-business-services.md)

[Group application services](organizing_services-into-groups.md)

[Control user access to application services](control-user-access-to-business-services.md)

[Service definition transfer from one instance to another](../concept/transfer-service-definitions.md#)

[Pattern-based discovery in Service Mapping](../concept/pattern-based-discovery.md)

