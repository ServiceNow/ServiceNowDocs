---
title: Configuring builder controls
description: Keep a human review between building an AI asset and deploying it by requiring AI steward approval for each asset type and triggering approval requests automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configuring-builder-controls.html
release: australia
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring builder controls

Keep a human review between building an AI asset and deploying it by requiring AI steward approval for each asset type and triggering approval requests automatically.

## AI steward approval for AI assets

When AI steward approval is required for an asset type, an AI steward must approve each asset of that type before it can be deployed. You set the requirement separately for each asset type, so requiring approval for one type doesn't change the requirement for the others.

-   **AI systems**

    AI skills and agents need AI steward approval before they're deployed.

-   **MCP servers**

    An MCP server can't be used by agents until an AI steward approves it. In AI Agent Studio, an unapproved server doesn't display its tools, and a message directs the builder to check the MCP server record and contact an AI steward. For the approval workflow, see [MCP server approval playbook workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-mcp-server-approval-playbook-workflow.md).

-   **AI models**

    An AI model needs AI steward approval before AI systems can use it.


Approval isn't required for any asset type by default. When approval isn't required for a type, an AI asset manager can still request AI steward approval for an individual asset.

## Automatic approval requests

When automatic approval requests are on, approval playbooks are triggered automatically for AI assets, so no one has to request approval. When they're off, which is the default, AI asset managers must request approval for each asset. For more information about the playbooks that run these approvals, see [AI Control Tower playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-playbooks-reference.md).

-   **[Require AI steward approval for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-ai-steward-approval.md)**  
Make sure every AI system, MCP server, or AI model is reviewed before deployment by requiring AI steward approval for that asset type and starting approval requests automatically.

**Parent Topic:**[Configuring ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-servicenow-ai-settings.md)

