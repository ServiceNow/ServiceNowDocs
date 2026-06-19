---
title: Exploring ITOM AIOps
description: Overview of ITOM AIOps applications and capabilities that enable proactive IT operations management through AI-powered monitoring, analytics, and automation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/exploring-itom-aiops.html
release: australia
product: IT Operations Management
classification: it-operations-management
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 6
keywords: [explore]
breadcrumb: [ITOM AIOps, IT Operations Management]
---

# Exploring ITOM AIOps

Overview of ITOM AIOps applications and capabilities that enable proactive IT operations management through AI-powered monitoring, analytics, and automation.

## ITOM AIOps overview

ITOM AIOps enables IT operations teams, site reliability engineers, and DevOps professionals to proactively monitor, analyze, and optimize the health and performance of their IT infrastructure and services.

ServiceNow® ITOM AIOps provides AIOps capabilities that transform how organizations manage IT operations. By combining advanced analytics, machine learning, and automation, ITOM AIOps helps teams avoid service outages, reduce mean time to resolution, and optimize infrastructure performance.

## Service Operations Workspace

Network Operations Center \(NOC\) operators and IT operations teams use Service Operations Workspace as their primary interface for managing IT operations powered by ITOM AIOps. The workspace consolidates alerts, incidents, and operational data from multiple AIOps applications into unified dashboards and workflows.

In their daily work, operators use the workspace to monitor service health across the entire IT infrastructure, investigate alerts with full context from multiple data sources, and coordinate response activities. The workspace presents correlated events, suggested remediation actions, and service impact information in a single interface, enabling operators to quickly understand and respond to issues.

The workspace integrates data from all AIOps products to provide operators with comprehensive situational awareness and streamlined incident management capabilities.

## ITOM AIOps workflow

Each AIOPs application focuses on specific aspects of IT operations while contributing to a unified AIOps platform.

-   **Agent Client Collector**

    Monitors service availability and infrastructure performance in real-time. Combined with Metric Intelligence, it establishes dynamic thresholds and detects anomalies that may indicate potential service outages before they occur.

-   **Synthetic monitoring**

    Monitors critical services by simulating user transactions on API endpoints, identifying performance bottlenecks and helping maintain optimal user experiences. It provides early warning of service degradation before real users are affected.

-   **Health Log Analytics**

    Collects log data in real time and uses machine learning to identify patterns and detect anomalies. It typically ingests logs through the MID Server, identifies normal operating patterns, and using Event Management, raises actionable alerts when it detects significant deviations that might indicate emerging issues.

-   **Event Management**

    Serves as the central nervous system for your IT operations. It receives alerts from monitoring tools and correlates related events to reduce noise. The system maps alerts to configuration items in the Configuration Management Database \(CMDB\) and calculates business impact using service dependencies from Service Mapping. This correlation transforms hundreds of individual alerts into prioritized, context-rich incidents that focus teams on the most critical issues.

-   **Express List**

    Is the SOW view into Event Management, allowing operators to efficiently monitor systems and services,​ resolve alerts, evaluate the alert impact,​ track issues, and report incidents.

-   **Service Observability**

    Combines external observability telemetry with Configuration Management Database \(CMDB\) data, to reveal dependencies that may not be obvious from individual alerts. Charts provide critical insights by showing how infrastructure components may be affecting a single service.

-   **Service Reliability Management**

    Enables teams to respond to incidents with structured workflows, automated escalation, and collaborative tools that streamline incident response.

-   **SLO Management**

    Helps organizations define, monitor, and report on service level objectives and service level indicators. It provides automated SLO tracking and alerting when services approach or breach defined thresholds, enabling proactive service quality management.


## ITOM AIOps users

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin\[evt\_mgmt\_admin\]

</td><td>

Configures and sets up Event Management properties and rules.

</td></tr><tr><td>

Operator\[evt\_mgmt\_operator\]

</td><td>

Manages alerts, including closing and acknowledging them.

</td></tr><tr><td>

User\[evt\_mgmt\_user\]

</td><td>

Manages the lifecycle of alerts, including performing basic operations such as viewing and acknowledging them.

</td></tr></tbody>
</table>## ITOM AIOps benefits

<table id="table_qx2_hdt_y3c"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Predictive issue detection

</td><td>

-   [Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-landing-page.md)
-   [Synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/synthetic-monitoring-landing-page.md)

</td><td>

Admin, operator

</td></tr><tr><td>

Automated alert response

</td><td>

[Alert automation in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/sow-itom-alert-automation.md)

</td><td>

Admin

</td></tr><tr><td>

Performance optimization

</td><td>

[Exploring Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/exploring-agent-client-collector.md)

</td><td>

Admin, operator

</td></tr><tr><td>

Service health and investigation

</td><td>

[Exploring Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/exploring-service-observability.md)

</td><td>

Admin, operator

</td></tr><tr><td>

Service level management

</td><td>

-   [Exploring Service Reliability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/exploring-service-reliability-management.md)
-   [Exploring SLO Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/exploring-service-level-objective-management.md)

</td><td>

Admin, operator

</td></tr></tbody>
</table>## Products that add value to ITOM AIOps

In the context of ITOM AIOps, which focuses on maintaining the health and performance of IT systems and infrastructure, there are several ServiceNow products that can add significant value:

-   **Discovery**

    Discovery automatically identify and collect information about IT assets, configurations, and relationships, providing organizations with a comprehensive inventory to effectively manage and monitor their IT infrastructure.

-   **Service Mapping**

    Service Mapping offers detailed information about application instance services within the \[cmdb\_ci\_service\_discovered\] table. This data helps establish connections between infrastructure and application configuration items \(CIs\) stored in the \[cmdb\_ci\_appl\] table, enhancing visibility into IT environments and facilitating efficient management and monitoring processes.

-   **Service Portfolio Management**

    Service Portfolio Management \(SPM\) offers the associated product model, while Software Asset Management \(SAM\) and Hardware Asset Management \(HAM\) provide life-cycle data for Technology Portfolio Management \(TPM\). Together, they enable comprehensive management of IT assets, ensuring effective utilization, compliance, and optimization throughout their life cycles.


## Products that benefit from ITOM AIOps

-   **Incident Management**

    Incident Management tools leverage downstream information from Event Management to create incidents swiftly, ensuring timely resolution of issues.

-   **Customer Service Management \(CSM\)**

    Customer Service Management \(CSM\) systems benefit from ITOM AIOps by utilizing application service impact data to identify affected users promptly, enhancing customer support efficiency and satisfaction.


## What to know before you begin

Before implementing ITOM AIOps, verify that your instance has the necessary prerequisites and that you understand the configuration requirements for each application.

A well-populated Configuration Management Database \(CMDB\) is crucial to get the most out of AIOps. ITOM AIOps relies on accurate configuration item data to map events to infrastructure components, calculate service impact, and provide context for alert correlation. Use Discovery to populate your CMDB with current infrastructure data before activating AIOps applications.

Configure the MID Web Server extension to enable ITOM AIOps features. The MID Web Server is an extension that enables external clients to push metric data and events to the MID Server, which is required for Event Management, and many instances of Agent Client Collector, and Health Log Analytics.

Setup Hub provides a sequence of tasks that help you configure Event Management on your ServiceNow instance. For more information about using the Setup Hub, see [Configure Event Management using Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/aiops-conf-console.md).

