---
title: Add or remove CIs for multiple application services using connection suggestions
description: If the discovery based on Predictive Intelligence is enabled, the newly mapped application services include only CIs and CI connections added by discovery patterns. Use connection suggestions to decide which configuration items \(CIs\) to include or exclude globally. Service Mapping then updates all relevant discovered application services to reflect your decisions.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Map multiple application services suggested by classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Add or remove CIs for multiple application services using connection suggestions

If the discovery based on Predictive Intelligence is enabled, the newly mapped application services include only CIs and CI connections added by discovery patterns. Use connection suggestions to decide which configuration items \(CIs\) to include or exclude globally. Service Mapping then updates all relevant discovered application services to reflect your decisions.

## Before you begin

Confirm that fingerprint-based discovery remains enabled, since it is enabled by default. To verify, navigate to **All** &gt; **System Properties** &gt; **All Properties**. Check that the **sys\_property process.clustering.appfingerprint.enabled** property does not appear on the list.

Confirm that discovery based on Predictive Intelligence is enabled. Navigate to the System Property \[sys\_properties\] table and verify that the **sa\_ml.connection\_suggestions.active** property is set to **True**.

You can add or remove CIs using connection suggestions only in application services discovered by Service Mapping.

Role required: service\_mapping\_admin

## About this task

If Predictive Intelligence is enabled, Service Mapping automatically adds connections to service instances based on connection rules. These suggestions are generated using traffic-related data from the Configuration Management Database \(CMDB\) and the analysis of application fingerprints, CIs, and processes by Predictive Intelligence. Predictive Intelligence evaluates connections between application fingerprints, CIs, and processes, and ranks their relevancy. Service Mapping uses this information to create connections based on connection rules. It also generates connection suggestions for servers and load balancers for you to decide which connections to add or remove from the service instances. For more information, see [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

If you are not sure which traffic-based connections are relevant, identify a group of application services that your organization uses for the same purpose. [Add or remove CI connections for a single application service](add-remove-ci-connections-services.md) in this group. Then use the connections you created for this service as an example of traffic-based connections for multiple application services.

## Procedure

1.  [Discover applications based on fingerprints](../../discovery/task/discover-application-based-process.md) to view information about all application CIs in connection suggestions.

    **Important:** Not using fingerprint-based discovery may result in mapping some application CIs as generic applications.

2.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Connection Suggestions**.

    The Connection Suggestions window opens.

3.  Expand the relevant group to see the connection suggestions.

    For example, expand the **python - python** group.

4.  Review the suggestion details paying attention to the parameters covered in [Connection Suggestions list](../reference/connection-suggestions-list.md).

5.  Select the check boxes next to the relevant suggestions and click the action button at the bottom of the window:

<table id="table_ahl_r3s_fnb"><thead><tr><th>

Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Add

</td><td>

Service Mapping includes both the connections and the CIs that these connections lead to, making them part of the service instance. The **Decision** value for added connections changes to **Added manually**.

</td></tr><tr><td>

Exclude

</td><td>

Service Mapping excludes connections and the CIs they lead to from the service instance. The **Decision** value for removed connections changes to **Excluded manually**.

</td></tr><tr><td>

Reset

</td><td>

Service Mapping reverses earlier decisions, whether made manually or by rule. The **Decision** value for reset connections changes to **Undecided**. This action is relevant only if you have already used connection suggestions to complete this service instance.

</td></tr></tbody>
</table>6.  Refresh the connection suggestions to see the changes that you made:

    1.  Click the List controls icon ![List control button](../image/list-controls-button.png).

    2.  Select **Refresh list**.


## Result

Service Mapping applies the changes to traffic-based connections to all relevant application services in the background.

**Parent Topic:**[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

