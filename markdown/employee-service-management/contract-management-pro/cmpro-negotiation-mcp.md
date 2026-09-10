---
title: Contract Management Pro MCP Server
description: Contract fulfillers and reviewers can review and redline contract documents in an external AI tool that retrieves approved playbook containing clause level organizational positions from Contract Management Pro through the MCP Server. The AI tool proposes redlines that follow the playbook guidance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-negotiation-mcp.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Contract negotiation, MCP server, Model Context Protocol, Contract analysis playbook, AI contract negotiation, External AI tools for contract management pro]
breadcrumb: [AI capabilities in Contract Management Pro, Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract Management Pro MCP Server

Contract fulfillers and reviewers can review and redline contract documents in an external AI tool that retrieves approved playbook containing clause level organizational positions from Contract Management Pro through the MCP Server. The AI tool proposes redlines that follow the playbook guidance.

**Important:**

Generative AI may produce inaccurate or incomplete information. Review AI-generated redlines and playbook guidance for accuracy before you accept them.

## Contract Management Pro MCP Server Overview

The Contract Management Pro MCP Server connects MCP-compatible external AI tools to Contract Management Pro. This enables contract fulfillers and reviewers to access approved playbook containing clause level organizational positions while reviewing documents. When an AI tool calls the playbook tool, the server returns the active playbook for the contract type.

To configure MCP server, see [Configure Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-install-mcp-app.md).

## Key benefits

Contract analysis with external AI tools provides the following benefits:

-   AI-proposedredlines that follows your approved playbooks containing clause level organizational positions, not general guidance.
-   Fulfillers and reviewers can use their preferred AI tool while Contract Management Pro manages the playbook content and access control.
-   Separate playbooks per contract type, auto-selected so reviews use the right guidance.
-   Contract playbooks for contract types are available in centralized location within Contract Management Pro, so administrators can handle changes centrally instead of maintaining playbooks in different locations or local folders.

## Contract states for playbook retrieval

The playbook tool returns playbook guidance only when the contract is in one of the following states and the user has thesn\_cm\_gen\_ai.ai\_contract\_fulfiller role:

-   Contract fulfillers \(Assigned to, Collaborator, or Group manager\) can retrieve playbooks when the contract is in the Work in Progress state.
-   Contract reviewers can retrieve playbooks when the contract is in the Awaiting Review state and review task is in Work in Progress state.

