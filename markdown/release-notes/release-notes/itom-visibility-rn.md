---
title: ITOM Visibility release notes
description: The ServiceNow ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# ITOM Visibility release notes

The ServiceNow® ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Australia release.

## ITOM Visibility highlights for the Australia release

-   Discovery: Power Shell 7 support for Discovery.
-   Kubernetes Visibility Agent \(KVA\) and Service Mapping: Create service maps for extended services beyond Kubernetes.
-   AI Agent Topology Mapping: Discover AI agent infrastructure and dependencies using the new AI Agent Topology Mapping application, including:
    -   Amazon Bedrock AI agents, models, and prompts
    -   Microsoft Foundry \(Classic\) AI agents, models, and prompts

-   **Store updates for ITOM Visibility**

    The majority of Visibility apps are updated monthly or quarterly via the ServiceNow Store. The latest updates are available in the ServiceNow Store. For cumulative release notes and compatibility information, see the ServiceNow Store version details.

    -   [Service Mapping Plus](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-mapping-plus.html)

        Multi-Source Service Mapping – gain a single, trusted view of your services by eliminating fragmented maps and blind spots across discovery and service mapping methods. Unify top-down, tag-based, and ML-powered services into composite service maps.

    -   [AI-Powered Service Mapping](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html)

        Two AI Agents automatically generate service maps from ML candidates and connect Business Applications to discovered Application Services, eliminating manual CSDM relationship maintenance at scale. Available starting with Australia Patch 2.

        Use the Service Mapping MCP tools to query live service topology, relationships, and CI data through a conversational interface via Claude Desktop. Available starting with Australia Patch 3.

    -   [Discovery Admin Workspace](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-discovery-admin-workspace.html)

        Expanded Cloud support to include Alibaba, IBM, OCI, OpenStack, oVirt, and Vmware. New dashboards: URL Discovery Insights, Discovery Operations Monitor. Create discovery schedules automatically using integration with IP Address Management \(IPAM\) systems. Create discovery schedules for multi-cloud deployments. Improve security posture for Discovery. Receive real-time alerts including Discovery Schedule failures, Anomaly detection, MID down and Automated discovery schedule in Microsoft Teams and Outlook. Improve security posture for Discovery.

    -   [Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-patterns.html)

        New CI classes and fields for NSX infrastructure. Scan container repositories not reachable through a proxy using the new system property "sn\_itom\_pattern.container\_image\_scan\_no\_proxy". Container image scanning now supports MID Server selection per datacenter for private repositories. Multiple fixes and improvements for patterns for cloud and on premise discovery.

    -   [Certificate Inventory and Management](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cert-inv-mgmt.html)

        Seamless certificate renewal via Microsoft Outlook and CMDB Data Certification for TLS certificates.

    -   [Kubernetes Visibility Agent](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-kubernetes-visibility-agent.html) and [Agent Client Collector for Visibility](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-visibility.html)

        Increase visibility and control over Kubernetes environments: Service maps for Kubernetes and all related service resources, service maps for micro-services, KubeVirt VMs added to the CMDB, CI visualization. KVA is supported in OKE \(Oracle Kubernetes Engine\).

    -   [Service Graph Connector for AWS](https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-aws.html)
    -   [Service Graph Connector for Microsoft Azure](https://www.servicenow.com/docs/r/store-release-notes/store/platform-c/store-platcap-rn-service-graph-connector-ms-azure.html)

        Resource types aren't dynamically populated in the allowlist.

    -   [Service Graph Connector for GCP](https://www.servicenow.com/docs/r/store-release-notes/page/release-notes/store/platform-capabilities/store-platcap-rn-service-graph-connector-gcp.html)

        The Project Number field is populated in the GCP Project \[cmdb\_ci\_gcp\_project\] table, enabling the quick identification of GCP projects when searching by project number.

    -   [Tag Governance](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-tag-governance.html)

        Enhanced functionality for better visualization and navigation.

    -   [Learning Enhanced Automation Playbook \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap.md)

        The Learning Enhanced Automation Playbook \(LEAP\) application uses AI to analyze incident data and facilitate the creation of automations that resolve high-impact issues for Service Operations teams. By leveraging data-driven analytics to accurately identify critical incidents, LEAP enables a more proactive problem management approach.

    -   [AI Agent Topology Mapping](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-agent-topology-mapping.html)

        Get transparency and oversight of AI agents, including clear tracking of their business ownership.


See [ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility-landing-page.md) for more information.

## New in the Australia release

-   **Install ITOM Visibility apps using Now Assist for Setup**

    Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.


-   **[PowerShell 7 support for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/powershell-remoting.md)**

    Discovery now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Discovery on Code Signing instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/code-sign-disco-probes.md)**

    Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.

-   **[Discovery generic attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/disco-generic-attributes.md)**

    Enhance Configuration Management Database \(CMDB\) data accuracy with new Discovery capabilities that auto-populate non-discoverable attributes using a schedule-based mechanism. This update simplifies configuration item \(CI\) management by propagating generic attribute values across schedules and ranges, reducing manual effort and improving usability.

-   **[Use Kubernetes Visibility Agent \(KVA\) and Service Mapping to create service maps for extended services beyond Kubernetes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/mapping-k8s-sm-kva.md)**

    Service Mapping complements Kubernetes Visibility Agent \(KVA\) capabilities to map services that include Kubernetes and all related service resources beyond the Kubernetes environment. Install the latest version of Kubernetes Visibility Agent \(KVA\) to detect the latest changes in your Kubernetes cluster and run Service Mapping to have an up to date visualization of your services across Kubernetes and related resources.

-   **[Quick start tests for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/quick-start-tests-service-mapping.md)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping works as expected. If you customized Service Mapping, copy the quick start tests and configure them for your customizations.


## Deprecations

-   Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/t_ActivateTheDiscoveryPlugin.md) and [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/t_ActivateServiceMappingPlugin.md). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store..

## Plugin information

-   **New plugins**

    The following ServiceNow Store application is new in Australia:

    AI Agent Topology Mapping \(sn\_itom\_agnt\_ptrn\): Discovers and maps AI agents, large language models, and prompts across hyperscaler environments, and populates the CMDB with the results.


## Related ServiceNow applications and features

-   ****

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

    Event Management gathers alerts from infrastructure events that both third-party monitoring tools and the ServiceNow® internal agent capture. Event Management uses IT-related information that ServiceNow® Discovery gathers so it can map alerts to configuration items. Based on the collected information, Event Management then provides dashboards that show a consolidated view of all service-impact events.

    The Agent Client Collector application enables you to do the following:

    -   Monitor your service availability.
    -   Examine the health and performance of your environment.
    -   Ensure that your infrastructure and its applications are running properly.
    Agent Client Collector collects events and metrics. It runs in either a Windows or Linux environment.

-   **[ITOM Cloud Accelerate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-cloud-accelerate-landing-page.md)**

    ITOM Cloud Accelerate workflows streamline cloud automation across the cloud adoption journey via self-service catalogs and controlled workflows. It expedites application migration by facilitating assessment, planning, and resource migration tracking.

    ITOM Cloud Accelerate includes the following apps:

    -   Cloud Account Management
    -   Cloud Services Catalog
    -   Cloud Configuration Governance
    -   Cloud Action Library

-   **[MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-landing.md)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-operations-management-rn-landing.md)

