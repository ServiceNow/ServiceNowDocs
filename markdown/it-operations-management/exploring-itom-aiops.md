---
title: Exploring ITOM AIOps
description: Overview of ITOM AIOps applications and capabilities that enable proactive IT operations management through AI-powered monitoring, analytics, and automation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 5
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

## ITOM AIOps users

|User|Description|
|----|-----------|
|||
| | |
| | |

## ITOM AIOps Benefits

Data collected and analyzed by ITOM AIOps provides intelligent insights that support the following business outcomes and operational workflows:

-   **Predictive Issue Detection**

    Identify potential problems before they impact users through predictive analytics and anomaly detection.

-   **Automated Incident Response**

    Streamline incident management with intelligent alert correlation, automated remediation actions, and context-aware notifications that reduce noise and accelerate resolution.

-   **Performance Optimization**

    Continuously monitor infrastructure health metrics and application performance to identify optimization opportunities and capacity planning requirements.

-   **Service Impact Analysis**

    Understand how infrastructure issues affect business services through service mapping and dependency analysis.

-   **Operational Intelligence**

    Gain actionable insights from log data, metrics, and events to improve operational efficiency and reduce the risk of service disruptions.

-   **Service Level Management**

    Define, monitor, and maintain service level objectives that align IT operations with business requirements. Track service reliability metrics and receive automated alerts when services approach defined thresholds.


## ITOM AIOps workflow

Each AIOPs application focuses on specific aspects of IT operations while contributing to a unified AIOps platform.

![Typical flow through AIOps](../image/aiops_overview.png)

-   **Agent Client Collector**

    Monitors service availability and infrastructure performance in real time. Combined with Metric Intelligence, it establishes dynamic thresholds and detects anomalies that may indicate potential service outages before they occur.

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


##  benefits

|Benefit|Feature|Users|
|-------|-------|-----|
||||
| | | |
| | | |
| | | |
| | | |

## ITOM AIOps licensing and products

When you activate AIOps, you get a core set of applications that provide foundational monitoring and event management capabilities. Additional applications can be installed from the ServiceNow Store to extend these capabilities based on your specific requirements. The ServiceNow AI Platform® uses a licensing method where your organization is billed for using ITOM AIOps applications.

AIOps includes the following applications by default:

-   AIOps dashboard
-   Integration Launchpad
-   Alert Automation
-   ITOM/OT SU Licensing
-   Event Management Connectors
-   Event Management Core
-   Tag Based Alert Clustering Engine
-   Alert Rules Management
-   Metric Explorer
-   Performance analytics
-   Mid Server
-   Event Management and Service Mapping Core

Optional applications that extend AIOps capabilities are available from the ServiceNow Store and can be installed based on your operational requirements and use cases:

-   Agent Client Collector
-   Health Log Analytics
-   Service Observability
-   Service Reliability Management
-   SLO Management
-   Synthetic monitoring

The ServiceNow Product Documentation doesn't provide information on prices, packaging, or other details determined by your organization customer contract. For general information about licensing and subscriptions, see [ITOM/OT SU Licensing and subscriptions](itom-su-licensing-landing-page.md).

## What to know before you begin

Before implementing ITOM AIOps, verify that your instance has the necessary prerequisites and that you understand the configuration requirements for each application.

A well-populated Configuration Management Database \(CMDB\) is crucial to get the most out of AIOps. ITOM AIOps relies on accurate configuration item data to map events to infrastructure components, calculate service impact, and provide context for alert correlation. Use Discovery to populate your CMDB with current infrastructure data before activating AIOps applications.

Configure the MID Web Server extension to enable ITOM AIOps features. The MID Web Server is an extension that enables external clients to push metric data and events to the MID Server, which is required for Event Management, and many instances of Agent Client Collector, and Health Log Analytics.

IT Operations Management Guided Setup provides a sequence of tasks that help you configure IT Operations Management applications on your ServiceNow instance. To open IT Operations Management guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**. For more information about using the guided setup interface, see Using guided setup.

## What to explore next

To learn more about configuring and using ITOM AIOps, see:

-   -   -   
