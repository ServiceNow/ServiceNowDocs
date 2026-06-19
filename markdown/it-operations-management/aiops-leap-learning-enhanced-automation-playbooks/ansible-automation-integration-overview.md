---
title: Ansible automation integration
description: The Ansible automation integration connects LEAP with Ansible Automation Platform to enable AI-driven discovery of relevant job templates and automated incident remediation from the Service Operations Workspace.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/ansible-automation-integration-overview.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2025-01-07"
reading_time_minutes: 1
keywords: [LEAP, Ansible, automation, integration, MCP]
breadcrumb: [Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Ansible automation integration

The Ansible automation integration connects LEAP with Ansible Automation Platform to enable AI-driven discovery of relevant job templates and automated incident remediation from the Service Operations Workspace.

The Ansible automation integration addresses the critical operational gap of lack of automated remediation capabilities during incident resolution.

## Key capabilities

The integration provides these core capabilities:

-   **AI-driven automation discovery**

    LEAP automatically identifies relevant Ansible job templates for automation opportunities using semantic analysis.

-   **Step-to-job mapping**

    The integration enables LEAP administrators to map discovered Ansible job templates to specific resolution steps through an intuitive UI.

-   **Automated incident remediation**

    The integration allows incident responders to execute mapped Ansible automations directly from the Service Operations Workspace during incident resolution.

-   **Manual step handling**

    The integration supports mixed workflows where some steps require manual intervention while others can be automated.


## Integration architecture

The integration uses these key components:

-   Ansible discovery agent: Analyzes automation opportunities and identifies candidate job templates
-   Ansible execution agent: Executes mapped automation opportunities during incident remediation
-   Ansible MCP server: Provides secure API access to Ansible Automation Platform
-   Step-to-job mapping store: Maintains the relationship between resolution steps and Ansible job templates

## Workflow overview

The integration follows this high-level workflow:

1.  The Ansible discovery agent analyzes automation opportunities and discovers relevant job templates
2.  LEAP administrators map discovered job templates to specific resolution steps
3.  When incidents occur, LEAP predicts the automation opportunity group
4.  If mappings exist, automation options are presented to incident responders
5.  The Ansible execution agent launches selected automations and reports status

## Benefits

The Ansible automation integration provides these benefits:

-   Reduces mean time to resolution \(MTTR\) by automating incident remediation
-   Eliminates the requirement to search for relevant job templates or automation playbooks
-   Increases automation utilization across the organization
-   Provides structured linkage between automation opportunities and Ansible job templates
-   Enables consistent, repeatable incident resolution processes

