---
title: Ansible discovery agent
description: The Ansible discovery agent analyzes automation opportunities and identifies relevant Ansible job templates using AI-powered semantic matching and historical execution patterns.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-discovery-agent.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2025-01-07"
reading_time_minutes: 1
keywords: [Ansible Discovery Agent, automation discovery, job templates, semantic matching]
breadcrumb: [Ansible automation integration, Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Ansible discovery agent

The Ansible discovery agent analyzes automation opportunities and identifies relevant Ansible job templates using AI-powered semantic matching and historical execution patterns.

The Ansible discovery agent automates the process of finding relevant Ansible job templates for automation opportunities. The agent eliminates the manual effort required by automation engineers to search and identify appropriate automation resources.

## Discovery process

The Ansible discovery agent follows this process to identify relevant job templates:

1.  Parses the problem description of the automation opportunity for keywords and context
2.  Queries Ansible Automation Platform via the Ansible MCP server to retrieve available job templates
3.  Applies AI-powered matching to identify relevant job templates based on problem description similarity using semantic natural language processing
4.  Presents discovered job templates to the LEAP administrator for step-to-job mapping

## Matching capabilities

The agent uses these techniques to match automation opportunities with job templates:

-   **Semantic analysis**

    Analyzes the meaning and context of problem descriptions to identify relevant automation patterns.

-   **Keyword extraction**

    Identifies key terms and technical concepts from automation opportunity descriptions.


## Integration points

The Ansible discovery agent integrates with these components:

-   AI Teammate Dashboard: Entry point for automation engineers and LEAP administrators.
-   Ansible MCP server: Secure API access to Ansible Automation Platform job templates.
-   LEAP clustering engine: Source of automation opportunity data and problem descriptions.
-   Step-to-job mapping UI: Destination for discovered job template recommendations.

