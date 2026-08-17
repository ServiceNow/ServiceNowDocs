---
title: AI in ITOM Visibility
description: AI features in ITOM Visibility help administrators automate service map creation, diagnose discovery issues, manage certificates, request firewall rules, and generate incident resolution artifacts using generative AI and agentic workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/explore-ai-in-itom-visibility.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 8
keywords: [Now Assist, AI, ITOM Visibility, generative AI, agentic AI]
breadcrumb: [ITOM Visibility, IT Operations Management]
---

# AI in ITOM Visibility

AI features in ITOM Visibility help administrators automate service map creation, diagnose discovery issues, manage certificates, request firewall rules, and generate incident resolution artifacts using generative AI and agentic workflows.

AI features in ITOM Visibility span several products. The following tables summarize all available AI features by type and product.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Agentic workflows

Agentic workflows in ITOM Visibility use AI agents to complete investigation and management tasks autonomously or with minimal administrator input.

<table id="table_explore-visibility-agentic-workflows"><thead><tr><th>

Product

</th><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Discovery

</td><td>

Pattern diagnostic agentic workflow

</td><td>

Investigates missing CI attributes in pattern-based discovery. The workflow identifies the attribute gap, parses discovery logs, determines the root cause, and suggests a remediation — all from the ServiceNow Otto panel. Uses two agents: the Pattern diagnostic agent and the EF Remediation Agent.

</td><td>

A discovery administrator notices that a CI attribute is missing and wants to identify the root cause and a fix without manually navigating discovery logs and tables.

</td><td>

[Pattern diagnostic agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/pattern-diagnostic-agentic-workflow.md)

</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

Firewall Management Task Creation agentic workflow

</td><td>

Uses AI to accept natural-language firewall rule requests, extract required parameters, run a risk analysis, and create a rule task. The risk level determines whether the task is created automatically or requires confirmation.

</td><td>

A firewall administrator wants to request a new firewall rule by describing it in plain language rather than filling out a form manually.

</td><td>

-   [Firewall rule requests using agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-rule-requests-ai-workflow.md)
-   [Request firewall rules using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-rule-requests-ai-workflow.md)

</td></tr><tr><td>

Service Mapping

</td><td>

Analyze potential impact agentic workflow

</td><td>

Analyzes how a change request might affect relevant servers and services. The agent verifies prerequisites, retrieves the change request, selects up to 10 affected servers, identifies matches with suggested services, and displays an impact analysis in the ServiceNow Otto panel. The analysis is also saved to the change request work notes.

</td><td>

An operator or change manager wants to assess the risk of a change request before approving it, without manually reviewing all affected CIs.

</td><td>

-   [Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Assess a change request with the Analyze potential impact workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/use-now-assist-analyze-impact-agentic-workflow.md)
-   [Activate the Service Mapping Candidate skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidate-skill.md)
-   [Activate the Service Mapping Candidates Impact skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidates-impact-skill.md)

</td></tr><tr><td>

LEAP

</td><td>

Ansible discovery agent

</td><td>

Analyzes automation opportunities and uses AI-powered semantic matching to identify relevant Ansible job templates from Ansible Automation Platform. Presents discovered templates to the LEAP administrator for step-to-job mapping.

</td><td>

A LEAP administrator wants to find the most relevant Ansible job templates for an automation opportunity without manually searching the Ansible catalog.

</td><td>

-   [Ansible automation integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-automation-integration-overview.md)
-   [Ansible discovery agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-discovery-agent.md)

</td></tr><tr><td>

LEAP

</td><td>

Ansible execution agent

</td><td>

Automatically launches mapped Ansible job templates during incident remediation in the Service Operations Workspace. Reports execution status back to the incident responder.

</td><td>

An incident responder wants to trigger an Ansible automation directly from the Service Operations Workspace during active incident resolution, without switching to the Ansible platform.

</td><td>

-   [Ansible automation integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-automation-integration-overview.md)
-   [Execute Ansible automations for incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/execute-ansible-automations-for-incidents.md)

</td></tr></tbody>
</table>## AI agents

Standalone AI agents in ITOM Visibility run autonomously on a schedule or in response to a trigger, without requiring user input for each operation.

<table id="table_explore-visibility-ai-agents"><thead><tr><th>

Product

</th><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Service Mapping

</td><td>

Service Mapping AI Agent

</td><td>

Autonomously creates service maps from ML-powered Application Service Candidates \(ASCs\). The agent evaluates candidates, filters noise such as monitoring clients and operating system processes, and creates the service topology in the CMDB. Created service maps are set to non-operational by default for administrator review. Runs automatically every 15 minutes after activation.

</td><td>

A Service Mapping administrator wants to process a large volume of ML-powered candidates and create service maps automatically, without reviewing each candidate individually.

</td><td>

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Service Mapping

</td><td>

Business App Mapping AI Agent

</td><td>

Automatically creates CSDM "Uses::Used by" relationships between Business Applications and discovered Application Services using AI semantic search. High-confidence matches are connected automatically. Medium-confidence matches are saved to a staging table for administrator review.

</td><td>

A Service Mapping administrator wants to connect discovered application services to their business application context in the CSDM without manually mapping each relationship.

</td><td>

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Certificate Inventory and Management

</td><td>

Certificate renewal AI agent

</td><td>

Uses AI to automatically renew a single TLS certificate through a conversational prompt. The agent guides the user through the renewal process and provides a link to the task record when complete.

</td><td>

A PKI administrator wants to renew a certificate without manually navigating the renewal workflow.

</td><td>

[Automatically renew certificates using the AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/automatically-renew-cert-now-assist.md)

</td></tr><tr><td>

LEAP

</td><td>

LEAP AI agent

</td><td>

Uses automation opportunities created by LEAP analysis to generate artifacts — problem records, AI-enhanced knowledge base articles, or playbooks — based on user requests. The agent is turned on by default.

</td><td>

A LEAP administrator wants to convert a recurring incident pattern into a problem record, a structured knowledge base article, or a playbook without manually authoring each artifact.

</td><td>

-   [LEAP AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/leap-ai-agent.md)
-   [Create LEAP problem records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/create-problem-records.md)
-   [Generate LEAP knowledge base articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generate-aiops-leap-knowledge-base.md)
-   [Generate LEAP playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generate-playbooks.md)

</td></tr></tbody>
</table>## Generative AI skills

Generative AI skills in ITOM Visibility are discrete, on-demand capabilities that administrators invoke to generate analyses, summaries, or insights for a specific discovery error set, service map, or incident pattern.

|Product|AI feature|Description|Use case|Resources|
|-------|----------|-----------|--------|---------|
|Service Mapping|Service Mapping Candidate skill|Classifies application service candidates and generates names and descriptions for the processes within them. Retrieves publisher, product, and description details for each process, then generates a name and description for the candidate. Active by default. Used by the Analyze potential impact agentic workflow.|A Service Mapping administrator wants AI to automatically name and describe application service candidates during a change impact analysis, without manually reviewing each process.|[Activate the Service Mapping Candidate skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidate-skill.md)|
|Service Mapping|Service Mapping Candidates Impact skill|Analyzes connections and effects on servers following a change request, and generates an impact summary of affected components. Active by default. Used by the Analyze potential impact agentic workflow.|A Service Mapping administrator wants AI to automatically summarize which components are affected by a change request, without manually tracing server dependencies.|[Activate the Service Mapping Candidates Impact skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidates-impact-skill.md)|
|Discovery|AI Insights for discovery errors|Analyzes current Discovery errors and surfaces the highest-impact and highest-leverage errors in the Discovery Admin Workspace Diagnostics page. Each insight includes a summary of affected schedules and devices, and recommended remediation steps. Powered by ServiceNow Otto for Error Framework.|A discovery administrator wants to quickly identify which errors to resolve first to have the greatest effect on discovery health, without reviewing every error individually.|[Discovery Admin Workspace Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md)|
|LEAP|AI-generated resolution steps|Uses generative AI to analyze grouped incidents and generate structured resolution steps for each automation opportunity. Resolution steps can be reviewed and modified before use.|A LEAP administrator wants to produce actionable resolution guidance for a recurring incident pattern without manually authoring steps from scratch.|[Generate and modify resolution steps in LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generating-and-modifying-resolution-steps.md)|

