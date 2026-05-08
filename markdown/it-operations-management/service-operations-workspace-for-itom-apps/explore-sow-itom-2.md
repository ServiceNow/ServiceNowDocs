---
title: Exploring Service Operations Workspace for ITOM 2
description: Discover how operators use Service Operations Workspace for ITOM in daily workflows and how administrators configure the workspace to support efficient alert management and operational processes.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 4
keywords: [SOW configuration, SOW ITOM admin setup]
breadcrumb: [Exploring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Exploring Service Operations Workspace for ITOM 2

Discover how operators use Service Operations Workspace for ITOM in daily workflows and how administrators configure the workspace to support efficient alert management and operational processes.

## Overview of operational usage and configuration

Service Operations Workspace for ITOM serves as a centralized platform where operators manage daily alert workflows while administrators configure the workspace to optimize operational efficiency.

Administrators establish the foundation by configuring workspace layouts, alert automation rules, and integration settings. Operators then leverage these configurations to efficiently triage alerts, investigate issues, and coordinate responses. This collaborative approach ensures that the workspace adapts to organizational needs while maintaining operational consistency.

The workspace integrates capabilities from Event Management, Health Log Analytics, Now Assist for ITOM, and other AIOps applications to provide unified operational intelligence. This integration enables proactive issue detection, intelligent alert correlation, and AI-powered insights that transform reactive operations into predictive service management.

## Administrator configuration workflows

Administrators play a crucial role in establishing and maintaining the Service Operations Workspace environment. Their configuration activities directly impact operator efficiency and organizational alert management capabilities.

-   **Workspace layout configuration**

    Administrators customize dashboard layouts, configure widget arrangements, and establish default views that align with operational priorities. This includes setting up service dashboards, alert lists, and integration panels to match team workflows.

-   **Alert automation setup**

    Configure automated alert processing rules, including alert grouping criteria, escalation policies, and response automation. Administrators establish thresholds and conditions that determine how alerts are categorized and routed to appropriate teams.

-   **Integration management**

    Set up and maintain connections to external monitoring tools, configure data ingestion pipelines, and establish integration mappings. This includes configuring Agent Client Collector for infrastructure monitoring, Service Observability for application performance data, and various third-party integrations through the Integrations Launchpad. These configurations promote that alert data flows seamlessly from various sources into the unified workspace.

-   **AI and automation configuration**

    Configure Now Assist for ITOM capabilities including alert summarization, incident analysis, and automated response workflows. Administrators set up AI agent configurations, define automation triggers, and establish approval workflows for AI-recommended actions. This includes configuring agentic workflows for alert triage and autonomous operator assistance.

-   **Role and permission configuration**

    Define user roles, establish access controls, and configure permission levels that align with organizational security policies. Administrators promote that operators have appropriate access to Health Log Analytics, Service Reliability Management, and other integrated tools needed for their responsibilities.

-   **Performance optimization**

    Monitor workspace performance, configure caching settings, and optimize query parameters to promote responsive user experiences. Regular performance tuning helps maintain efficiency as data volumes and user activity increase across the organization.


## Operator daily workflows

Operators use the configured Service Operations Workspace environment to manage their daily responsibilities, leveraging the administrative setup to efficiently handle alerts and coordinate responses. A typical operational shift demonstrates how the workspace transforms reactive firefighting into proactive, intelligent operations management.

1.  **Morning briefing and prioritization:** Operators begin their shift by reviewing the workspace dashboard to understand current alert status, identify high-priority issues, and assess overall system health based on configured metrics and thresholds. The unified dashboard consolidates alert prioritization, service health overviews, trending anomalies, and predicted issues into a single view, eliminating the need to check multiple monitoring tools.
2.  **Alert triage and investigation:** Using the configured alert lists and filtering options, operators systematically review new alerts, apply established triage criteria, and initiate investigations using integrated tools and historical data. Now Assist for ITOM provides AI-powered alert analysis, summarization, and recommended actions to accelerate triage decisions.
3.  **Collaborative problem-solving:** Operators leverage workspace collaboration features to communicate with team members, share findings, and coordinate response efforts directly within the alert context. Integration with Service Reliability Management enables structured incident response workflows and automated escalation procedures.
4.  **Response execution:** Following established procedures and using configured automation tools, operators execute response actions, apply fixes, and monitor resolution progress through the workspace interface. Agentic workflows can autonomously execute approved remediation actions while maintaining human oversight for complex scenarios.
5.  **Documentation and handoff:** Operators document their actions, update alert status, and prepare handoff information for subsequent shifts, ensuring continuity of operations.
6.  **Continuous monitoring:** Throughout their shift, operators monitor workspace notifications, respond to new alerts, and maintain situational awareness using configured dashboards and real time updates.

## Users

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
</table>## Operational and configuration benefits

-   **Streamlined configuration management**

    Centralized configuration interface enables administrators to efficiently manage workspace settings, reducing setup time and ensuring consistent configurations across teams and environments.

-   **Enhanced operator productivity**

    Optimized workspace layouts and automated workflows reduce manual tasks, enabling operators to focus on high-value activities such as root cause analysis and strategic problem-solving. AI-powered alert summarization and automated incident creation reduce time spent on routine tasks by up to 60%.

-   **Improved operational visibility**

    Configurable dashboards and real-time monitoring capabilities provide operators with comprehensive situational awareness, supporting faster decision-making and more effective incident response.

-   **Flexible workflow adaptation**

    Administrative configuration options allow organizations to tailor workflows to specific operational requirements, accommodating diverse team structures and process variations.

-   **Scalable operations support**

    Configuration flexibility and automation capabilities enable organizations to scale operations efficiently, accommodating growth in alert volumes and operational complexity without proportional increases in staffing. Organizations typically achieve 3x infrastructure management capacity with the same team size through intelligent automation and streamlined workflows.


**Related topics**  


[bundle-platux.list-of-workspaces]

