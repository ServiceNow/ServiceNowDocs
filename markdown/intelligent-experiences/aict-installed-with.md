---
title: Components installed with AI Control Tower
description: Several types of components are installed with activation of AI Control Tower, including plugins, user roles, and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-installed-with.html
release: australia
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 8
keywords: [AI Control Tower, installed components, plugins, roles, tables]
breadcrumb: [Reference, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Components installed with AI Control Tower

Several types of components are installed with activation of AI Control Tower, including plugins, user roles, and tables.

## Plugins installed

The plugins in the [Core plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-installed-with.md) table are installed with AI Native Experience for AI Control Tower. The plugins in the [Additional plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-installed-with.md) table are installed with AI Control Tower \(`sn_aict`\), which is part of AI Control Tower for Enterprise AI Foundation. If `sn_aict` is already on your instance when you install AI Native Experience for AI Control Tower, you already have these plugins.

|Plugin|Plugin ID|Description|
|------|---------|-----------|
|AI Control Tower Core|`sn_ai_governance`|Centralizes AI governance across the enterprise by combining AI assets and controls in a single hub.|
|AI Asset Management|`sn_ai_asset_mgmt`|Tracks and manages the lifecycle of AI assets such as systems, models, datasets, and prompts.|
|AICT UI Application|`sn_app_aict_ui`|Provides the AI Control Tower user interface.|
|AI Experience - Core|`com.glide.ai_experience`|Provides the services that AI Control Tower uses to render pages and cards, apply themes, and save card configuration changes.|
|AI Control Tower - Evaluations|`sn_ai_observe`|Enables the evaluation framework, scoring engine, and monitoring components for your AI systems.|
|AI Policy Framework|`sn_ai_policy_fwk`|Authors and enforces policies for AI agents and systems, including automatic containment.|
|AI Security and Privacy|`sn_ai_security`|Provides security and privacy monitoring for AI assets.|
|AWH for AI Control Tower|`sn_awh_config`|Configures the Agent Workspace Hub for AI Control Tower.|
|Value dashboard for AI Control Tower|`sn_ai_value`|Provides the Value dashboard for measuring AI investment return and adoption.|
|AI Risk and Compliance Management|`sn_grc_ai_gov`|Manages AI risks across their lifecycle, including risk classification, mapping to regulatory authority documents, and policy compliance.|
|AI Case Management|`sn_ai_case_mgmt`|Tracks, triages, and resolves inquiries and incidents related to AI assets.|
|AI Risk and Compliance Integration with Control Tower|`sn_grc_ai_irm_intg`|Surfaces risk posture, compliance status, and case workflows directly in AI Control Tower so you can manage AI use cases against regulatory frameworks.|
|AI Control Tower for ServiceNow Otto|`sn_aict_nowassist`|Syncs ServiceNow Otto AI skills into the AI Control Tower inventory.|
|ServiceNow Otto for AI Control Tower|`sn_aict_genai`|Adds built-in AI insights and recommendations to AI Control Tower.|
|Expanded Model and Asset Classes|`sn_ent`|Provides the model and asset classes that AI Control Tower uses. Required for API access to AI asset records.|
|ServiceNow AI Lens|`sn_ai_lens`|Provides AI reporting and lens capabilities.|

Supporting plugins, such as Setup Hub, Data Privacy, Data Discovery, Security Center, the Model Context Protocol client and server, and the GRC and Smart Assessment plugins, are installed automatically as dependencies. To see every dependency for an application, open the application in Application Manager.

<table id="table_plugins_additional"><thead><tr><th>

Plugin

</th><th>

Plugin ID

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

`sn_aict`

</td><td>

Centralizes AI governance across the enterprise, including AI discovery, asset lifecycle management, risk and compliance, and value measurement.

</td></tr><tr><td>

AI Discovery

</td><td>

`sn_ai_disc`

</td><td>

Discovers AI assets, agents, and usage from hyperscaler and external AI platform connectors.

</td></tr><tr><td>

AI SGC Discovery

</td><td>

`sn_ai_sgc_disc`

</td><td>

Installs the Service Graph Connectors that AI Discovery uses.

</td></tr><tr><td>

AI Service Graph Connectors for Amazon, Google, LangGraph, and Microsoft

</td><td>

-   `sn_ai_disc_aws_sgc`
-   `sn_ai_disc_gcp_sgc`
-   `sn_langgraph_integ`
-   `sn_ai_msft_integ`

</td><td>

Discover AI assets from Amazon, Google, LangGraph, and Microsoft platforms.

</td></tr><tr><td>

AI Trace Collector

</td><td>

`sn_aict_trace_coll`

</td><td>

Collects trace data from external AI platforms for monitoring and evaluation.

</td></tr></tbody>
</table>The following plugins aren't installed with AI Control Tower. Install them separately to add the features that they provide.

|Plugin|Plugin ID|Description|
|------|---------|-----------|
|Enterprise Architecture for AICT|`sn_ea_aict`|Provides the shared many-to-many data model connecting AI systems and business applications, independently of the plugin. For more information, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-ea-common-upgrade-considerations.md).|
|Shadow AI Detection|`sn_shadow_ai`|Detects unsanctioned AI use on your network and endpoints.|

## Roles installed

Roles installed with AI Control Tower are described in the following tables. When you assign a role, you also assign the roles that it contains.

<table id="table_roles_installed"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI Steward

 \[sn\_ai\_governance.ai\_steward\]

</td><td>

Leads the execution of AI Control Tower initiatives and coordinates governance activities between innovation, legal, security, risk, and compliance teams. Configures governance and approval workflows, approves or rejects AI asset approval requests, configures Multi-instance Management, activates hyperscaler connections, sets up MCP client connections, and deactivates or reinstates AI agents to contain security risks.

</td><td>

-   aig\_admin
-   sn\_ai\_asset\_mgmt.ai\_asset\_owner
-   sn\_ai\_case\_mgmt.ai\_case\_manager
-   sn\_ai\_governance.integration.rest
-   sn\_ai\_governance.workspace\_user
-   sn\_ai\_opty\_engine.ai\_insight\_user
-   sn\_ai\_policy\_fwk.admin
-   sn\_ai\_security.operator
-   sn\_ai\_security.viewer
-   sn\_aia.viewer
-   sn\_awh\_config.awh\_admin
-   sn\_awh\_config.data\_read
-   sn\_doc.admin
-   sn\_generative\_ai.data\_steward
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader
-   sn\_mif.mif\_admin
-   sn\_mif.mif\_read
-   sn\_na\_conv\_eval.eval\_admin
-   sn\_nowassist\_admin.user
-   sn\_query\_gen.user
-   sn\_shadow\_ai.admin
-   sn\_vsc.task\_manager
-   telemetry\_query\_service\_user

</td></tr><tr><td>

Workspace Administrator

 \[sn\_ai\_governance.workspace\_admin\]

</td><td>

Has all AI Steward permissions. Configures the cards on AI Control Tower pages, including titles, chart types, list sizes, and record conditions. Card configurations that this role saves apply to all users on the instance.

</td><td>

-   sn\_ai\_governance.ai\_steward
-   sn\_ai\_governance.workspace\_user
-   aix\_config\_admin

</td></tr><tr><td>

AI Control Tower Workspace User

 \[sn\_ai\_governance.workspace\_user\]

</td><td>

Accesses the AI Control Tower home page and the AI Portfolio tab. Owns and manages AI assets.

</td><td>



</td></tr><tr><td>

AI Asset Owner

 \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Manages AI systems, AI models, datasets, and prompts through the asset lifecycle from intake to retirement. Confirms that AI assets are represented accurately and kept up to date, and marks Deploy-phase lifecycle tasks complete.

</td><td>

-   aix\_read
-   sn\_ai\_governance.workspace\_user
-   sn\_ai\_opty\_engine.ai\_insight\_user
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user
-   sn\_vsc.task\_manager

</td></tr><tr><td>

AI Observability Admin

 \[sn\_ai\_observe.ai\_observability\_admin\]

</td><td>

Accesses and manages evaluation data, including sessions, traces, and spans.

</td><td>

None

</td></tr><tr><td>

AI Policy Framework Admin

 \[sn\_ai\_policy\_fwk.admin\]

</td><td>

Has full access to AI Policy Framework records, including execution audit records.

</td><td>

sn\_ai\_policy\_fwk.viewer

</td></tr><tr><td>

AI Policy Framework Viewer

 \[sn\_ai\_policy\_fwk.viewer\]

</td><td>

Views and reports on AI Policy Framework connectors, actions, and instances, and views execution audit history.

</td><td>

None

</td></tr><tr><td>

AI Security Operator

 \[sn\_ai\_security.operator\]

</td><td>

Deactivates and reinstates AI agents using kill switch protocol. Also views the agent containment list. Every AI Steward has this role.

</td><td>

sn\_ai\_security.viewer

</td></tr><tr><td>

AI Security Viewer

 \[sn\_ai\_security.viewer\]

</td><td>

Views AI Security and Privacy information, including the Access Map.

</td><td>

-   data\_privacy\_channel\_auditor
-   data\_privacy\_telemetry\_accessor
-   sn\_aia.viewer
-   sn\_na\_analytics.viewer

</td></tr><tr><td>

AWH Admin

 \[sn\_awh\_config.awh\_admin\]

</td><td>

Configures AWH for AI Control Tower.

</td><td>

-   sn\_awh\_config.awh\_read
-   sn\_awh\_config.data\_read

</td></tr><tr><td>

AWH Reader

 \[sn\_awh\_config.awh\_read\]

</td><td>

Views the AWH configuration.

</td><td>

sn\_awh\_config.data\_read

</td></tr><tr><td>

AI Discovery Admin

 \[sn\_ai\_disc.discovery\_admin\]

</td><td>

Administers AI Discovery and its connections. Installed with the AI Discovery plugin.

</td><td>

-   connection\_admin
-   sn\_ai\_governance.ai\_steward
-   sn\_cmdb\_int\_util.sgc\_admin

</td></tr></tbody>
</table>For the roles installed with AI Risk and Compliance and AI Case Management, see [Roles and responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/roles-installed-with-ai-risk-and-compliance.md).

<table id="table_roles_integration"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration REST

 \[sn\_ai\_governance.integration.rest\]

</td><td>

Provides read-only access to AI asset inventory and governance data for ServiceNow products and third-party platforms, including asset details, assessments, risks, controls, issues, policy exceptions, and lifecycle information.

</td></tr><tr><td>

External Registry Editor

 \[sn\_ai\_governance.external\_registry\_editor\]

</td><td>

Allows an approved partner service account, such as Microsoft Agent365, to sync discovered agent registration status through the External Registration Sync API.

</td></tr><tr><td>

Retrieve Publishable Asset

 \[sn\_ai\_governance.retrieve\_publishable\_asset\]

</td><td>

Allows a service account to retrieve ServiceNow AI assets that are marked as publishable. Intended for third-party platforms such as Microsoft Admin Center.

</td></tr><tr><td>

AI Data Sender

 \[sn\_ai\_observe.ai\_data\_sender\]

</td><td>

Sends and retrieves evaluation data through API calls.

</td></tr><tr><td>

AWH Integration REST

 \[sn\_awh\_config.integration.rest\]

</td><td>

Provides access to the AWH Gateway REST API.

</td></tr></tbody>
</table>## Tables installed

The following tables store the AI assets, governance records, and monitoring data that you work with in AI Control Tower.

<table id="table_tables_installed"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI System Digital Asset

 \[alm\_ai\_system\_digital\_asset\]

</td><td>

Records for AI system assets. Captures class, state, ownership, model category, and the associated models and datasets.

</td></tr><tr><td>

AI Model Digital Asset

 \[alm\_ai\_model\_digital\_asset\]

</td><td>

Records for AI model assets. Captures training and evaluation datasets and defaults the category to AI Model.

</td></tr><tr><td>

AI Dataset Digital Asset

 \[alm\_ai\_dataset\_digital\_asset\]

</td><td>

Records for AI dataset assets. Captures dataset relationships and defaults the category to AI Dataset.

</td></tr><tr><td>

AI Prompt Digital Asset

 \[alm\_ai\_prompt\_digital\_asset\]

</td><td>

Records for AI prompt assets. Prompt assets are created from the AI Control Tower workspace only, not through Service Catalog.

</td></tr><tr><td>

MCP Digital Asset

 \[alm\_mcp\_digital\_asset\]

</td><td>

Records for Model Context Protocol \(MCP\) server assets, including a link to the external server documentation.

</td></tr><tr><td>

AI Asset Governance Details

 \[sn\_ai\_governance\_asset\_governance\_details\]

</td><td>

Primary lifecycle governance record. Provides end-to-end lifecycle visibility, governance state tracking, and oversight across the Assess, Build &amp; Test, and Deploy phases.

</td></tr><tr><td>

AI Asset Lifecycle

 \[sn\_ai\_governance\_lifecycle\]

</td><td>

Lifecycle phase definitions. AI Stewards can extend the default Assess, Build &amp; Test, and Deploy phases by adding records to this table and updating the corresponding playbook.

</td></tr><tr><td>

AI Asset Approval Request

 \[sn\_ai\_governance\_assessment\_request\]

</td><td>

Approval requests that operationalize the lifecycle defined in the AI Asset Governance Details record. Configured with Type = "AI Governance Lifecycle" and drives progression across the lifecycle phases.

</td></tr><tr><td>

AI Asset Approval Task

 \[sn\_ai\_governance\_assessment\_task\]

</td><td>

Discrete governance and compliance tasks created within an approval request. Each task represents an activity across the Assess, Build &amp; Test, or Deploy phase.

</td></tr><tr><td>

AI Asset Use and Purpose

 \[sn\_ai\_governance\_asset\_use\_purpose\]

</td><td>

Records the intended outcome, usage area, output type, impacted stakeholders, human involvement, interaction model, and autonomy level for each AI system. Used as input to risk classification and impact assessments.

</td></tr><tr><td>

AI System

 \[sn\_grc\_ai\_gov\_ai\_system\]

</td><td>

Operational AI system record used by AI Risk and Compliance. Drives risk assessments, compliance workflows, and regulatory tracking. Created when the AI Steward starts the lifecycle review for an AI system.

</td></tr><tr><td>

Evaluated sessions

 \[sn\_ai\_observe\_ai\_session\]

</td><td>

Records for evaluated AI sessions. Captures cost, token counts, and quality, safety, and task completeness scores for each session.

</td></tr><tr><td>

Evaluated traces

 \[sn\_ai\_observe\_ai\_trace\]

</td><td>

Records for the evaluated traces in a session. Captures cost, token counts, duration, and scores such as quality, safety, completeness, tone, and output toxicity.

</td></tr><tr><td>

Connections

 \[sn\_aict\_trace\_coll\_collector\_config\]

</td><td>

Connections that collect trace data from external AI platforms. Captures the credential, MID Server, collection frequency, and last collection status. Installed with the AI Trace Collector plugin.

</td></tr><tr><td>

AI Usage

 \[sn\_ai\_disc\_ai\_usage\]

</td><td>

Usage records imported from hyperscaler and external AI platform connectors. Installed with the AI Discovery plugin. Consumed by the AI Control Tower value dashboard.

</td></tr><tr><td>

Business Application Product Model Map

 \[sn\_ea\_aict\_ba\_product\_model\_map\]

</td><td>

Many-to-many association table between AI System Component Product Model records and business applications. Installed with the Enterprise Architecture for AICT plugin.

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Migrate BA Product Model Map from EA Workspace|Migrates existing AI system-to-business application associations from the Enterprise Architecture Workspace map \[sn\_apm\_ws\_ba\_product\_model\_map\] to the Enterprise Architecture for AICT map \[sn\_ea\_aict\_ba\_product\_model\_map\]. Installed with the Enterprise Architecture for AICT plugin. This job doesn't run automatically. For steps, see [Run the Migrate BA Product Model Map job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.md).|

**Related topics**  


[Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-ea-common-upgrade-considerations.md)

[Run the Migrate BA Product Model Map job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.md)

