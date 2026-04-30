---
title: Configuring Service Mapping
description: You get started with Service Mapping by configuring roles, credentials, and MID Server connections.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configuring Service Mapping

You get started with Service Mapping by configuring roles, credentials, and MID Server connections.

Setting up Service Mapping is the first stage in the Service Mapping workflow.

![Setting up Service Mapping in the workflow](../image/SMMapFlowSetup.png "Service Mapping workflow")

Service Mapping is part of the ServiceNow AI Platform and deploys some of its platform-wide mechanisms and features. At the same time, there are some configurations that are specific to Service Mapping only.

**Warning:** The Service Mapping setup for the Advance Release is different from the standard Service Mapping setup.

Perform the following tasks in the exact order they are listed below:

1.  [Request Service Mapping](../task/t_ActivateServiceMappingPlugin.md).
2.  [Install Service Mapping Plus](../task/install-service-mapping-plus.md).
3.  Install and configure MID Server. MID Servers, which are located in the enterprise private network, facilitate communication between servers on the network and some ServiceNow applications, such as Service Mapping, and Discovery. For more information, see [MID Server configuration for Service Mapping](configure-mid-service-mapping.md).
4.  Verify that [Discovery](../../discovery/reference/r-discovery.md) is set up and runs horizontal discovery as expected.
5.  Configure [credentials required for host discovery](../reference/r_Credentials4HostDiscovery.md).
6.  Configure credentials required for Service Mapping to access applications inside your organization private network. See [Prerequisites for performing top-down discovery using Service Mapping](../reference/prerequisites-service-mapping.md).
7.  If your organization network contains load balancers running on a Linux host, [create a discovery behavior for load balancers](../task/t_CreateDiscoBehavior4LB.md).
8.  Grant the following Service Mapping roles to relevant users:
    -   **service\_mapping\_admin**

        Sets up the Service Mapping application. Maps, fixes, and maintains service instances. Also performs advanced configuration and customization of the product. Assign this role to application administrators.

    -   **service\_mapping\_user**

        Views maps for operational service instances to plan change or migration, as well as analyze the continuity and availability of services. Assign this role to application users.

    -   **sm\_app\_owner**

        Provides information necessary for successful mapping of a service instance. Once a service is mapped, this user reviews the results and either approves it or suggests changes. Assign the sm\_app\_owner role to users who own service instances and are familiar with the infrastructure and applications that make up the services.

9.  [Verify that Service Mapping is set up properly](../task/check-service-mapping-readiness-for-mapping.md).
10. If your organization has a ServiceNow deployment with customized Discovery or CMDB attributes, perform additional configuration described in [KB0647574: Preparing customized ServiceNow deployments to work with Service Mapping](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsys_kb_id%3D334cd265db4a4fc0d7e37aa31f9619f7%26sysparm_stack%3D%26sysparm_view%3D).

In addition to the obligatory setup configurations described here, you may need to perform additional configurations after you complete the initial mapping process. For more information, see [Advanced Service Mapping configuration](c_ConfigureSM.md).

