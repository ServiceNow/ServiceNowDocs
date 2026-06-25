---
title: Admin configuration use case for AIOps
description: Learn how IT administrators configure and optimize ITOM AIOps for enterprise environments. This use case demonstrates the setup journey for a multi-cloud financial services organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-health-admin-config-use-case.html
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 5
keywords: [ITOM Health, admin configuration, AIOps setup, Event Management, Service Operations Workspace]
breadcrumb: [Explore, ITOM AIOps, IT Operations Management]
---

# Admin configuration use case for AIOps

Learn how IT administrators configure and optimize ITOM AIOps for enterprise environments. This use case demonstrates the setup journey for a multi-cloud financial services organization.

This use case demonstrates how IT administrators configure ITOM AIOps to transform operations from reactive to proactive. The scenario follows an IT administrator implementing AIOps capabilities for a global financial services company with hybrid cloud infrastructure.

## Configuration scenario

The IT administrator is responsible for implementing ITOM AIOps across a complex environment including on-premises data centers and cloud services. The organization runs critical trading applications, customer-facing banking services, and internal business systems that require 99.9% availability.

The configuration goals include reducing alert noise, enabling predictive issue detection, and providing unified visibility across all environments. The goals also include empowering NOC operators with intelligent workflows and AI-powered insights.

## Phase 1: Event sources and intelligent correlation

The administrator configures Event Management to aggregate and intelligently correlate alerts from multiple monitoring tools and data sources.

-   **Event source integration**

    The administrator integrates existing monitoring tools including network monitoring systems, application performance monitoring platforms, and infrastructure monitoring solutions. The administrator also integrates cloud-native monitoring services. Each integration is configured with appropriate event parsing rules and severity mappings.

-   **Correlation rules configuration**

    Intelligent correlation rules are established based on CMDB relationships, time-based patterns, and business service dependencies. The administrator configures advanced correlation algorithms that consolidate related infrastructure alerts into a single root cause alert.

-   **Alert prioritization**

    Trading system alerts are automatically designated as Priority 1 with immediate escalation during market hours. Customer-facing banking services receive Priority 2 classification with 15-minute response requirements. Internal tools receive lower priority during business hours with standard response times. Business service criticality scoring uses revenue impact, customer count, and regulatory requirements as weighting factors.


## Phase 2: Predictive analytics and machine learning

The administrator configures advanced analytics capabilities that enable proactive issue detection and intelligent insights for operational teams.

-   **Health Log Analytics setup**

    HLA is configured to ingest log data from critical applications and infrastructure components. The administrator sets up log parsing rules, anomaly detection thresholds, and predictive models. These models learn normal operational patterns and identify deviations that indicate potential issues.

-   **Metric Intelligence configuration**

    Machine learning algorithms are trained on historical performance data to establish baseline behaviors for key metrics. The administrator configures anomaly detection sensitivity.

-   **Synthetic monitoring**

    Synthetic transactions are configured to continuously test critical user journeys through API endpoints. The administrator sets up monitoring with 5-minute frequency intervals.

-   **Service Reliability Management configuration**

    Service Reliability Management is configured to establish incident response workflows, collaboration channels, and automated remediation capabilities. The administrator sets up on-call schedules, escalation policies, and integration with communication platforms. This enables rapid response when alerts require immediate attention.

-   **Service Level Objective Management setup**

    SLO targets are defined for critical business services based on customer expectations and business requirements. The administrator configures SLO monitoring for availability, performance, and error rate metrics. The administrator establishes error budgets and burn rate alerts that provide early warning when services risk missing reliability targets.

-   **Service Observability integration**

    Service Observability is configured to combine Observability telemetry from external monitoring tools with CMDB relationship data. This data integration enables rapid identification of issues in specific microservices and their related entities without having to use an external tool.


## Phase 3: Unified workspace and user experience

The administrator configures the Service Operations Workspace to provide role-based dashboards and workflows that enable efficient operations management.

-   **Dashboard customization**

    Role-specific dashboards are created for different user types including NOC operators, incident managers, and executive stakeholders. Each dashboard displays relevant metrics, alerts, and service health information appropriate for the user's responsibilities and decision-making needs.

-   **Workflow integration**

    Automated workflows are configured for common operational scenarios including alert escalation, and notification routing. The administrator establishes integration with IT Service Management \(ITSM\) processes. This creates seamless handoffs between monitoring and service management.

-   **AI-Powered assistance**

    Now Assist for ITOM is configured to provide intelligent alert analysis, recommended actions, and contextual guidance. AI models use organization-specific knowledge including historical incident patterns, common error code translations, and proven remediation procedures to provide insights. Approval workflows are established for high-risk AI-recommended actions while allowing automatic execution of low-risk remediation steps.


## Phase 4: Performance tuning and optimization

After initial deployment, the administrator continuously optimizes the system based on operational feedback and performance data to maximize effectiveness and user adoption.

-   **Alert tuning**

    Based on operator feedback and false positive analysis, the administrator refines correlation rules and adjusts thresholds. The administrator optimizes alert prioritization to reduce noise while maintaining comprehensive coverage of critical issues.

-   **Machine learning model refinement**

    Anomaly detection models are tuned based on operational patterns and seasonal variations. The administrator adjusts sensitivity settings, incorporates feedback on false positives, and expands training data sets. This improves prediction accuracy.


## Configuration outcomes

The comprehensive ITOM AIOps configuration delivers measurable improvements in operational efficiency and service reliability:

-   **Alert reduction**

    Alert volume reduced through intelligent correlation and noise suppression

-   **Proactive detection**

    Critical issues identified and resolved before customer impact during typical operational shifts

-   **Faster resolution**

    Mean time to resolution reduced through AI-powered insights and automated workflows

-   **Unified visibility**

    Single pane of glass for hybrid cloud and on-premises infrastructure

-   **Predictive capabilities**

    Capacity issues and performance degradation predicted in advance

-   **Business alignment**

    Alert prioritization and impact analysis directly tied to business service criticality


This configuration enables the operational workflows demonstrated in the [NOC operator use case for AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/noc-operator-aiops-use-case.md). The configuration transforms reactive operations into intelligent, proactive service management.

**Related topics**  


[NOC operator use case for AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/noc-operator-aiops-use-case.md)

[ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md)

[Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/sow-landing-page-itom.md)

