---
title: Combined AI Control Tower release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for AI Control Tower from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-aicontroltower-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 33
breadcrumb: [Products combined by family]
---

# Combined AI Control Tower release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for AI Control Tower from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Control Tower release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Control Tower to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for AI Control Tower.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Control AI asset usage through policies](https://www.servicenow.com/docs/access?context=gov-pol-landing&family=australia&ft:locale=en-US)**

Apply policies to block AI activity and respond to AI threats.

-   **[Add an Azure AI Foundry connection](https://www.servicenow.com/docs/access?context=aict-configure-azure-foundry-security-connection&family=australia&ft:locale=en-US)**

Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

-   **[Add metrics from the AI system record](https://www.servicenow.com/docs/access?context=mon-ai-configure-ai-system-metrics&family=australia&ft:locale=en-US)**

Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more external AI systems](https://www.servicenow.com/docs/access?context=mon-ai-configure-asset-metrics-external&family=australia&ft:locale=en-US)**

Add, remove, or adjust the sample rate of metrics for one or more external AI systems, without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more ServiceNow AI systems](https://www.servicenow.com/docs/access?context=mon-ai-configure-asset-metrics-servicenow&family=australia&ft:locale=en-US)**

Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

-   **[Exclude an AI system from a metric](https://www.servicenow.com/docs/access?context=mon-ai-exclude-ai-systems-external&family=australia&ft:locale=en-US)**

Exclude one or more AI systems from a specific metric, without changing that metric's configuration for every other system.

-   **[AI system performance metrics](https://www.servicenow.com/docs/access?context=mon-ai-asset-monitor&family=australia&ft:locale=en-US)**

Monitor operational health at a glance, including average latency and token usage per session.

-   **[Latency and span counts for sessions](https://www.servicenow.com/docs/access?context=mon-ai-evaluated-sessions-overview&family=australia&ft:locale=en-US)**

See each session's response time and span count in the evaluated sessions lists and on individual session detail pages.

-   **[Scoring bias indicator](https://www.servicenow.com/docs/access?context=mon-ai-monitoring-overview&family=australia&ft:locale=en-US)**

Learn when a composite score might be skewed. See how many evaluations back each metric, and identify when uneven evaluation coverage is influencing the score more than the configured weight suggests.

-   **[Trace data retention controls](https://www.servicenow.com/docs/access?context=mon-ai-configure-trace-retention&family=australia&ft:locale=en-US)**

Keep session, trace, and span data for up to 30 days for scoring, or discard it to reduce storage usage, with quality and safety scores staying available either way. Discarding also disables AI Skill Kit insights and hides the evaluated sessions views.

-   **[Custom date ranges for monitoring](https://www.servicenow.com/docs/access?context=mon-ai-monitoring-overview&family=australia&ft:locale=en-US)**

Analyze exactly the period you need by specifying an exact start and end date, up to 18 months apart.

-   **[Review AI security posture in design-time metrics](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=australia&ft:locale=en-US)**

Identify configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk with AI security posture metrics.

-   **[AI Inventory Intelligence Agent](https://www.servicenow.com/docs/access?context=inventory-intelligence-agent&family=australia&ft:locale=en-US)**

AI Inventory Intelligence Agent automatically analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.

-   **[Configuring connectors](https://www.servicenow.com/docs/access?context=aict-configuring-connectors&family=australia&ft:locale=en-US)**
    -   The Microsoft connector introduces the A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   **[Client registration and AI Gateway setup](https://www.servicenow.com/docs/access?context=client-registration&family=australia&ft:locale=en-US)**
    -   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
    -   The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`


 -   **[Activity Center](https://www.servicenow.com/docs/access?context=aict-activity-center&family=australia&ft:locale=en-US)**

Track and act on the governance work generated across AI Control Tower from a single workspace, including lifecycle tasks, security tasks, change and offboarding requests, and AI recommendations.

-   **[Recommendations and AI insights](https://www.servicenow.com/docs/access?context=aict-recommendations-ai-insights&family=australia&ft:locale=en-US)**

Recommendations and AI insights direct your attention to the AI governance work that matters most, so you can resolve high-impact issues without searching for them. Act on recommendations from the Home page, an asset record, or Activity Center.

-   **[Monitor quality and safety for AI systems](https://www.servicenow.com/docs/access?context=mon-ai-landing&family=australia&ft:locale=en-US)**

Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.

-   **[Trace connections](https://www.servicenow.com/docs/access?context=aict-configuring-trace-connections&family=australia&ft:locale=en-US)**

Collect trace data for discovery, security, and monitoring from hyperscalers including AWS, Azure, and Google Cloud by configuring trace connections.

-   **[Plan AI strategy, prioritize, and execute](https://www.servicenow.com/docs/access?context=aict-planning-ai-strategy&family=australia&ft:locale=en-US)**

Track your AI portfolio from strategy to delivery with the Plan menu. Plan connects goal alignment, intake management, and execution tracking in a single workspace, giving portfolio managers and AI COE leads a current view of AI investments.

-   **[ServiceNow Otto in AI Governance](https://www.servicenow.com/docs/access?context=aict-convrstn-support&family=australia&ft:locale=en-US)**

Use ServiceNow Otto premium chat in AI Control Tower for a better conversational experience with unified search and chat capabilities, including integrated web search and file uploads.

-   **[AI agent containment using kill switch protocol manually](https://www.servicenow.com/docs/access?context=gov-sec-exploring-ai-agent-containment&family=australia&ft:locale=en-US)**

Deactivate and reinstate AI agents running in AWS Bedrock, AWS Bedrock AgentCore, GCP Vertex AI \(limited support\), and ServiceNow agents. Revoke AI agent session tokens through Okta.

-   **[Discover your agent network with the map](https://www.servicenow.com/docs/access?context=gov-sec-use-map&family=australia&ft:locale=en-US)**

See AI models, MCP servers, and providers in the agent map for complete resource visibility across your enterprise, along with agents, agentic workflows, and other AI assets.

-   **[Configure post-runtime security metrics](https://www.servicenow.com/docs/access?context=gov-sec-configure-event-metrics&family=australia&ft:locale=en-US)**

System prompt leakage, threat monitoring, and sensitive data disclosure post-runtime metrics are now configured and active by default.

-   **[Specify the asset state during AI asset creation](https://www.servicenow.com/docs/access?context=creating-ai-assets-newexperience&family=australia&ft:locale=en-US)**

Specify the asset state when you create AI assets manually. By specifying the state during initial asset creation, you can track and manage your assets more accurately throughout their life cycles. You can specify the asset state in the **Asset state** field of the following forms:

    -   Add AI system asset
    -   Add AI model asset
    -   Add prompt asset
    -   Add dataset asset
-   **[Review AI risk and compliance posture](https://www.servicenow.com/docs/access?context=gov-airc-using&family=australia&ft:locale=en-US)**

See regulatory risk classification, compliance posture, and aggregated risk posture for AI assets across your portfolio from the **Govern** tab. Review related cases, issues, and governance actions associated with those assets.

-   **[Track regulatory risk classification and compliance score](https://www.servicenow.com/docs/access?context=gov-airc-regulatory-status&family=australia&ft:locale=en-US)**

See how AI systems, models, and datasets are categorized by regulatory risk, and track compliance scores against the priority frameworks configured in your environment.

-   **[Review inherent and residual risk posture](https://www.servicenow.com/docs/access?context=gov-airc-risk-posture&family=australia&ft:locale=en-US)**

Compare inherent risk, residual risk, and control effectiveness for AI systems using the risk heat map, and identify concentrations of higher-risk assets across your portfolio.

-   **[View governance records for AI assets](https://www.servicenow.com/docs/access?context=gov-airc-governance-records&family=australia&ft:locale=en-US)**

Review assessments, risks, controls, attestations, issues, and policy exceptions for an AI asset directly from its **Risk &amp; Compliance** tab, without leaving the asset record.

-   **[AI Service Graph Connector for Anthropic connector](https://www.servicenow.com/docs/access?context=aict-configuring-connectors&family=australia&ft:locale=en-US)**

Discover and import Anthropic AI Models and track usage data \(per-user AI asset cost\).

-   **[AWS](https://www.servicenow.com/docs/access?context=aws_0&family=australia&ft:locale=en-US)**
    -   Admins can now configure all AWS AI discovery services using a single credential page.
    -   Admins can enable automatic rotation of AWS access keys for AI SGC connections.
    -   Admins can discover multiple explicit AWS accounts by specifying a comma-separated list of account IDs.
-   **[Microsoft](https://www.servicenow.com/docs/access?context=microsoft&family=australia&ft:locale=en-US)**
    -   Unified single-page connection for Azure ML and AI services.
    -   Resource group discovery and storage for Azure Foundry assets.
    -   Certificate-based authentication for Azure and Copilot.
    -   Knowledge Base integration in configuration review.

 -   **[Publish ServiceNow agents to Microsoft Agent 365](https://www.servicenow.com/docs/access?context=publish-servicenow-agents-to-microsoft-agent-365&family=australia&ft:locale=en-US)**

Publish the ServiceNow Agents to Microsoft Agent 365 ensuring the ServiceNow agents are sent to external registries.

-   **[Service Graph Connectors for AI Control Tower](https://www.servicenow.com/docs/access?context=service-graph-connectors-for-ai-control-tower&family=australia&ft:locale=en-US)**

AI Service Graph Connector for Databricks discover AI agents and import to AI Control Tower from Databricks environment.


 -   **[Security &amp; privacy tab in AI Governance](https://www.servicenow.com/docs/access?context=security-privacy-tab&family=australia&ft:locale=en-US)**
    -   Customize the AI asset security score by weighting LLM guardrail categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to the AI asset security score.
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by the **Access** and **Guardrails** tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&family=australia&ft:locale=en-US)**

Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics. These metrics measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see, [AI Risk and Compliance release notes](https://www.servicenow.com/docs/access?context=grc-ai-risk-and-compliance-rn&family=australia&ft:locale=en-US) [Assessment templates](https://www.servicenow.com/docs/access?context=airc-assessment-templates&family=australia&ft:locale=en-US)and [Risk assessment methodologies](https://www.servicenow.com/docs/access?context=airc-rams&family=australia&ft:locale=en-US).

-   **[Associate additional related AI asset types with AI systems](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of generative AI or agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&family=australia&ft:locale=en-US)**

Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   Datasets
In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[AI connections](https://www.servicenow.com/docs/access?context=enterprise-ai-discovery&family=australia&ft:locale=en-US)**

AI connections are created using AI Service Graph Connectors. AI connections are a combination of hyperscalers, AI apps, and agentic AI frameworks.The following AI Service Graph Connectors are available from March 2026

    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&family=australia&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&family=australia&ft:locale=en-US)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&family=australia&ft:locale=en-US)
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&family=australia&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&family=australia&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&family=australia&ft:locale=en-US)
-   **[AI assets- Managed and Unmanaged](https://www.servicenow.com/docs/access?context=assets-list-managing-and-unmanaging-assets&family=australia&ft:locale=en-US)**

Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, don't have access to these AI Control Tower capabilities.

-   **[AI Gateway](https://www.servicenow.com/docs/access?context=ai-gateway-overview&family=australia&ft:locale=en-US)**

AI Gateway offers MCP Global Clients, which can be used across all servers.A Gateway offers MCP Catalog to choose while adding MCP servers.MCP server can be added to an AI Asset inventory from AI Control Tower.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Control AI asset usage through policies](https://www.servicenow.com/docs/access?context=gov-pol-landing&family=brazil&ft:locale=en-US)**

Create AI asset usage policies that automatically respond to detected AI threats or block an AI agent, domain, or model outright.

-   **[Add an Azure AI Foundry connection](https://www.servicenow.com/docs/access?context=aict-configure-azure-foundry-security-connection&family=brazil&ft:locale=en-US)**

Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

-   **[Add metrics from the AI system record](https://www.servicenow.com/docs/access?context=mon-ai-configure-ai-system-metrics&family=brazil&ft:locale=en-US)**

Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more external AI systems](https://www.servicenow.com/docs/access?context=mon-ai-configure-asset-metrics-external&family=brazil&ft:locale=en-US)**

Add, remove, or adjust the sample rate of metrics for one or more external AI systems, without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more ServiceNow AI systems](https://www.servicenow.com/docs/access?context=mon-ai-configure-asset-metrics-servicenow&family=brazil&ft:locale=en-US)**

Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

-   **[Exclude an AI system from a metric](https://www.servicenow.com/docs/access?context=mon-ai-exclude-ai-systems-external&family=brazil&ft:locale=en-US)**

Exclude one or more AI systems from a specific metric, without changing that metric's configuration for every other system.

-   **[AI system performance metrics](https://www.servicenow.com/docs/access?context=mon-ai-asset-monitor&family=brazil&ft:locale=en-US)**

Monitor operational health at a glance, including average latency and token usage per session.

-   **[Latency and span counts for sessions](https://www.servicenow.com/docs/access?context=mon-ai-evaluated-sessions-overview&family=brazil&ft:locale=en-US)**

See each session's response time and span count in the evaluated sessions lists and on individual session detail pages.

-   **[Scoring bias indicator](https://www.servicenow.com/docs/access?context=mon-ai-monitoring-overview&family=brazil&ft:locale=en-US)**

Learn when a composite score might be skewed. See how many evaluations back each metric, and identify when uneven evaluation coverage is influencing the score more than the configured weight suggests.

-   **[Trace data retention controls](https://www.servicenow.com/docs/access?context=mon-ai-configure-trace-retention&family=brazil&ft:locale=en-US)**

Keep session, trace, and span data for up to 30 days for scoring, or discard it to reduce storage usage, with quality and safety scores staying available either way. Discarding also disables AI Skill Kit insights and hides the evaluated sessions views.

-   **[Custom date ranges for monitoring](https://www.servicenow.com/docs/access?context=mon-ai-monitoring-overview&family=brazil&ft:locale=en-US)**

Analyze exactly the period you need by specifying an exact start and end date, up to 18 months apart.

-   **[Review AI security posture in design-time metrics](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=brazil&ft:locale=en-US)**

Use AI security posture metrics to identify potential configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk.

-   **[AI Inventory Intelligence Agent](https://www.servicenow.com/docs/access?context=inventory-intelligence-agent&family=brazil&ft:locale=en-US)**

AI Inventory Intelligence Agent automatically analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.

-   **[Configuring connectors](https://www.servicenow.com/docs/access?context=aict-configuring-connectors&family=brazil&ft:locale=en-US)**
    -   The Microsoft connector introduces the A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   **[Client registration and AI Gateway setup](https://www.servicenow.com/docs/access?context=client-registration&family=brazil&ft:locale=en-US)**
    -   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
    -   The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`

-   **[Updated playbooks for governing managed assets](https://www.servicenow.com/docs/access?context=dynamic-playbooks-for-governing-managed-assets&family=brazil&ft:locale=en-US)**

Manage AI assets through structured lifecycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to understand impact to your existing playbooks, flows, and subflows before switching to the new playbook.

-   **[\[Placeholder link text to key mv-data-visibility-by-ai-control-tower-role\]](https://www.servicenow.com/docs/access?context=mv-data-visibility-by-ai-control-tower-role&family=brazil&ft:locale=en-US)**

AI Control Tower now scopes value, engagement, and cost data based on the user’s role and assigned AI systems.

AI stewards can view data for all AI systems in an instance. Product owners can view data only for the AI systems that they manage.

Data scope is determined by the **Managed by** field on the AI system record.

Product owners can review and adjust measurements for the AI systems that they manage. Cost configuration remains read-only because vendor-level changes can affect AI systems outside a product owner’s scope.


 -   **[Monitor agent activity chart improvements](https://www.servicenow.com/docs/access?context=mon-ai-monitoring-overview&family=brazil&ft:locale=en-US)**

Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.

-   **[Session details improvements](https://www.servicenow.com/docs/access?context=mon-ai-session-details&family=brazil&ft:locale=en-US)**

View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.

-   **Connectors**

Amazon Quick connector is a new connector which is part of discovering Systems, models, and prompts for creating AI connections.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing AI Control Tower features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Domain separation and AI Governance](https://www.servicenow.com/docs/access?context=aict-domain-separation&family=australia&ft:locale=en-US)**

Use AI Control Tower on a domain-separated instance. In Security, detail pages for some metrics include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured.

-   **[Domain separation and AI Governance](https://www.servicenow.com/docs/access?context=aict-domain-separation&family=australia&ft:locale=en-US)**

Use AI Control Tower on a domain-separated instance. In Security, detail pages for some metrics include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured.

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=australia&ft:locale=en-US)**

Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **[Design-time metrics reorganized into subtabs](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=australia&ft:locale=en-US)**

Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by asset source \(for example, ServiceNow or AWS Bedrock\).

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=australia&ft:locale=en-US)**

On the Security tab for an AI asset, a metric isn't shown if there's no data available for the asset. Also, access issues and access posture don't appear for AI models.

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=australia&ft:locale=en-US)**

AI agent containment using kill switch protocol is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity. It also supports retrying a failed or partial containment operation. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event.

-   **[Configuring security connections](https://www.servicenow.com/docs/access?context=aict-configuring-security-connections&family=australia&ft:locale=en-US)**

The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   **[Add a Gemini Enterprise Agent Platform connection](https://www.servicenow.com/docs/access?context=aict-configure-gcp-vertex-ai-security-connection&family=australia&ft:locale=en-US)**

The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **[Agent containment list](https://www.servicenow.com/docs/access?context=gov-sec-review-kill-switch-protocol-log&family=australia&ft:locale=en-US)**

The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **[AI Gateway](https://www.servicenow.com/docs/access?context=ai-gateway&family=australia&ft:locale=en-US)**

Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   **[Configuring connectors](https://www.servicenow.com/docs/access?context=aict-configuring-connectors&family=australia&ft:locale=en-US)**
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.

 -   **[New AI Control Tower experience](https://www.servicenow.com/docs/access?context=aict-ai-portfolio-overview&family=australia&ft:locale=en-US)**

The new AI Control Tower provides a more efficient, streamlined way for you to work. For information about how to upgrade, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support. Note that the legacy AI Control Tower workspace is still supported in this release.

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Discover your agent network with the map](https://www.servicenow.com/docs/access?context=gov-sec-use-map&family=australia&ft:locale=en-US)**

The access map is renamed to agent map and shows Veza access intelligence and node details for AI assets, giving you a holistic view of your enterprise.

-   **[Configure post-runtime security metrics](https://www.servicenow.com/docs/access?context=gov-sec-configure-event-metrics&family=australia&ft:locale=en-US)**

You can now adjust the sampling rate for more Post-runtime metrics.

-   **[Reference](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=australia&ft:locale=en-US)**

Improved accuracy of AI threat metrics and evaluation datasets that use Traceloop for continuous monitoring in Overview and Runtime metrics. Access issues metrics now support external agents. Azure, Google Cloud Platform \(GCP\), and Google Vertex AI assets are now supported.

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=australia&ft:locale=en-US)**

The Security tab of the AI asset record shows the AI asset security score and metrics for an individual asset.

-   **[GCP Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&family=australia&ft:locale=en-US)**

The Service Graph Connector for GCP Vertex AI now displays as "AI Connector for Google" to align with the AI Connector naming convention.

-   **[Risk Management tasks for Asset owner](https://www.servicenow.com/docs/access?context=aict-activity-center&family=australia&ft:locale=en-US)**

Users with the AI Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can access and act on risk and compliance lifecycle tasks, such as impact assessments and control attestations, from the Activity Center. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for the asset owner. On the asset record page, all lifecycle tasks specific to the assigned assets can be accessed and performed.

-   **[Unifying lifecycle tasks for Risk and Compliance](https://www.servicenow.com/docs/access?context=risk-compliance-lifecycle-tasks-aict&family=australia&ft:locale=en-US)**

In the legacy AI Control Tower workspace, users with the AI Steward \[sn\_ai\_governance.ai\_steward\] and AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] roles can take and manage risk assessments directly from the Playbook. This eliminates the need to switch between workspaces.


 -   **[Additional regulatory frameworks in the AI Risk and Compliance content pack](https://www.servicenow.com/docs/access?context=airc-content-pack&family=australia&ft:locale=en-US)**

After AI Risk and Compliance is updated to version 22.3.0 and the new frameworks are activated, authority documents, agency mappings, and citations for the Transparency in Frontier Artificial Intelligence Act \(SB 53\) and the Colorado Artificial Intelligence Act \(SB 205\) appear in the compliance posture and related views on the **Risk &amp; compliance** tab. For more information, see [AI Risk and Compliance release notes](https://www.servicenow.com/docs/access?context=grc-ai-risk-and-compliance-rn&family=australia&ft:locale=en-US), [Content pack](https://www.servicenow.com/docs/access?context=airc-content-pack&family=australia&ft:locale=en-US), [Activate or update the Transparency in Frontier Artificial Intelligence Act \(SB 53\)](https://www.servicenow.com/docs/access?context=activate-or-update-sb53&family=australia&ft:locale=en-US), and [Activate or update the Colorado Artificial Intelligence Act](https://www.servicenow.com/docs/access?context=activate-or-update-colorado-ai-act&family=australia&ft:locale=en-US).

-   **[Impact assessment field auto-population](https://www.servicenow.com/docs/access?context=airc-intake&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.5, if you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, the screening question responses that capture the AI system's intended use and operational context from the Use and Purpose section of the AI use case request form are automatically populated in the corresponding Use and Purpose fields of a new impact assessment. This synchronization reduces manual entry and helps ensure that impact assessment responses are consistent with the information submitted at intake. For more information, see [AI Risk and Compliance release notes](https://www.servicenow.com/docs/access?context=grc-ai-risk-and-compliance-rn&family=australia&ft:locale=en-US) and [Intake requests](https://www.servicenow.com/docs/access?context=airc-intake&family=australia&ft:locale=en-US).


 -   **[AI record type label](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=australia&ft:locale=en-US)**

The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). The **Record type** field on AI system, AI model, and dataset records in the AI Control Tower inventory now displays **AI record** instead of the previous asset-specific labels.


 -   **[Drop-down menu for associating AI assets with related assets](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=australia&ft:locale=en-US)**

In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that aren't currently available in your asset inventory.

-   **[Editable asset details fields on the Details tab of AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=australia&ft:locale=en-US)**

You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=australia&ft:locale=en-US)**

The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Domain separation and AI Governance](https://www.servicenow.com/docs/access?context=aict-domain-separation&family=brazil&ft:locale=en-US)**

Use AI Control Tower on a domain-separated instance. In Security, detail pages for Privileged AI agents, Dormant AI agents, Access issues, Security events detected, Agent map, Post-runtime, and AI asset security score include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured. Your top recommendations is replaced by a Security events detected section on the Security dashboard, and Sensitive data metrics aren't shown for ServiceNow AI systems.

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=brazil&ft:locale=en-US)**

Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **[Security design-time metrics reorganized into subtabs](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=brazil&ft:locale=en-US)**

Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by source \(for example, Cisco or HiddenLayer\).

-   **[Governing AI asset security](https://www.servicenow.com/docs/access?context=gov-sec-ai-asset&family=brazil&ft:locale=en-US)**

On the Security tab for an AI asset, access issues and access posture metrics aren't shown for AI models because they're agent-level signals derived from agent identity and permissions. Therefore, they don't apply to AI models.

-   **[Contain AI agents manually using kill switch protocol](https://www.servicenow.com/docs/access?context=gov-sec-manage-ai-agents-using-kill-switch-protocol&family=brazil&ft:locale=en-US)**

AI agent containment \(kill switch\) supports retrying a failed or partial containment operation from the asset record or the agent containment list. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event. AI agent containment \(kill switch\) is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity.

-   **[Configuring security connections](https://www.servicenow.com/docs/access?context=aict-configuring-security-connections&family=brazil&ft:locale=en-US)**

The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   **[Add a Gemini Enterprise Agent Platform connection](https://www.servicenow.com/docs/access?context=aict-configure-gcp-vertex-ai-security-connection&family=brazil&ft:locale=en-US)**

The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **[Agent containment list](https://www.servicenow.com/docs/access?context=gov-sec-review-kill-switch-protocol-log&family=brazil&ft:locale=en-US)**

The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **[Reference](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=brazil&ft:locale=en-US)Security dates and times shown in UTC**

Date and time values in the Security tab — including the agent containment list, the Overview tab's Dormant AI agents and Privileged AI agents details, and the Post-runtime tab's security events — are now shown in Coordinated Universal Time \(UTC\) rather than your local timezone.

-   **[AI Gateway](https://www.servicenow.com/docs/access?context=ai-gateway&family=brazil&ft:locale=en-US)**

Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   **[Configuring connectors](https://www.servicenow.com/docs/access?context=aict-configuring-connectors&family=brazil&ft:locale=en-US)**
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.
-   **[Veza connector authentication](https://www.servicenow.com/docs/access?context=aict-create-ai-connection-veza&family=brazil&ft:locale=en-US)**

The Veza connector now authenticates using OAuth 2.0. Configure an OAuth profile and alias on the platform, then select it from **Settings** &gt; **Integrations** &gt; **Connectors**. Depending on which OAuth credential is active, tokens are either issued per user and tied to user identity, or shared at the system level, replacing API key authentication as the default method. The Veza tile appears in **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

-   **[Create Asset Task action renamed](https://www.servicenow.com/docs/access?context=gov-sec-use-events&family=brazil&ft:locale=en-US)**

The **Create AI Task** action, available on AI asset security events, privileged AI agents, and dormant AI agents, is renamed to **Create Asset Task**.

-   **[AI security posture metrics added and renamed](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=brazil&ft:locale=en-US)**

On the Design-time tab in Security, AI security posture subtab, three metrics were added under **AI assets with critical findings**: **MCP servers**, **Tools**, and **System prompts**.

Several metrics on the same subtab were renamed for clarity:

    -   **Critical findings approaching remediation target** is renamed **Findings approaching remediation target**.
    -   **Critical findings with remediation overdue** is renamed **Findings with remediation overdue**.
    -   **Number of findings deferred** is renamed **Findings deferred**.
    -   **Findings by risk rating** is renamed **Posture findings by risk rating**.
    -   **Findings by OWASP LLM Top 10** is renamed **Critical findings by OWASP top ten**.
    -   **Findings by MITRE ATLAS techniques** is renamed **Critical findings by MITRE ATLAS technique**.
The **Critical findings by platform**, **Critical findings by OWASP top ten**, and **Critical findings by MITRE ATLAS technique** metrics require the AI Security Exposure Management plugin, and are no longer available in the base system.

-   **[Updated default Sampling rate and Max skill calls](https://www.servicenow.com/docs/access?context=gov-sec-configure-event-metrics&family=brazil&ft:locale=en-US)**

In **Settings** &gt; **Rules and templates** &gt; **Security**, the default values for Sampling rate and Max skill calls have changed to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings under **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


 -   **[View input and output in trace details](https://www.servicenow.com/docs/access?context=mon-ai-session-details&family=brazil&ft:locale=en-US)**

Toggle between input and output when viewing trace details.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some AI Control Tower features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some AI Control Tower features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Now LLM Service deprecation notice](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


 -   AI Control Tower removed in [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US):

The Number of clients connecting to MCP servers metrics in Overview tab have been removed. Also, you can't create security incidents from dormant agents using conversational prompts.


 -   AI Control Tower \(legacy\) removed in [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US):

The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.


 -   AI Control Tower \(legacy\) removed in [Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US):

Adding legacy AI connections via Service Graph Connectors \(SGC\) is deprecated. In AI connections, under Legacy connections, the **New** button has been removed to block users from creating new connections using SGC.


 -   The ability to add hyperscalers from the AICT configuration section is no longer available. You can find any previously created hyperscaler connections in the AI connections section, under Legacy connections.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Now LLM Service deprecation notice](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=brazil&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Veza API key authentication deprecated](https://www.servicenow.com/docs/access?context=gov-sec-reference-system-properties&family=brazil&ft:locale=en-US)**

The Veza connector now authenticates using OAuth 2.0 instead of an API key. The sn\_ai\_security.veza.api.key system property is deprecated.

-   **[Findings by severity metric removed from Security](https://www.servicenow.com/docs/access?context=gov-sec-reference&family=brazil&ft:locale=en-US)**

The **Findings by severity** metric is removed from the Security Design-time tab, AI security posture subtab.


 -   **[Now LLM Service deprecation notice](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=brazil&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Control Tower.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Control Tower, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Accessibility information**
    -   AI asset security score details, AI agent containment, and configuration pages on the Security tab are fully navigable by keyboard and compatible with screen readers.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Localization information**

Strings in AI asset security score details, AI agent containment, and configuration pages on the Security tab are available in your organization's configured language, including strings that were previously untranslated.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

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


 AI Control Tower highlights in [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US):

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

 AI Control Tower \(legacy\) highlights in [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US):

-   The AI asset list in AI Inventory includes Asset State and Asset Status columns.
-   The system assigns a unique ID to every asset. The ID appears in the Asset tag field under Asset details.
-   AI Service Graph Connectors for OpenAI, Moveworks, IBM, and OCI are available in AI Control Tower for AI connections.
-   The AI Service Graph Connector for OpenAI discovers AI models and tracks model usage.
-   When you mark a managed asset as unmanaged, the asset's active workflows, tasks, and governance processes are canceled, and the asset is excluded from value tracking.
-   When you mark an unmanaged asset as managed, the asset is actively monitored and governed, making it visible and eligible for governance workflows and value tracking.

 AI Control Tower \(legacy\) highlights in [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US):

-   Customize the AI asset security score calculation to reflect your security requirements.
-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance's AI Gateway.
-   Configure and create automation rules to set AI assets as managed assets.
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.

 AI Control Tower \(legacy\) highlights in [Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US):

-   AI assets—including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors \(SGC\).
-   The AI model providers supported by ServiceNow contains providers such as Now LLM Service, AWS Claude, Now LLM LTS model, and so on.
-   The AI model providers configured by your organization contains providers such as Perplexity, IBM Watson, and so on.
-   AI Gateway offers Global MCP clients, which once created can be used across all MCP servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers into AI Control Tower.

 For more information on the new AI Control Tower experience, see [AI Governance](https://www.servicenow.com/docs/access?context=aict-landing&family=australia&ft:locale=en-US).

 For more information on the legacy AI Control Tower experience, see [AI Governance \(legacy\)](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Brazil

</td><td>

-   Discover and maintain a complete, current inventory of AI systems, models, datasets, and prompts across ServiceNow and external platforms.
-   Track regulatory compliance posture against frameworks like NIST AI RMF and EU AI Act across your entire AI portfolio.
-   Secure AI systems across platforms with automated scoring and access hygiene, model vulnerability and validation findings, real-time guardrails against prompt injection and data leakage, and graduated containment for AI agents.
-   Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.
-   Quantify the business value of AI investments with productivity, cost savings, and adoption metrics tied to individual AI systems.
-   Coordinate governance work across cross-functional teams with lifecycle playbooks, approval routing, and AI-generated recommendations.

 See [AI Governance](https://www.servicenow.com/docs/access?context=aict-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

