---
title: AI Control Tower release notes
description: Version history for the AI Control Tower application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ai-control-tower.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# AI Control Tower release notes

Version history for the AI Control Tower application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.0 - September 2026**
    -   AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage.
    -   Inventory and Discovery
        -   Detect unsanctioned AI use with network detection \(Armis\) and endpoint detection \(ITOM ACC\), including model, user, department, and device details.
        -   Block AI services detected through ACC.
        -   An AI Inventory Enrichment Agent scans your inventory for incomplete records and suggests values to fill the gaps.
        -   New and enhanced connectors extend discovery to Microsoft Agent365, Azure AI Foundry, Copilot, and AWS.
    -   Govern
        -   Discovered AI systems are now risk-classified at the point of discovery, before they enter the managed workflow.
        -   An AI Risk &amp; Control Applicability Advisor recommends the most relevant risks and controls for each system, with rationale.
        -   Dynamic Playbook 2.0 tailors onboarding tasks to an asset's risk classification.
        -   ServiceNow-managed AI agents can now be published to Microsoft Agent365 and other external registries.
    -   Secure
        -   AI agent containment can be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\).
        -   Design-time security now covers AI agents, tools, MCP servers, and system prompts, not just AI models.
        -   The Veza connector now uses OAuth 2.0 for authentication.
    -   Monitor
        -   Configure trace data retention to fit your needs.
        -   View new latency and token-usage visualizations.
        -   Set evaluation metrics at the asset level.
        -   Use custom date ranges of up to 18 months for evaluation data.
    -   Measure
        -   Product owners can now view and work with just the AI systems and metrics that matter to them.
    -   Foundations
        -   Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant.
    -   For full details, see. AI Control Tower release notes
-   **Version 7.0.2 - August 2026 \(Australia\)**
    -   This application is available for customers entitled to the AI Control Tower for the Enterprise \(SU\) SKU.
    -   Discovery &amp; Inventory
        -   New: Multi-tenant credential support for hyperscaler connectors
        -   Changed:
            -   Enhanced asset enrichment with cloud-native metadata and AI system relationship mapping
            -   Relationship mapping with Business applications \(requires EA entitlement\)
            -   Simplified asset states and status which replaces lifecycle phase and lifecycle status in asset record view
        -   Removed: Legacy single-tenant discovery connectors
    -   Governance
        -   New:
            -   Pre-built compliance content — Ready-to-use pack of regulations, control objectives, and risk statements with Day-1 readiness for California and Colorado AI laws
            -   Common Controls Alignment across frameworks to avoid duplication
        -   Changed: Unified Task Experience streamlining navigation between playbook tasks for faster impact and risk assessments
        -   Removed:
            -   Manual control framework templates
            -   Security
        -   New:
            -   Data security and privacy enforcement rules integrated into AI system governance
            -   Compliance-aware data masking and redaction for regulated environments
    -   Changed:
        -   Security assessments now integrated into AI lifecycle workflows
        -   Enhanced visibility into data flow and AI model access patterns
-   **Version 5.2.2 - August 2026 \(Zurich\)**
    -   This application is available for customers entitled to the AI Control Tower for the Enterprise \(SU\) SKU.
    -   Discovery &amp; Inventory:
        -   New: Multi-tenant credential support for hyperscaler connectors
        -   Changed:
            -   Enhanced asset enrichment with cloud-native metadata and AI system relationship mapping
            -   Relationship mapping with Business applications \(requires EA entitlement\)
            -   Simplified asset states and status which replaces lifecycle phase and lifecycle status in asset record view
        -   Removed: Legacy single-tenant discovery connectors
    -   Governance:
        -   New:
            -   Pre-built compliance content — Ready-to-use pack of regulations, control objectives, and risk statements with Day-1 readiness for California and Colorado AI laws
            -   Common Controls Alignment across frameworks to avoid duplication
        -   Changed: Unified Task Experience streamlining navigation between playbook tasks for faster impact and risk assessments
        -   Removed:
            -   Manual control framework templates
            -   Security
        -   New:
            -   Data security and privacy enforcement rules integrated into AI system governance
            -   Compliance-aware data masking and redaction for regulated environments
        -   Changed:
            -   Security assessments now integrated into AI lifecycle workflows
            -   Enhanced visibility into data flow and AI model access patterns
-   **Version 6.0.0 - July 2026**
    -   New:
        -   Assign unique asset IDs for each asset
        -   Opt-in to model preview program
    -   Changed:
        -   Post-upgrade fix: Auto-flag existing active assets as "Managed" for AICT Enterprise SKU customers upgrading from pre-March release
        -   Simplified asset state and status values - replaces lifecycle states
-   **Version 5.1.0 - July 2026 \(Zurich\)**
    -   New:
        -   Assign unique asset IDs for each asset
        -   Opt-in to model preview program
    -   Changed:
        -   Post-upgrade fix: Auto-flag existing active assets as "Managed" for AICT Enterprise SKU customers upgrading from pre-March release
        -   Simplified asset state and status values - replaces lifecycle states
-   **Version 5.0.0 - June 2026**

    This is a "marker app" with no new functionality added; its purpose is to automatically trigger installation of other apps.

-   **Version 4.2.0 - May 2026**

    Changed: MIF Sync Jobs to support new CI Relationship entries for ServiceNow AI assetsFramework updates to support future enhancements and features

-   **Version 4.1.0 - April 2026**
    -   New:
        -   Updated plugin dependencies for product tier support
        -   Automation rules to move assets from Unmanaged to Managed assets
    -   Changed:
        -   Enhanced data model for MCP Server Asset Type
        -   Enhanced Product Model Category to support AI Worker as a new category for AI System asset type
-   **Version 4.0.0 - March 2026**

    Integrate new features for AI assets, intake processes and risk and compliance.

-   **Version 3.0.0 - December 2025**
    -   New:
        -   Discovery: Connectors for
            -   Microsoft Foundry \(Azure Machine Learning Services, AI Hub and Azure Cognitive Services\)
            -   Microsoft Copilot Studio
            -   GCP Vertex AI
        -   Change Management and Offboarding workflows for AI assets
        -   Audit logs to capture configuration changes
        -   Global Value templates repository
        -   Multiple risk assessments
        -   Data segregation to secure unauthorized data exposure and regulatory noncompliance risks
        -   Framework to manage and streamline adoption of content library for Risk
        -   Email-Driven AI Misuse / Inquiry Reporting
-   **Version 2.1.0 - September 2025**
    -   New: Impact summary for 3P model provider choices
    -   Updated: Enhancements to Value and Adoption dashboards
-   **Version 2.0.0 - August 2025**
    -   Highlights:
        -   Enhanced Product Owner experience with a personalized homepage and improved visibility into AI assets to simplify task management.
        -   Value management tools to manage AI investments
        -   Monitor performance, track progress, costs, project risks and issues, and make informed decisions related to your AI strategies, goals, and targets from the AI strategy tab.
        -   Evaluate AI productivity and adoption across the enterprise using defined value metrics and performance indicators to drive data-informed decisions and maximize AI impact.
        -   Access and security monitoring for ServiceNow AI Agents, especially around access issues, agents running as privileged users, and dormant agents
        -   Discover AI assets built and deployed in AWS Bedrock and Azure Foundry.
        -   Enable choice for 3rd party model providers powering ServiceNow skills and agents
        -   Access to aggregated risk scores to improve decision-making, manage risks, and ensure ethical and transparent AI practices
-   **Version 1.0.1 - May 2025**

    AI Control Tower enables enterprises to actively manage, optimize, govern, secure &amp; measure the value of their AI investments, ensuring performance, compliance, &amp; workforce transformation while seamlessly embedding AI into enterprise strategy. AI Control Tower centralized enterprise AI asset inventory, boosts efficiency in the AI development with automated workflows and embeds risk and compliance management in the AI asset lifecycle.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

