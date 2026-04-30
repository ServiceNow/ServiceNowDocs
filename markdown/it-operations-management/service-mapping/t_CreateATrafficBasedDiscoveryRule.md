---
title: Enable traffic-based discovery for CI types or specific CIs
description: Service Mapping can discover and map CIs by detecting the inbound and outbound traffic that the CIs generate. Create a traffic-based discovery rule to determine which configuration items are available for traffic-based mapping.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Enable traffic-based discovery for CI types or specific CIs

Service Mapping can discover and map CIs by detecting the inbound and outbound traffic that the CIs generate. Create a traffic-based discovery rule to determine which configuration items are available for traffic-based mapping.

## Before you begin

If your ServiceNow instance uses domain separation and you have access to the global domain, log in to the relevant domain. The selected domain must be a domain without any child domains.

Role required: service\_mapping\_admin

-   Ensure that the traffic-based discovery is enabled at the Service Mapping product level: navigate to **Service Mapping** &gt; **Administration** &gt; **Properties** and verify that the **Traffic based discovery** check box is selected.
-   Enable traffic-based discovery for a specific service instance as described in [Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md).

## About this task

You may choose to use traffic-based discovery in addition to the pattern-based mapping.

You can create rules to configure Service Mapping to use traffic-based discovery for certain CIs. You can configure traffic-based discovery rules to monitor specific CIs or types of CIs.

For example, you enable traffic-based discovery for a specific service instance that includes a Tomcat server, a MySQL database, and a web application. You create a CI type rule that excludes all Tomcat servers from traffic-based discovery. However, you also create a discovery rule enabling traffic-based discovery for a specific Tomcat server. Service Mapping uses traffic-based discovery to discover the MySQL database, the web application, and that specific Tomcat despite the CI type rule excluding all Tomcat servers.

Depending on your configuration, the behavior of traffic-based discovery is different. If Predictive Intelligence is enabled, Service Mapping automatically adds connections to service instances based on connection rules. These suggestions are generated using traffic-related data from the Configuration Management Database \(CMDB\) and the analysis of application fingerprints, CIs, and processes by Predictive Intelligence.

If discovery based on Predictive Intelligence isn't enabled, Service Mapping automatically adds traffic-based connections using data from the CMDB to the service instances. However, to keep your service instances well-organized, you might need to manually remove connections to irrelevant CIs. To learn more about traffic-based method, see [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

If your instance uses domain separation, you can create traffic-based rules for specific domains. Rules in the base system are assigned to the global domain and apply to all domains of all levels.

When you create a rule for a specific domain, the new rule is used only for this domain and does not exist in any other domains. If you customize an existing rule in the global domain and assign it to a specific domain, you create a copy of the global rule, which is still used in all other domains except the domain that has the customized version of this rule. Likewise, if you customize a rule in the global domain, the change affects all domains except the one that uses a customized copy of this rule.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Traffic Based Discovery**.

2.  Click **New**.

3.  Define the rule parameters as follows:

    |Field|Description|
    |-----|-----------|
    |Action|Select **Enable** to add traffic-based connections to the specific CI or CI Type.|
    |Rule Scope|Select **Specific CI** to detect traffic for one configuration item, or select **CI Type** to detect traffic for all configuration items in one of the CI-based table.|
    |CI/CI Type|Select a specific CI, or select the table that contains the CIs for which you want to detect traffic.|
    |Domain|Select the domain to which the rule belongs.|

4.  Click **Submit**.

5.  To fine-tune traffic-based discovery, define advanced parameters as follows:

<table id="table_gdf_1zp_5w"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sa.traffic\_based\_discovery.conn\_aging\_time

</td><td>

Time period in hours for a Traffic Based Connection to remain active since last discovered. -   **Type**: integer
-   **Default value**: 72
-   **Other possible values**: any number higher than 24
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.


</td></tr><tr><td>

sa.traffic\_based\_discovery.ignored\_ports

</td><td>

Ports to ignore when found by traffic-based discovery. This property is available in the System Property \[sys\_properties\] table.

 Change this property to define ports that Service Mapping ignores while performing traffic-based discovery. It makes discovery more efficient since resources are not wasted on discovering irrelevant connections.

 -   **Type**: string
-   **Default value**: 445, 139, 111, 2049, 860, 3260, 135, 53
-   **Other possible values**: any relevant port numbers
-   **Location**: System Property \[sys\_properties\] table


</td></tr><tr><td>

sa.traffic\_based\_discovery.max\_connections

</td><td>

Maximum number of traffic-based connections from a single CI.This property is available in the System Property \[sys\_properties\] table.

 This property helps to keep the map size reasonable by limiting the number of possible CI connections.

 -   **Type**: integer
-   **Default value**: 30
-   **Other possible values**: any number higher than 1
-   **Location**: System Property \[sys\_properties\] table


</td></tr></tbody>
</table>
