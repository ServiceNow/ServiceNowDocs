---
title: Use Now Assist for Zero Copy Connector agentic workflows
description: Use Now Assist for Zero Copy Connector generative AI and agentic workflows to improve and enhance working with ERP data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Use Now Assist for Zero Copy Connector agentic workflows

Use Now Assist for Zero Copy Connector generative AI and agentic workflows to improve and enhance working with ERP data.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative and agentic AI in Now Assist for ZCC.

<table id="table_cxs_mpl_vfc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Explore ERP models

</td><td>

Answers questions about working with configured ERP database tables and models.

</td><td>

1.  ERP action invoker AI agent
2.  ERP data fetcher AI agent
3.  ERP output formatter AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Role masking

Required role: sn\_erp\_integration.erp\_admin.

AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

