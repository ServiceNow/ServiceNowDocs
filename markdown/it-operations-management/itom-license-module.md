---
title: Subscriptions for IT Operations Management
description: The ServiceNow AI Platform uses a licensing method where your organization is billed for using the following IT Operations Management products: ServiceNow ITOM Visibility, ServiceNow ITOM Discovery, ServiceNow ITOM AIOps, ServiceNow Health Log Analytics, ServiceNow ITOM Optimization, and ServiceNow ITOM Cloud Accelerate.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Exploring ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Subscriptions for IT Operations Management

The ServiceNow AI Platform® uses a licensing method where your organization is billed for using the following IT Operations Management products: ServiceNow® ITOM Visibility, ServiceNow® ITOM Discovery, ServiceNow® ITOM AIOps, ServiceNow® Health Log Analytics, ServiceNow® ITOM Optimization, and ServiceNow® ITOM Cloud Accelerate.

For licensing purposes, licensable resources are assigned to CI categories. License usage is measured using subscription units, which may cover a different number of resources, depending on the resource CI category. The customer contract for your organization determines the CI categories from the available options, and also the ratios of CI allocation for subscription units in each CI category. Information from the customer contract is synchronized with the ServiceNow platform. The latest version of ServiceNow® ITOM/OT SU Licensing supports the following CI categories:

-   Containers
-   PaaS
-   FaaS
-   Servers
-   Unresolved Monitored Object
-   Unclassed category
-   End User Devices
-   IoT
-   Customer Prem Devices

You have the option to buy subscriptions for individual ITOM products separately \(a la carte\) or as part of a bundle with multiple products. You can also purchase both—a bundle subscription that covers most required applications and an a la carte subscription for applications that consume more subscription units. For more information, see [ITOM/OT SU Licensing subscription types](itom-licensing-subscription-types.md).

ServiceNow® charges for the following IT Operations Management products:

-   **ITOM Visibility**

    The ServiceNow® ITOM Visibility product consists of ServiceNow® [Discovery](../../discovery/reference/r-discovery.md), ServiceNow® [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md), Certificate Inventory and Management, Service Graph Connectors, CMDB 360, and Firewall Audits and Reporting. Discovery and Service Mapping give you a unified, connected view of your entire IT network and the services that it supports.

    In addition, Service Graph Connectors populate the CMDB by bringing in data from third-party monitoring and management systems. CMDB 360 enables you to track how the CMDB contains various discovery sources at the CI attribute level. Use Certificate Inventory and Management to avoid service outages due to expired TLS certificates. Firewall Audits and Reporting helps you to discover and manage your firewall security policies to heighten the security awareness for firewall audits.

    For licensing purposes, ITOM Visibility provides the CI count it discovers, both during horizontal and top-down discovery. It also reports CIs that the Service Graph Connectors populate the CMDB with.

    You can also use limited Tag Governance functionality under the ITOM Visibility subscription. You can identify on-premises resources that are inconsistent and don't comply with the tag policies of your organization.

-   **ITOM Discovery**

    ServiceNow® ITOM Discovery is an entry-level package alternative where customers can build a healthy data platform. This package measures licensed usage of the Discovery feature and Service Graph Connectors. Discovery is a "subset" of ITOM Visibility that is also based on subscription units. ITOM Discovery includes the following basic features: ServiceNow® Discovery, Service Graph Connectors, and CMDB 360. ServiceNow® Discovery finds applications and devices on your network, and then updates the CMDB. Service Graph Connectors supplement the population of the CMDB, while CMDB 360 retains the complete history of discovery sources and proposed values.

    ITOM Discovery provides the count of CIs found by ServiceNow® Discovery and brought in by Service Graph Connectors.

-   **ITOM AIOps**

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

    ITOM AIOps reports the number of CIs, where it captures alerts, events, and metric data. ITOM AIOps reports the CI count for all CI categories.

-   **Health Log Analytics**

    Health Log Analytics CI count is based on log data received from licensable resource types. The consumption is reflected in ITOM AIOps as well as in Health Log Analytics. For that reason, you need the ITOM AIOps subscription in addition to the Health Log Analytics subscription.

-   **ITOM Cloud Accelerate**

    The ITOM Cloud Accelerate product consists of the following workflow applications: Tag Governance, Cloud Migration Assessment, Cloud Configuration Governance, and Cloud Action Library. In Tag Governance, you can update CI tags in the cloud environment, in addition to updating them in the CMDB.

    For licensing purposes, the ITOM Cloud Accelerate license provides the CI count for CIs managed and monitored by Cloud Migration Assessment, Cloud Configuration Governance, or Cloud Action Library. If different ITOM Cloud Accelerate features report the same CIs as their resources, the CI count is manipulated to remove the duplication.

-   **ITOM Optimization**

    The ServiceNow® ITOM Optimization application provides automation for the cloud workflows used to manage the cloud resources throughout their life cycle. It enables certified and enterprise-compliant cloud deployment, cost visibility, and other cloud management processes.


-   **Service Observability**

    The ITOM Service Observability feature creates actionable dashboards and observability tabs that centralize data from existing third-party monitoring tools. It allows you to track the performance of business-critical services, enables faster root cause analysis, and reduces mean time to resolution \(MTTR\). Application and platform telemetry insights from multiple observability tools are combined into a centralized workflow.


**Parent Topic:**[Exploring ITOM/OT SU Licensing](explore-itom-licensing.md)

**Related topics**  


[Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

