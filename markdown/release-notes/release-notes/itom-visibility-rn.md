---
title: ITOM Visibility release notes
description: The ServiceNow ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# ITOM Visibility release notes

The ServiceNow® ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Australia release.

## About ITOM Visibility

-   Discovery: Power Shell 7 support for Discovery.
-   Kubernetes Visibility Agent \(KVA\) and Service Mapping: Create service maps for extended services beyond Kubernetes.
-   AI Agent Topology Mapping: Discover AI agent infrastructure and dependencies using the new AI Agent Topology Mapping application, including:
    -   Amazon Bedrock AI agents, models, and prompts
    -   Microsoft Foundry \(Classic\) AI agents, models, and prompts
-   Cryptographic Asset Compliance: Inventory, assess, and manage cryptographic assets, including certificates and keys, across cloud and on-premises environments to support post-quantum cryptography \(PQC\) readiness and maintain security compliance.

-   **Store updates for ITOM Visibility**

    The majority of Visibility apps are updated monthly or quarterly via the ServiceNow Store. The latest updates are available in the ServiceNow Store. For cumulative release notes and compatibility information, see the ServiceNow Store version details.

    -   [Cryptographic Asset Compliance](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-advanced.html)

        Cryptographic Asset Compliance is a part of the ITOM - Advanced app. This app helps you manage cryptographic assets, including certificates and cloud keys \(AWS KMS and Azure Key Vault\) discovered across on-premises and cloud environments from a centralized inventory. You can identify at-risk cryptographic assets with policy-based risk indicators and focus remediation efforts where they matter most.

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

    -   [Learning Enhanced Automation Playbook \(LEAP\)](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-leap.html)

        The Learning Enhanced Automation Playbook \(LEAP\) application uses AI to analyze incident data and facilitate the creation of automation that resolves high-impact issues for Service Operations teams. By leveraging data-driven analytics to accurately identify critical incidents, LEAP enables a more proactive problem management approach.

    -   [AI Agent Topology Mapping](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-agent-topology-mapping.html)

        Get transparency and oversight of AI agents, including clear tracking of their business ownership.


See [ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/t_ActivateTheDiscoveryPlugin.md) and [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/t_ActivateServiceMappingPlugin.md). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store..


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-operations-management-rn-landing.md)

