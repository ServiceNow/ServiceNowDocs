---
title: ITOM Visibility
description: The ServiceNow ITOM Visibility product consists of ServiceNow DiscoveryServiceNow Discovery is an automated process that continuously scans and identifies all the components within the IT infrastructure. It plays a crucial role in maintaining an accurate and up-to-date CMDB 360 with the information it finds., Firewall Audits and ReportingUse the Firewall Audits and Reporting application to explore and create an inventory of your firewall security policies, devices, device groups, and manager information. Additionally, you can initiate requests for new firewall rules through the Service Catalog application and conduct audits of firewall security policies within specified time frames., Certificate Inventory and ManagementWith Certificate Inventory and Management, you can discover, conduct an inventory, and proactively manage all TLS certificates. Certificate Inventory and Management supports IPv6, providing comprehensive coverage for your certificate management needs., Service MappingThe ServiceNow Service Mapping application discovers all application services in your organization and builds a comprehensive map of all devices, applications, and configuration profiles used in these application services., AI Agent Topology MappingWith AI Agent Topology Mapping, you can use patterns to identify AI infrastructure components across cloud platforms in your organization. Discover your AI agents, models, and prompts, and get centralized CMDB visibility to track security compliance and vulnerabilities across your AI deployments., ITOM Content ServiceServiceNow ITOM Content Service offers extensive visibility of products in your infrastructure. The classification of processes identified by Predictive Intelligence enables wider discovery and weekly updates of new configuration items in the CMDB. Use the Discovery Admin Workspace to review and manage ITOM Content Service suggestions., Tag GovernanceEffective tag management improves reporting and overall operations management efficiency. Use the ServiceNow Tag Governance app to identify and remediate on-premises or cloud resources that are inconsistent and don't comply with the tag policies of your organization., Cloud Discovery Workspace Cloud Discovery Workspace offers a comprehensive solution to manage the cloud operations of your organization., and Cloud License EstimatorCloud License Estimator enables you to get the estimated resource count for all the cloud resources that are eligible for licensing. applications. Discovery and Service Mapping give you a unified, connected view of your entire IT network and the services that it supports. The Service Graph Connectors and CMDB 360 applications provide data to ITOM Visibility.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [IT Operations Management]
---

# ITOM Visibility

The ServiceNow® ITOM Visibility product consists of ServiceNow® [Discovery](../../discovery/reference/r-discovery.md), [Firewall Audits and Reporting](../../discovery/reference/firewall-audit-reporting.md), [Certificate Inventory and Management](../../discovery/reference/cert-inventory-mgmt.md), [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md), [AI Agent Topology Mapping](../../ai-agent-topology-mapping/concept/ai-agent-topology-mapping-landing.md), [ITOM Content Service](../../discovery/concept/discovery-content-services.md), [Tag Governance](landing-page-tag-governance.md), [Cloud Discovery Workspace](../../cloud-operations-workspace/reference/cow-landing-page.md), and [Cloud License Estimator](../../cloud-license-estimator/Concept/cloud-license-estimator-landing.md) applications. Discovery and Service Mapping give you a unified, connected view of your entire IT network and the services that it supports. The [Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [CMDB 360](https://www.servicenow.com/docs/access?context=multisource-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) applications provide data to ITOM Visibility.

## Who uses ITOM Visibility

ITOM Visibility enables the IT departments of enterprises and cloud companies providing platform as a service to discover their IT resources.

ServiceNow® Configuration Management Database \(CMDB\) is not just an operational tool, it is a strategic necessity in today’s IT landscape. Maintaining an accurate and complete CMDB provides the foundation for maintaining critical services and drives multiple outcomes important to IT departments.

![ITOM Visibility discovers many things which are stored in the CMDB.](../image/itom-visibility.png)

Data collected by ITOM Visibility provides a foundation for operation of the following business units and products of ServiceNow AI Platform:

-   **[ITOM AIOps](itom-health-landing-page.md)**

    Use ITOM AIOps to track and maintain the health of services in your organization. ITOM AIOps gathers alerts from infrastructure events captured by third-party monitoring tools. It then uses IT-related information gathered by Discovery to map alerts to configuration items. Based on the collected information, ITOM AIOps provides dashboards showing a consolidated view of all service-impact events. You can also use ITOM AIOps to proactively analyze your IT infrastructure to spot issues and prevent service outages. Using advanced machine learning to analyze information about your IT infrastructure, the application automatically determines dynamic thresholds and identifies anomalies that may indicate potential service outages.

-   **[ITOM Optimization](itom-optimization-landing-page.md)**

    ITOM Optimization gives you tools to provision private and public cloud infrastructure and services and to achieve consistent management and cost visibility. The [Cloud Insights](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) application, available in the ServiceNow Store, helps you to analyze the full range of costs associated with cloud assets so you can identify and take action on opportunities to save money and optimize operations.

-   **[Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

    Understand the software running in your IT environment. Software Asset Management works together with the CMDB powered up by ITOM Visibility. Use Software Asset Management to track configurations that impact software license consumption across your IT environments and datacenter.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

    Efficiently diagnose and resolve issues related to the IT infrastructure by using near real-time data supplied by ITOM Visibility.

-   **[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

    Rely on the IT infrastructure discovered by ITOM Visibility to manage and deliver services to your users. See changes and incidents created and managed by IT Service Management applications in ITOM Visibility service maps.

-   **[Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=r_ITBusinessManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    Use data collected by ITOM Visibility to gain a comprehensive understanding of the applications used in your organization.

-   **[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=australia&pubname=australia-security-management&ft:locale=en-US)**

    View security incidents in the context of ITOM Visibility to find out which application services are at risk. Use this information to prioritize and resolve threats based on the impact they pose to your organization.


## How you use ITOM Visibility

The Discovery feature offers a replicable and reliable method of identifying the enterprise IT infrastructure. Discovery can find computers, servers, software, printers, routers, and switches. It can also find IP-enabled devices and applications that run on them, resources from various cloud providers, and TLS certificates. This method is referred to as horizontal discovery. Connections between the devices and applications are not included in horizontal discovery.

The Service Mapping feature maps dependencies, based on a connection between devices and applications. This method is referred to as top-down mapping. The top-down mapping helps you immediately see the impact of a problematic object on the rest of the application service operation. Application service maps show infrastructure objects and connections between them. Service Mapping regenerates application service maps regularly, to keep them updated and relevant. Any faulty objects are shown along with the devices and applications they affect, providing a visual clue of the state of the application service.

![Diagram showing results of horizontal discovery and top-down mapping results](../../service-mapping/image/horizontal-top-down-comparison.png "Comparison of horizontal discovery and top-down mapping results")

## How ITOM Visibility works

Discovery can use scripts to collect and process data on a host and then update the CMDB. Scripts that explore or investigate CIs on your network are called probes. Sensors are the scripts that parse the data returned from the probes. In addition, Discovery uses discovery patterns. A pattern is a sequence of operations whose purpose is to detect attributes of devices and applications and, when used by Service Mapping, their outbound connections.

Service Mapping can deploy different methods for creating application services. Discovery patterns are the main method used by Service Mapping. However, you can also map application services using tags, and traffic connections between devices and applications. For more information, see [Choose the right method for mapping application services](../../service-mapping/concept/choose-mapping-method.md).

## ITOM Visibility licensing

The ServiceNow AI Platform® uses a licensing method where your organization is billed for using ITOM Visibility applications. Licensing options can vary based on your organization’s agreement. The ServiceNow Product Documentation doesn't provide information on prices, packaging, or other details determined by your organization customer contract. For general information about licensing and subscriptions, see [ITOM/OT SU Licensing and subscriptions](itom-su-licensing-landing-page.md).

## What to know before you begin

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](../../discovery/task/t_ActivateTheDiscoveryPlugin.md) and [Request Service Mapping](../../service-mapping/task/t_ActivateServiceMappingPlugin.md). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store.

Define users and configure credentials to enable ITOM Visibility access to applications and devices inside your organization network. For details, see [Prerequisites for performing top-down discovery using Service Mapping](../../service-mapping/reference/prerequisites-service-mapping.md).

