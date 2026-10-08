---
title: AI Control Tower release notes
description: The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.The Australia Patch 7 release adds support for policy management improvements, improved monitoring visualizations, and more.This release adds support for domain separation, policies, quality and safety metrics for specific assets, and more.The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/ai-control-tower-rn.html
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 27
breadcrumb: [AI Experiences release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# AI Control Tower release notes

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

## About AI Control Tower

AI Control Tower highlights in Australia patch 6:

-   Apply policies to block AI activity and respond to AI threats.
-   Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.
-   Discard session, trace, and span data to reduce storage usage, while retaining quality and safety scores.
-   Use AI Control Tower on a domain-separated instance.
-   AI Inventory Intelligence Agent analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.
-   The GCP Vertex AI connector is renamed to Gemini Enterprise Platform Agent
-   The AI Service Graph Connector for GCP application is renamed to AI Service Graph Connector for Google.
-   The Salesforce connector is renamed to AI Connector for Salesforce.
-   The Microsoft connector introduces A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   Starting in the September 2026 release, AI Gateway is available in AI Control Tower.
-   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
-   The AI Gateway proxy URL format has changed. The new format is:

    `https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

    Previously, the URL format was:

    `https://<instance-url>/sncapps/awh/<mcp-server>/mcp`


AI Control Tower highlights in [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md):

-   Manage your AI governance work in a redesigned AI Control Tower experience that lets you find information and complete tasks using natural language.
-   Resolve important issues using auto-generated recommendations and AI insights that direct your attention to the AI governance work that matters most.
-   Detect quality and safety regressions in AI systems before they escalate, using automated scoring and trend analysis for AI interactions in production.
-   Use ServiceNow Otto premium chat in AI Control Tower for a better conversational experience with unified search and chat capabilities, including integrated web search and file uploads.
-   Contain rogue AI agents by using kill switch protocol to limit damage, preserve your security posture, and provide business continuity for your users.
-   Make a managed AI agent discoverable to external systems by publishing it to the External Registry. The Microsoft integration provides two methods to publish an agent so that Microsoft can discover it.
    -   Publish agents from the AI asset record page.
    -   Publish agents while onboarding an asset.
-   Detect AI assets in your inventory that perform the same function using deduplication. Deduplication enables AI stewards to review and consolidate redundant entries instead of governing them independently.
-   ServiceNow Otto is the new AI experience brand. This change is reflected in AI Control Tower. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The AI Control Tower home page includes a Guided Setup widget that walks you through the initial configuration of AI Control Tower.
-   AI Service Graph Connectors integrate with AI Control Tower to create AI connections for discovering AI assets and tracking data usage. For information about connectors, prerequisites, and the configuration process, see [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2986990) article in the Now Support Knowledge Base.
-   AI Service Graph Connectors and versions available for August 2026 release:
    -   AI Service Graph Connector for Microsoft \(version 3.1.7\)
    -   AI Service Graph Connector for GCP Vertex AI \(version 1.2.4\)
    -   AI Service Graph Connector for Anthropic \(version 2.0.7\)
-   Model Preview Program \(MPP\) is an opt-in program that gives eligible users an early access to AI models that aren't yet Generally Available \(GA\).

AI Control Tower \(legacy\) highlights in [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md):

-   The AI asset list in AI Inventory includes Asset State and Asset Status columns.
-   The system assigns a unique ID to every asset. The ID appears in the Asset tag field under Asset details.
-   AI Service Graph Connectors for OpenAI, Moveworks, IBM, and OCI are available in AI Control Tower for AI connections.
-   The AI Service Graph Connector for OpenAI discovers AI models and tracks model usage.
-   When you mark a managed asset as unmanaged, the asset's active workflows, tasks, and governance processes are canceled, and the asset is excluded from value tracking.
-   When you mark an unmanaged asset as managed, the asset is actively monitored and governed, making it visible and eligible for governance workflows and value tracking.

AI Control Tower \(legacy\) highlights in [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md):

-   Customize the AI asset security score calculation to reflect your security requirements.
-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance's AI Gateway.
-   Configure and create automation rules to set AI assets as managed assets.
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.

AI Control Tower \(legacy\) highlights in [Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-all-other-fixes.md):

-   AI assets—including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors \(SGC\).
-   The AI model providers supported by ServiceNow contains providers such as Now LLM Service, AWS Claude, Now LLM LTS model, and so on.
-   The AI model providers configured by your organization contains providers such as Perplexity, IBM Watson, and so on.
-   AI Gateway offers Global MCP clients, which once created can be used across all MCP servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers into AI Control Tower.

For more information on the new AI Control Tower experience, see [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md).

For more information on the legacy AI Control Tower experience, see [AI Control Tower \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-landing.md).

## Activation and other requirements

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/intelligent-experiences-rn-landing.md)

## Australia Patch 7

The Australia Patch 7 release adds support for policy management improvements, improved monitoring visualizations, and more.

### What's new

-   **[Monitor agent activity chart improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.

-   **[Session details improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-session-details.md)**

    View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.

-   **Connectors**

    Amazon Quick connector is a new connector which is part of discovering Systems, models, and prompts for creating AI connections.

-   **[Edit an Explicit Block policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-edit-explicit-block-policy.md)**

    Change who an Explicit Block policy blocks, what they're blocked from using, or its follow-up actions after the policy is published.

-   **[Block AI usage by department](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-create-explicit-block-policy.md)**

    Scope an Explicit Block policy to a department so everyone in that department is blocked from a specific AI agent, model, or domain.

-   **[Use new role to contain AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md)**

    Perform AI agent containment \(kill switch\) with the AI Security Operator role. You can deactivate an AI agent without requiring full AI Steward–level access.

-   **[Check whether the Security Analyzer agent is enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-ai-aict-security-analyzer-agent-ai-agent.md)**

    Check the status of the Security Analyzer agent which determines security event severity and insights for your top recommendations, data integrity incident detection, system prompt leakage, correctness detection, prompt injection, and agent goal deviation metrics. Available on the Security Insights tab in Settings &gt; Rules and templates &gt; Security.

-   **Sub-vendor AI costs**

    Set a rate for a specific service from an integrated vendor, such as an agent platform. The sub-vendor rate takes precedence over the vendor rate. The vendor rate applies to any usage that doesn't have a sub-vendor rate.

-   ****

    Record per-seat subscription costs for integrated and non-integrated vendors. Specify the number of licensed seats, the cost per seat, and the contract dates. Optionally, add a one-time setup fee and distribute it over a set number of months so that it's included in the estimated monthly cost.


### What's changed

-   **[View input and output in trace details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-session-details.md)**

    Toggle between input and output when viewing trace details.

-   **[Usability improvements to Security Overview metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-reference.md)**

    See only actionable items in your top recommendations on the Security Overview tab. In addition, the recommendations rank AI agent insights by number of critical security events and show the agent name, critical event count, and top threat categories. The security events list now matches the list on the Post-runtime tab. The Access issues detailed view includes a description that explains each access issue in plain language—identifying the agent, the operation, the resource, and the denial count.

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-domain-separation.md)**

    Review sensitive data metrics for ServiceNow AI systems in a domain-separated instance. Available on the Runtime tab in Security.

-   **[Configure Excessive Agency in Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

    Control whether Excessive Agency is enabled in Post-runtime configuration in Security. This setting controls data for Access issues and Privileged AI agents metrics, as well as post-runtime metrics. The setting is off by default.

-   **[Post-runtime Security probabilistic metrics and AI agent disabled by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

    To reduce token consumption, screening for data integrity incident detection, system prompt leakage, correctness detection, prompt injection, and agent goal deviation is disabled by default. In addition, the Security Analyzer agent that determines security event severity and insights is disabled by default. The default sampling rate for all metrics is 1%. If you're upgrading, your Detection enabled setting for each metric isn’t affected. After upgrading, check your settings in **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


### What's deprecated or removed

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Traceloop Warehouse HTTPS connection removed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.md)**

    The base system Traceloop Warehouse HTTPS connection \(sn\_ai\_security.Traceloop\_API alias\) is removed. If you're upgrading and use Traceloop-based external AI metrics, create a new HTTPS connection under that alias and re-create your credential with connection URL `https://api.traceloop.com`.


## Australia Patch 6

This release adds support for domain separation, policies, quality and safety metrics for specific assets, and more.

### What's new

-   **[Control AI asset usage through policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-landing.md)**

    Apply policies to block AI activity and respond to AI threats.

-   **[Add an Azure AI Foundry connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-azure-foundry-security-connection.md)**

    Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

-   **[Add metrics from the AI system record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-ai-system-metrics.md)**

    Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-external.md)**

    Add, remove, or adjust the sample rate of metrics for one or more external AI systems, without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.md)**

    Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

-   **[Exclude an AI system from a metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-exclude-ai-systems-external.md)**

    Exclude one or more AI systems from a specific metric, without changing that metric's configuration for every other system.

-   **[AI system performance metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-asset-monitor.md)**

    Monitor operational health at a glance, including average latency and token usage per session.

-   **[Latency and span counts for sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-evaluated-sessions-overview.md)**

    See each session's response time and span count in the evaluated sessions lists and on individual session detail pages.

-   **[Scoring bias indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Learn when a composite score might be skewed. See how many evaluations back each metric, and identify when uneven evaluation coverage is influencing the score more than the configured weight suggests.

-   **[Trace data retention controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-trace-retention.md)**

    Keep session, trace, and span data for up to 30 days for scoring, or discard it to reduce storage usage, with quality and safety scores staying available either way. Discarding also disables AI Skill Kit insights and hides the evaluated sessions views.

-   **[Custom date ranges for monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Analyze exactly the period you need by specifying an exact start and end date, up to 18 months apart.

-   **[Review AI security posture in design-time metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-reference.md)**

    Identify configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk with AI security posture metrics.

-   **[AI Inventory Intelligence Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/inventory-intelligence-agent.md)**

    AI Inventory Intelligence Agent automatically analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The Microsoft connector introduces the A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   **[Client registration and AI Gateway setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/client-registration.md)**
    -   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
    -   The AI Gateway proxy URL format has changed. The new format is:

        `https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

        Previously, the URL format was:

        `https://<instance-url>/sncapps/awh/<mcp-server>/mcp`


### What's changed

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-domain-separation.md)**

    Use AI Control Tower on a domain-separated instance. In Security, detail pages for some metrics include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured.

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-domain-separation.md)**

    Use AI Control Tower on a domain-separated instance. In Security, detail pages for some metrics include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured.

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **[Design-time metrics reorganized into subtabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-reference.md)**

    Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by asset source \(for example, ServiceNow or AWS Bedrock\).

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    On the Security tab for an AI asset, a metric isn't shown if there's no data available for the asset. Also, access issues and access posture don't appear for AI models.

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    AI agent containment using kill switch protocol is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity. It also supports retrying a failed or partial containment operation. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event.

-   **[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md)**

    The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   **[Add a Gemini Enterprise Agent Platform connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.md)**

    The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **[Agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md)**

    The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **[AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-gateway.md)**

    Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.

### What's deprecated or removed

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    AI Policy Framework \(sn\_ai\_policy\_framework\): Mitigate AI exposure through policies.


## Australia Patch 4

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

### What's new

-   **[Activity Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-activity-center.md)**

    Track and act on the governance work generated across AI Control Tower from a single workspace, including lifecycle tasks, security tasks, change and offboarding requests, and AI recommendations.

-   **[Recommendations and AI insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-recommendations-ai-insights.md)**

    Recommendations and AI insights direct your attention to the AI governance work that matters most, so you can resolve high-impact issues without searching for them. Act on recommendations from the Home page, an asset record, or Activity Center.

-   **[Monitor quality and safety for AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-landing.md)**

    Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.

-   **[Trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md)**

    Collect trace data for discovery, security, and monitoring from hyperscalers including AWS, Azure, and Google Cloud by configuring trace connections.

-   **[Plan AI strategy, prioritize, and execute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-planning-ai-strategy.md)**

    Track your AI portfolio from strategy to delivery with the Plan menu. Plan connects goal alignment, intake management, and execution tracking in a single workspace, giving portfolio managers and AI COE leads a current view of AI investments.

-   **[ServiceNow Otto in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-convrstn-support.md)**

    Use ServiceNow Otto premium chat in AI Control Tower for a better conversational experience with unified search and chat capabilities, including integrated web search and file uploads.

-   **[AI agent containment using kill switch protocol manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-exploring-ai-agent-containment.md)**

    Deactivate and reinstate AI agents running in AWS Bedrock, AWS Bedrock AgentCore, GCP Vertex AI \(limited support\), and ServiceNow agents. Revoke AI agent session tokens through Okta.

-   **[Discover your agent network with the map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-use-map.md)**

    See AI models, MCP servers, and providers in the agent map for complete resource visibility across your enterprise, along with agents, agentic workflows, and other AI assets.

-   **[Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

    System prompt leakage, threat monitoring, and sensitive data disclosure post-runtime metrics are now configured and active by default. The default values for Sampling rate and Max skill calls have changed to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Active setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings under **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.

-   **[Specify the asset state during AI asset creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/creating-ai-assets-newexperience.md)**

    Specify the asset state when you create AI assets manually. By specifying the state during initial asset creation, you can track and manage your assets more accurately throughout their life cycles. You can specify the asset state in the **Asset state** field of the following forms:

    -   Add AI system asset
    -   Add AI model asset
    -   Add prompt asset
    -   Add dataset asset
-   **[Review AI risk and compliance posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-using.md)**

    See regulatory risk classification, compliance posture, and aggregated risk posture for AI assets across your portfolio from the **Govern** tab. Review related cases, issues, and governance actions associated with those assets.

-   **[Track regulatory risk classification and compliance score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-regulatory-status.md)**

    See how AI systems, models, and datasets are categorized by regulatory risk, and track compliance scores against the priority frameworks configured in your environment.

-   **[Review inherent and residual risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-risk-posture.md)**

    Compare inherent risk, residual risk, and control effectiveness for AI systems using the risk heat map, and identify concentrations of higher-risk assets across your portfolio.

-   **[View governance records for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-airc-governance-records.md)**

    Review assessments, risks, controls, attestations, issues, and policy exceptions for an AI asset directly from its **Risk &amp; Compliance** tab, without leaving the asset record.

-   **[AI Service Graph Connector for Anthropic connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-connectors.md)**

    Discover and import Anthropic AI Models and track usage data \(per-user AI asset cost\).

-   **[AI Service Graph Connector for Amazon](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aws_0.md)**
    -   Admins can now configure all AWS AI discovery services using a single credential page.
    -   Admins can enable automatic rotation of AWS access keys for AI SGC connections.
    -   Admins can discover multiple explicit AWS accounts by specifying a comma-separated list of account IDs.
-   **[AI Service Graph Connector for Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/microsoft.md)**
    -   Unified single-page connection for Azure ML and AI services.
    -   Resource group discovery and storage for Azure Foundry assets.
    -   Certificate-based authentication for Azure and Copilot.
    -   Knowledge Base integration in configuration review.

### What's changed

-   **[New AI Control Tower experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-ai-portfolio-overview.md)**

    The new AI Control Tower provides a more efficient, streamlined way for you to work. For information about how to upgrade, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support. Note that the legacy AI Control Tower workspace is still supported in this release.

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Discover your agent network with the map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-use-map.md)**

    The access map is renamed to agent map and shows Veza access intelligence and node details for AI assets, giving you a holistic view of your enterprise.

-   **[Configure post-runtime security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

    You can now adjust the sampling rate for more Post-runtime metrics.

-   **[Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-reference.md)**

    Improved accuracy of AI threat metrics and evaluation datasets that use Traceloop for continuous monitoring in Overview and Runtime metrics. Access issues metrics now support external agents. Azure, Google Cloud Platform \(GCP\), and Google Vertex AI assets are now supported.

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    The Security tab of the AI asset record shows the AI asset security score and metrics for an individual asset.

-   **[AI Service Graph Connector for GCP Vertex AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gcp-vertex-ai.md)**

    The Service Graph Connector for GCP Vertex AI now displays as "AI Connector for Google" to align with the AI Connector naming convention.

-   **[Risk Management tasks for Asset owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-activity-center.md)**

    Users with the AI Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can access and act on risk and compliance lifecycle tasks, such as impact assessments and control attestations, from the Activity Center. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for the asset owner. On the asset record page, all lifecycle tasks specific to the assigned assets can be accessed and performed.

-   **[Unifying lifecycle tasks for Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/risk-compliance-lifecycle-tasks-aict.md)**

    In the legacy AI Control Tower workspace, users with the AI Steward \[sn\_ai\_governance.ai\_steward\] and AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] roles can take and manage risk assessments directly from the Playbook. This eliminates the need to switch between workspaces.


-   **[Additional regulatory frameworks in the AI Risk and Compliance content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-content-pack.md)**

    After AI Risk and Compliance is updated to version 22.3.0 and the new frameworks are activated, authority documents, agency mappings, and citations for the Transparency in Frontier Artificial Intelligence Act \(SB 53\) and the Colorado Artificial Intelligence Act \(SB 205\) appear in the compliance posture and related views on the **Risk &amp; compliance** tab. For more information, see [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/grc-ai-risk-and-compliance-rn.md), [AI Risk and Compliance Content Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-content-pack.md), [Activate or update the Transparency in Frontier Artificial Intelligence Act \(SB 53\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-or-update-sb53.md), and [Activate or update the Colorado Artificial Intelligence Act](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-or-update-colorado-ai-act.md).

-   **[Impact assessment field auto-population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md)**

    After upgrading to version 22.3.5, if you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, the screening question responses that capture the AI system's intended use and operational context from the Use and Purpose section of the AI use case request form are automatically populated in the corresponding Use and Purpose fields of a new impact assessment. This synchronization reduces manual entry and helps ensure that impact assessment responses are consistent with the information submitted at intake. For more information, see [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/grc-ai-risk-and-compliance-rn.md) and [Intake requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md).


### What's deprecated or removed

-   AI Control Tower removed in [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md):

    The Number of clients connecting to MCP servers metrics in Overview tab have been removed. Also, you can't create security incidents from dormant agents using conversational prompts.


## Australia Patch 3

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

### What's changed

-   **[AI record type label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). The **Record type** field on AI system, AI model, and dataset records in the AI Control Tower inventory now displays **AI record** instead of the previous asset-specific labels.


## Australia Patch 2

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

### What's new

-   **[Publish ServiceNow agents to Microsoft Agent 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/publish-servicenow-agents-to-microsoft-agent-365.md)**

    Publish the ServiceNow Agents to Microsoft Agent 365 ensuring the ServiceNow agents are sent to external registries.

-   **[Service Graph Connectors for AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-graph-connectors-for-ai-control-tower.md)**

    AI Service Graph Connector for Databricks discover AI agents and import to AI Control Tower from Databricks environment.


## Australia Patch 1

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

### What's new

-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   Customize the AI asset security score by weighting LLM guardrail categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to the AI asset security score.
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by the **Access** and **Guardrails** tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **[Data section on Configurations page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/data.md)**

    Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics. These metrics measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see, [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/grc-ai-risk-and-compliance-rn.md) [Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-assessment-templates.md)and [Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-rams.md).

-   **[Associate additional related AI asset types with AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of generative AI or agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/creating-ai-asset-requests.md)**

    Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   Datasets
    In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


### What's changed

-   **[Drop-down menu for associating AI assets with related assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that aren't currently available in your asset inventory.

-   **[Editable asset details fields on the Details tab of AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


### What's deprecated or removed

-   AI Control Tower \(legacy\) removed in [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md):

    The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.


## Australia Early Availability

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. AI Control Tower was enhanced and updated in the Australia release.

### What's new

-   **[AI connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enterprise-ai-discovery.md)**

    AI connections are created using AI Service Graph Connectors. AI connections are a combination of hyperscalers, AI apps, and agentic AI frameworks.The following AI Service Graph Connectors are available from March 2026

    -   [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aws_0.md)
    -   [Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/microsoft.md)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gcp-vertex-ai.md)
    -   [n8n](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/n8n.md)
    -   [LangGraph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/langgraph.md)
    -   [Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/salesforce.md)
-   **[AI assets- Managed and Unmanaged](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/assets-list-managing-and-unmanaging-assets.md)**

    Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, don't have access to these AI Control Tower capabilities.

-   ****

    AI Gateway offers MCP Global Clients, which can be used across all servers.A Gateway offers MCP Catalog to choose while adding MCP servers.MCP server can be added to an AI Asset inventory from AI Control Tower.


### What's deprecated or removed

-   AI Control Tower \(legacy\) removed in [Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-all-other-fixes.md):

    Adding legacy AI connections via Service Graph Connectors \(SGC\) is deprecated. In AI connections, under Legacy connections, the **New** button has been removed to block users from creating new connections using SGC.


-   The ability to add hyperscalers from the AICT configuration section is no longer available. You can find any previously created hyperscaler connections in the AI connections section, under Legacy connections.

### Plugin information

-   **New plugins**

    The following plugins are new in Australia for AI Control Tower \(legacy\):

    -   com.sn\_ai\_disc - Enables the AI connections page in the AI Control Tower configuration.
    -   sn\_sgc\_central - Enables the Service Graph Connector \(SGC\) feature in the AI connections page.

