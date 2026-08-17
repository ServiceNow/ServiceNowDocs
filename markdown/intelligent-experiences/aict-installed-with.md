---
title: Components installed with AI Control Tower
description: Several types of components are installed with activation of AI Control Tower, including plugins, user roles, and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-installed-with.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 5
keywords: [AI Control Tower, installed components, plugins, roles, tables]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# Components installed with AI Control Tower

Several types of components are installed with activation of AI Control Tower, including plugins, user roles, and tables.

## Plugins installed

Activation of AI Control Tower installs the following plugins. Additional plugins listed in [Additional plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-installed-with.md) extend AI Control Tower with capabilities for discovery, security, dashboards, and reporting.

|Plugin|Plugin ID|Description|
|------|---------|-----------|
|AI Control Tower Core|`com.sn_ai_governance`|Centralizes AI governance across the enterprise by combining AI assets and controls in a single hub.|
|AI Asset Management|`com.sn_ai_asset_mgmt`|Tracks and manages the lifecycle of AI assets such as systems, models, datasets, and prompts.|
|AI Risk and Compliance Management|`com.sn_grc_ai_gov`|Manages AI risks across their lifecycle, including risk classification, mapping to regulatory authority documents, and policy compliance.|
|AI Case Management|`com.sn_ai_case_mgmt`|Tracks, triages, and resolves inquiries and incidents related to AI assets.|
|AI Risk and Compliance Integration with Control Tower|`com.sn_grc_ai_irm_intg`|Surfaces risk posture, compliance status, and case workflows directly in AI Control Tower so you can manage AI use cases against regulatory frameworks.|
|AI Control Tower Evaluations|`com.sn_ai_evaluations`|Enables the evaluation framework, scoring engine, and monitoring components for your AI systems.|
|AI Risk and Compliance Content \(optional\)|`com.sn_grc_ai_gov_cont`|Loads frameworks, citations, control objectives, risk statements, and assessment templates for the EU AI Act and the NIST AI Risk Management Framework.|

The following plugins extend AI Control Tower with capabilities for discovery, security and privacy monitoring, value and engagement dashboards, and reporting.

|Plugin|Plugin ID|Description|
|------|---------|-----------|
|AI Security and Privacy|sn\_ai\_security|Provides security and privacy monitoring for AI assets.|
|AI Discovery|sn\_ai\_disc|Discovers AI assets, agents, and usage from hyperscaler and external AI platform connectors.|
|AI Control Tower for Now Assist|sn\_aict\_nowassist|Syncs Now Assist AI skills into the AI Control Tower inventory.|
|Value Dashboard for AI Control Tower|sn\_ai\_value|Provides the Value dashboard for measuring AI investment return and adoption.|
|Health Dashboard for AI Control Tower|sn\_ai\_health|Provides the Health dashboard for monitoring the operational health of AI systems.|
|Engagement Dashboard for AI Control Tower|sn\_ai\_engagement|Provides the Engagement dashboard for tracking user engagement with AI assets.|
|AWH for AI Control Tower|sn\_awh\_config|Configures the Agent Workspace Hub for AI Control Tower.|
|ServiceNow AI Lens|sn\_ai\_lens|Provides AI reporting and lens capabilities.|
|Asset Classes|sn\_ent|Required for AI Assets API access. Activate this plugin before configuring API-based integrations to the AI Asset records.|

## Roles installed

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

Leads the execution of AI Control Tower initiatives, configures governance and approval workflows, and oversees AI asset adoption across the enterprise. Approves or rejects AI asset approval requests, configures Multi-instance Management, activates hyperscaler connections, and sets up MCP client connections.

</td><td>

-   sn\_ai\_governance.workspace\_admin
-   sn\_nowassist\_admin.user
-   sn\_aia.admin
-   aig\_admin
-   sn\_mcp\_client.admin

</td></tr><tr><td>

AI Asset Owner

 \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Manages AI systems, AI models, datasets, and prompts through the asset lifecycle from intake to retirement. Confirms that AI assets are represented accurately and kept up to date, and marks Deploy-phase lifecycle tasks complete. Administers the Smart Assessment Editor \(SAE\) application.

</td><td>

sn\_smart\_asmt.assessment\_admin

</td></tr><tr><td>

AI Risk and Compliance Admin

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\]

</td><td>

Configures risk assessment methodologies, risk contribution factors, and impact assessment templates. Defines automation rules for impact assessments, sets up and profiles AI case types, and deletes AI systems.

</td><td>

-   sn\_risk.admin
-   sn\_smart\_asmt.template\_manager
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager
-   sn\_smart\_asmt.assessment\_admin
-   sn\_grc\_workspace.state\_model\_admin
-   sn\_smart\_asmt.template\_contributor
-   sn\_compliance.admin
-   sn\_compliance.control\_framework\_admin
-   sn\_compliance.library\_admin
-   sn\_compliance.policy\_admin

</td></tr><tr><td>

AI Risk and Compliance Manager

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]

</td><td>

Accesses all AI systems on the instance. Initiates impact assessments, risk assessments, and control attestations, and manages the lifecycle of AI systems.

</td><td>

-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst
-   sn\_smart\_asmt.template\_contributor
-   sn\_smart\_asmt.template\_manager
-   sn\_risk\_advanced.risk\_asmt\_project\_manager
-   sn\_ai\_case\_mgmt.ai\_case\_manager
-   sn\_risk.manager
-   sn\_compliance.control\_framework\_manager
-   sn\_compliance.library\_manager
-   sn\_compliance.policy\_manager

</td></tr><tr><td>

AI Risk and Compliance Analyst

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]

</td><td>

Performs impact assessments, risk assessments, control attestations, and lifecycle management on the AI systems assigned to the analyst.

</td><td>

-   sn\_ai\_case\_mgmt.ai\_case\_analyst
-   sn\_smart\_asmt.assessment\_reader
-   sn\_smart\_asmt.template\_reader
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user
-   sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader
-   sn\_grc\_workspace.user
-   sn\_grc\_workspace.state\_model\_reader
-   sn\_risk.user
-   sn\_risk\_advanced.ara\_creator
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk\_advanced.ara\_approver
-   sn\_risk\_advanced.risk\_asmt\_project\_user
-   sn\_compliance.control\_framework\_user
-   sn\_compliance.library\_user
-   sn\_compliance.policy\_user

</td></tr><tr><td>

AI Risk and Compliance User

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\]

</td><td>

Creates AI cases through Employee Center, works on assigned tasks, and completes control attestations.

</td><td>

-   sn\_grc\_workspace.assessment\_template\_configuration\_reader
-   sn\_smart\_asmt.actor
-   sn\_grc\_workspace.user
-   sn\_smart\_asmt.assessment\_reader
-   sn\_risk\_advanced.risk\_asmt\_project\_reader
-   sn\_grc.business\_user
-   sn\_compliance.control\_framework\_business\_user
-   sn\_compliance.library\_business\_user
-   sn\_compliance.policy\_business\_user

</td></tr><tr><td>

AI Risk and Compliance Reader

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_reader\]

</td><td>

Reads AI system records and AI impact assessment records.

</td><td>

-   sn\_grc\_workspace.user
-   sn\_grc\_workspace.state\_model\_reader
-   sn\_risk.reader
-   sn\_compliance.library\_reader
-   sn\_compliance.control\_framework\_reader
-   sn\_compliance.policy\_reader

</td></tr><tr><td>

AI System Reader

 \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_ai\_system\_reader\]

</td><td>

Reads AI system records in both the AI Control Tower workspace and the AI Risk and Compliance workspace.

</td><td>

None

</td></tr><tr><td>

AI Case Business User

 \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\]

</td><td>

Creates AI cases and AI inquiries in Employee Center.

</td><td>

sn\_grc\_case\_mgmt.grc\_case\_business\_user

</td></tr><tr><td>

AI Case Analyst

 \[sn\_ai\_case\_mgmt.ai\_case\_analyst\]

</td><td>

Reviews AI cases and AI inquiries assigned to the analyst. Identifies and manages impacted policies, regulations, and compliance risks, and addresses root-cause issues.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_analyst
-   sn\_ai\_case\_mgmt.ai\_case\_business\_user

</td></tr><tr><td>

AI Case Manager

 \[sn\_ai\_case\_mgmt.ai\_case\_manager\]

</td><td>

Reviews all AI cases and AI inquiries across the organization. Monitors case volume and severity and oversees case resolution.

</td><td>

-   sn\_ai\_case\_mgmt.ai\_case\_analyst
-   sn\_grc\_case\_mgmt.grc\_case\_manager

</td></tr><tr><td>

AI Case Admin

 \[sn\_ai\_case\_mgmt.ai\_case\_admin\]

</td><td>

Configures AI case types, state models, assignment rules, and assessment templates. Deletes AI cases.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_admin
-   sn\_ai\_case\_mgmt.ai\_case\_manager

</td></tr></tbody>
</table>## Tables installed

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

AI System Component Product Model

 \[cmdb\_ai\_system\_component\_product\_model\]

</td><td>

Product model attributes for AI system assets. Linked 1:1 to the AI System Digital Asset record.

</td></tr><tr><td>

AI Model Product Model

 \[cmdb\_ai\_model\_product\_model\]

</td><td>

Product model attributes for AI model assets. Linked many-to-one to the AI Model Digital Asset record.

</td></tr><tr><td>

AI Dataset Product Model

 \[cmdb\_ai\_dataset\_product\_model\]

</td><td>

Product model attributes for AI dataset assets.

</td></tr><tr><td>

AI Prompt Product Model

 \[cmdb\_ai\_prompt\_product\_model\]

</td><td>

Product model attributes for AI prompt assets.

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

AI Usage

 \[sn\_ai\_disc\_ai\_usage\]

</td><td>

Usage records imported from hyperscaler and external AI platform connectors. Installed with the AI Discovery plugin. Consumed by the AI Control Tower value dashboard.

</td></tr></tbody>
</table>