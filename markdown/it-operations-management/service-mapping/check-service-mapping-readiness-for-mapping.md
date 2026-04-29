---
title: Verify that Service Mapping is set up properly
description: Before you start mapping application services, verify that you configured MID Servers to discover application services and provided all the necessary host and application credentials.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Verify that Service Mapping is set up properly

Before you start mapping application services, verify that you configured MID Servers to discover application services and provided all the necessary host and application credentials.

## Before you begin

To check readiness of mapping based on Predictive Intelligence, [install Service Mapping Plus](install-service-mapping-plus.md) from ServiceNow Store.

Role required: service\_mapping\_admin

## About this task

Service Mapping performs an automatic scan of the following resources and configurations to give you the readiness status:

-   \(Mandatory\) There are MID Servers with correctly configured IP ranges and the applications and capabilities settings. For more information, see [MID Server configuration for Service Mapping](../concept/configure-mid-service-mapping.md).

    If this check does not recognize correctly configured MID Servers, you cannot perform the bulk discovery.

-   \(Optional\) There are credentials for operating systems and applications as described in [Prerequisites for performing top-down discovery using Service Mapping](../reference/prerequisites-service-mapping.md).
-   \(Optional\) There are at least three load balancers recently discovered during horizontal discovery.
-   \(Optional\) There are at least 100 hosts discovered by the horizontal discovery in the last 14 days.
-   \(Optional\) The data collection using Netflow or VPC Flow Logs is configured. This configuration is necessary to enhance the traffic-based discovery in Service Mapping. For more information, see [Data collection and discovery using Netflow](../concept/data-collection-netflow-mapping.md) and [Data collection and discovery using VPC Flow Logs](../concept/data-collection-vpc-mapping.md).
-   \(Optional\) Cloud Discovery is activated and configured. This setting is necessary to discover application service based on IaaS.

If an optional resource or configuration is missing, you can still map application service, but it may result in partial discovery of some CIs and connections.

In addition, Service Mapping performs the readiness check for mapping functionality based on Predictive Intelligence.

## Procedure

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

    The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

2.  Verify that Service Mapping is set up and ready for discovery.

    If some obligatory configurations are missing, the error displays at the top of the window.

    1.  Click the link in the error or click the **Readiness Checklist** icon \(![Readiness Checklist icon](../image/ReadinessChecklistErrorIcon.png)\).

    2.  In the Service Mapping Readiness Checklist window, click the link next to the setup category with the error icon \(![Error icon](../image/BulkMappingSetupErrorIcon.png)\).

        You cannot perform discovery and mapping unless there are no errors in the Readiness Checklist window.

    3.  Perform the necessary action to complete the setup.

        For example, configure missing credentials.

3.  If more than one setup category has an error, return to the Readiness Checklist window and fix any other errors.

4.  Verify that Service Mapping is ready for discovery based on Predictive Intelligence.

    1.  Navigate to **Workspaces** &gt; **Service Mapping**, and then select **Application Service Readiness** icon ![](../image/icon-clipboard-check.png).

    2.  Verify that all items in the **Prerequisites status** list are in the **Ready** state.

        If any prerequisites are not fulfilled, perform the necessary procedure, and then select **Check readiness**.


## What to do next

[Map business services in bulk](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Application service readiness dashboard in configurable workspace](../reference/readiness-dashboard-ml.md)

