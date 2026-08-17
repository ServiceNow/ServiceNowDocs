---
title: Exploring AI in LEAP
description: AI-powered features in LEAP help administrators generate resolution steps, create problem records, publish knowledge base articles, build playbooks, and discover and execute Ansible automations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/exploring-ai-in-leap.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, LEAP, AI agent, resolution steps, playbooks, knowledge base, Ansible]
breadcrumb: [Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Exploring AI in LEAP

AI-powered features in LEAP help administrators generate resolution steps, create problem records, publish knowledge base articles, build playbooks, and discover and execute Ansible automations.

LEAP includes several AI-powered features. All features require ServiceNow Otto for IT Operations Management \(ITOM\) to be installed.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

<table id="table_exploring-ai-in-leap"><thead><tr><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

AI-generated resolution steps

</td><td>

Uses generative AI to analyze grouped incidents and generate structured resolution steps for each automation opportunity. Resolution steps can be reviewed and modified before use.

</td><td>

A LEAP administrator wants to produce actionable resolution guidance for a recurring incident pattern without manually authoring steps from scratch.

</td><td>

[Generate and modify resolution steps in LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generating-and-modifying-resolution-steps.md)

</td></tr><tr><td>

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

</td></tr><tr><td>

Ansible discovery agent

</td><td>

Analyzes automation opportunities and uses AI-powered semantic matching to identify relevant Ansible job templates from Ansible Automation Platform. Presents discovered templates to the LEAP administrator for step-to-job mapping.

</td><td>

A LEAP administrator wants to find the most relevant Ansible job templates for an automation opportunity without manually searching the Ansible catalog.

</td><td>

-   [Ansible automation integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-automation-integration-overview.md)
-   [Ansible discovery agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-discovery-agent.md)

</td></tr><tr><td>

Ansible execution agent

</td><td>

Automatically launches mapped Ansible job templates during incident remediation in the Service Operations Workspace. Reports execution status back to the incident responder.

</td><td>

An incident responder wants to trigger an Ansible automation directly from the Service Operations Workspace during active incident resolution, without switching to the Ansible platform.

</td><td>

-   [Ansible automation integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-automation-integration-overview.md)
-   [Execute Ansible automations for incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/execute-ansible-automations-for-incidents.md)

</td></tr></tbody>
</table>