---
title: AI Control Tower release notes
description: The ServiceNow AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. See the following sections for release notes by version.The Brazil Early Availability release adds support for domain separation, policies, quality and safety metrics for specific assets, and more.The Brazil Early Availability 2 release adds support for cost policy management, improved monitoring visualizations, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/ai-control-tower-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [AI Experiences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# AI Control Tower release notes

The ServiceNow® AI Control Tower application provides a centralized workspace to track and act on AI governance work across the enterprise. See the following sections for release notes by version.

## About AI Control Tower

-   Discover and maintain a complete, current inventory of AI systems, models, datasets, and prompts across ServiceNow and external platforms.
-   Track regulatory compliance posture against frameworks like NIST AI RMF and EU AI Act across your entire AI portfolio.
-   Secure AI systems across platforms with automated scoring and access hygiene, model vulnerability and validation findings, real-time guardrails against prompt injection and data leakage, and graduated containment for AI agents.
-   Evaluate the quality and safety of AI interactions across your portfolio using automated scoring, configurable metrics, and trend analysis for both ServiceNow and external AI systems.
-   Quantify the business value of AI investments with productivity, cost savings, and adoption metrics tied to individual AI systems.
-   Coordinate governance work across cross-functional teams with lifecycle playbooks, approval routing, and AI-generated recommendations.

See [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


## Accessibility and localization

-   **Accessibility information**
    -   AI asset security score details, AI agent containment, and configuration pages on the Security tab are fully navigable by keyboard and compatible with screen readers.
-   **Localization information**

    Strings in AI asset security score details, AI agent containment, and configuration pages on the Security tab are available in your organization's configured language, including strings that were previously untranslated.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/intelligent-experiences-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release adds support for domain separation, policies, quality and safety metrics for specific assets, and more.

### What's new

-   **[Control AI asset usage through policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-pol-landing.md)**

    Create AI asset usage policies that automatically respond to detected AI threats or block an AI agent, domain, or model outright.

-   **[Add an Azure AI Foundry connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-azure-foundry-security-connection.md)**

    Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

-   **[Add metrics from the AI system record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-ai-system-metrics.md)**

    Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-external.md)**

    Add, remove, or adjust the sample rate of metrics for one or more external AI systems, without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.md)**

    Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

-   **[Exclude an AI system from a metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-exclude-ai-systems-external.md)**

    Exclude one or more AI systems from a specific metric, without changing that metric's configuration for every other system.

-   **[AI system performance metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-asset-monitor.md)**

    Monitor operational health at a glance, including average latency and token usage per session.

-   **[Latency and span counts for sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-evaluated-sessions-overview.md)**

    See each session's response time and span count in the evaluated sessions lists and on individual session detail pages.

-   **[Scoring bias indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Learn when a composite score might be skewed. See how many evaluations back each metric, and identify when uneven evaluation coverage is influencing the score more than the configured weight suggests.

-   **[Trace data retention controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-trace-retention.md)**

    Keep session, trace, and span data for up to 30 days for scoring, or discard it to reduce storage usage, with quality and safety scores staying available either way. Discarding also disables AI Skill Kit insights and hides the evaluated sessions views.

-   **[Custom date ranges for monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Analyze exactly the period you need by specifying an exact start and end date, up to 18 months apart.

-   **[Review AI security posture in design-time metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

    Use AI security posture metrics to identify potential configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk.

-   **[AI Inventory Intelligence Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inventory-intelligence-agent.md)**

    AI Inventory Intelligence Agent automatically analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The Microsoft connector introduces the A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   **[Client registration and AI Gateway setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/client-registration.md)**
    -   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
    -   The AI Gateway proxy URL format has changed. The new format is:

        `https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

        Previously, the URL format was:

        `https://<instance-url>/sncapps/awh/<mcp-server>/mcp`

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**

    Manage AI assets through structured lifecycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to understand impact to your existing playbooks, flows, and subflows before switching to the new playbook.

-   ****

    AI Control Tower now scopes value, engagement, and cost data based on the user’s role and assigned AI systems.

    AI stewards can view data for all AI systems in an instance. Product owners can view data only for the AI systems that they manage.

    Data scope is determined by the **Managed by** field on the AI system record.

    Product owners can review and adjust measurements for the AI systems that they manage. Cost configuration remains read-only because vendor-level changes can affect AI systems outside a product owner’s scope.


### What's changed

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-domain-separation.md)**

    Use AI Control Tower on a domain-separated instance. In Security, detail pages for Privileged AI agents, Dormant AI agents, Access issues, Security events detected, Agent map, Post-runtime, and AI asset security score include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured. Your top recommendations is replaced by a Security events detected section on the Security dashboard, and Sensitive data metrics aren't shown for ServiceNow AI systems.

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **[Security design-time metrics reorganized into subtabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

    Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by source \(for example, Cisco or HiddenLayer\).

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

    On the Security tab for an AI asset, access issues and access posture metrics aren't shown for AI models because they're agent-level signals derived from agent identity and permissions. Therefore, they don't apply to AI models.

-   **[Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md)**

    AI agent containment \(kill switch\) supports retrying a failed or partial containment operation from the asset record or the agent containment list. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event. AI agent containment \(kill switch\) is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity.

-   **[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-security-connections.md)**

    The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   **[Add a Gemini Enterprise Agent Platform connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.md)**

    The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **[Agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md)**

    The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **[Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)Security dates and times shown in UTC**

    Date and time values in the Security tab — including the agent containment list, the Overview tab's Dormant AI agents and Privileged AI agents details, and the Post-runtime tab's security events — are now shown in Coordinated Universal Time \(UTC\) rather than your local timezone.

-   **[AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-gateway.md)**

    Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.
-   **[Veza connector authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-ai-connection-veza.md)**

    The Veza connector now authenticates using OAuth 2.0. Configure an OAuth profile and alias on the platform, then select it from **Settings** &gt; **Integrations** &gt; **Connectors**. Depending on which OAuth credential is active, tokens are either issued per user and tied to user identity, or shared at the system level, replacing API key authentication as the default method. The Veza tile appears in **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

-   **[Create Asset Task action renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-use-events.md)**

    The **Create AI Task** action, available on AI asset security events, privileged AI agents, and dormant AI agents, is renamed to **Create Asset Task**.

-   **[AI security posture metrics added and renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

    On the Design-time tab in Security, AI security posture subtab, three metrics were added under **AI assets with critical findings**: **MCP servers**, **Tools**, and **System prompts**.

    Several metrics on the same subtab were renamed for clarity:

    -   **Critical findings approaching remediation target** is renamed **Findings approaching remediation target**.
    -   **Critical findings with remediation overdue** is renamed **Findings with remediation overdue**.
    -   **Number of findings deferred** is renamed **Findings deferred**.
    -   **Findings by risk rating** is renamed **Posture findings by risk rating**.
    -   **Findings by OWASP LLM Top 10** is renamed **Critical findings by OWASP top ten**.
    -   **Findings by MITRE ATLAS techniques** is renamed **Critical findings by MITRE ATLAS technique**.
    The **Critical findings by platform**, **Critical findings by OWASP top ten**, and **Critical findings by MITRE ATLAS technique** metrics require the AI Security Exposure Management plugin, and are no longer available in the base system.

-   **[Updated default Sampling rate and Max skill calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

    In **Settings** &gt; **Rules and templates** &gt; **Security**, the default values for Sampling rate and Max skill calls have changed to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings under **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


### What's deprecated or removed

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Veza API key authentication deprecated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference-system-properties.md)**

    The Veza connector now authenticates using OAuth 2.0 instead of an API key. The sn\_ai\_security.veza.api.key system property is deprecated.

-   **[Findings by severity metric removed from Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

    The **Findings by severity** metric is removed from the Security Design-time tab, AI security posture subtab.


### Plugin information

-   **New plugins**

    AI Policy Framework \(sn\_ai\_policy\_framework\): Mitigate AI exposure through policies.


## Brazil Early Availability 2

The Brazil Early Availability 2 release adds support for cost policy management, improved monitoring visualizations, and more.

### What's new

-   **[Monitor agent activity chart improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

    Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.

-   **[Session details improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-session-details.md)**

    View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.

-   **Connectors**

    Amazon Quick connector is a new connector which is part of discovering Systems, models, and prompts for creating AI connections.


### What's changed

-   **[View input and output in trace details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-session-details.md)**

    Toggle between input and output when viewing trace details.


### What's deprecated or removed

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

     \(\): 

-   **Deprecated plugins**

     \(\): 

-   **Plugins planned for deprecation**

     \(\): Planned for deprecation in . 

-   **Renamed or changed plugins**

     \(\): 


