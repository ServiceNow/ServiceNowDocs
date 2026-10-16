---
title: AI Control Tower for Enterprise AI Foundation release notes
description: Version history for the ServiceNow AI Control Tower for Enterprise AI Foundation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-ai-control-tower-enterprise-ai-foundation.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# AI Control Tower for Enterprise AI Foundation release notes

Version history for the ServiceNow® AI Control Tower for Enterprise AI Foundation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.5 - October 2026**

    AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage.

    Secure:

    -   New: AI Security Operator role — lets teams delegate agent containment \(deactivate/reinstate\) without granting full AI Steward access.
    -   Changed
        -   Smarter Overview recommendations — "Your top recommendations" now ranks agents by critical security events \(with agent name, event count, and threat categories\); Overview and Post-runtime event lists are now consistent with each other.
        -   On the Overview tab, the Access issues detailed view includes a description that explains each access issue in plain language — identifying the agent, the operation, the resource, and the denial count.
        -   On the Runtime tab, Sensitive data metrics are shown for ServiceNow AI systems in a domain-separated instance.
        -   In Settings &gt; Rules and templates &gt; Security , the default values for Sampling rate and Max skill calls have changed on the External AI systems tab to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric isn’t affected. After upgrading, check your Sampling rate and Max skill calls settings and adjust if needed.
    -   Fixed
        -   In Policies, AWS Bedrock block and unblock actions fail without an error message when they don't succeed. \(PRB2077055\)
        -   After navigating to the Security page, tabs from the previous page were sometimes still shown until the page was refreshed. \(PRB2063965\)
        -   Selecting View source record from a security event's source log opened the underlying trace record directly, instead of the related page in Monitoring &gt; Traces. \(PRB2075468\)
        -   In the legacy UI experience, some users couldn't see the Security and Privacy tab. \(PRB2090102\)
        -   Security fixes
    -   Removed: The base system Traceloop Warehouse HTTPS connection \(sn\_ai\_security.Traceloop\_API alias\) is removed. If you're upgrading and use Traceloop-based external AI metrics, create a new HTTPS connection under that alias and re-create your credential with connection URL
    Monitor:

    -   Changed
        -   Go directly to the traces where a mismatch was detected from the AI agent usage deviates from declared purpose recommendation. Previously, the recommendation opened the parent asset record.
        -   A new recommendation groups AI agent quality and safety score drops by severity level, so related drops across multiple assets appear on a single card rather than one card per asset.
        -   Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.
        -   View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.
        -   Toggle between input and output when viewing trace details.
        -   Widget customization capability support across ALL AICT pages
    Measure:

    -   New
        -   Sub-vendor AI costs: Set a rate for a specific service from an integrated vendor, such as an agent platform. The sub-vendor rate takes precedence over the vendor rate. The vendor rate applies to any usage that doesn't have a sub-vendor rate.
        -   Subscription AI costs: Record per-seat subscription costs for integrated and non-integrated vendors. Specify the number of licensed seats, the cost per seat, and the contract dates. Optionally, add a one-time setup fee and distribute it over a set number of months so that it's included in the estimated monthly cost.
    -   Changed:
        -   Assign costs to specific services from integrated vendors.
        -   Include per-seat subscription costs in AI cost tracking.
-   **Version 1.9.2 - September 2026**
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
    -   Measure: Product owners can now view and work with just the AI systems and metrics that matter to them.
    -   Foundations: Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant.
    -   For full details, see.AI Control Tower release notes
-   **Version 1.8.3 - August 2026 \(Australia\)**
    -   This application is available for customers entitled to the AI Control Tower for the Enterprise Foundation SKU.
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
            -   New AI-enabled Risk &amp; Compliance conversational experience with action-based navigation and AI skills for task prioritization and control recommendations
            -   Common Controls Alignment across frameworks to avoid duplication
        -   Changed:
            -   Unified Task Experience streamlining navigation between playbook tasks for faster impact and risk assessments
            -   Enhanced control recommendation engine powered by AI
        -   Removed: Manual control framework templates
    -   Security
        -   New:
            -   Data security and privacy enforcement rules integrated into AI system governance
            -   Real-time anomaly detection and alert capabilities for AI model behavior
            -   Compliance-aware data masking and redaction for regulated environments
        -   Changed:
            -   Security assessments now integrated into AI lifecycle workflows
            -   Enhanced visibility into data flow and AI model access patterns
    -   Monitoring &amp; Value
        -   New:
            -   Continuous Controls Monitoring using LLM-as-a-judge for quality and safety scoring by metric and weight per AI system type
            -   Customizable evaluation templates for agent performance tracking
            -   Real-time productivity insights with cost per execution \(input/output tokens, total tokens breakdown by session/trace/span\)
            -   AI-generated insights for automatic triage and troubleshooting of low-scoring agents
            -   Agent auto-discovery from observability logs to keep inventory current
        -   Changed:
            -   Performance trend tracking with frequency visualizations integrated into agent asset records
            -   Value templates now support real-time quality scores as acceptance rates for productivity calculations
            -   Sampling rate customization \(1% to 100%\) by metric for flexible observability coverage
        -   Retired:
            -   Static evaluation frameworks
            -   Manual agent scoring processes
    -   AI Native Experience
        -   New:
            -   Insights and recommendations framework
            -   Duplicate asset detection insights and mark as duplicates
-   **Version 1.2.1 - July 2026**
    -   New: Now Assist powers new agentic and Gen AI capabilities in AI Risk and Compliance, providing built-in regulatory alignment and ethical AI governance for responsible deployment.
    -   Changed: All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.
-   **Version 1.1.1 - June 2026**
    -   New:
        -   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
        -   View the entity, risk, and control for each assessment directly in task and work queue lists, without opening individual records.
        -   Access authority documents, agency mappings, and citations for additional AI regulatory frameworks in the AI Risk and Compliance content pack.
    -   Changed: Added automated impact assessment flow whenever an AI Dataset is created.
    -   Fixed:
        -   Localization &amp; Performance issues are fixed.
        -   Fixed issue w.r.t to retired controls. Retired controls are excluded from the control based widgets.
        -   Fixed issue related to synchronization of AI asset life cycle tasks between AI Risk and Compliance and AICT workspace.
        -   Fixed functional domain issue w.r.t indicators feature on AI asset record page.
-   **Version 1.0.2 - April 2026**

    The AI Control Tower for Enterprise AI Foundation plug-in acts as a digital identifier, specifically designed to represent and validate the customer's licensing tier.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

