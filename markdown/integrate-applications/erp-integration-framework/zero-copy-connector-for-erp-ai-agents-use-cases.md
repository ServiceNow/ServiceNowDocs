---
title: Use Now Assist for Zero Copy Connector agentic workflows
description: Use Zero Copy Connector for ERP generative AI and agentic workflows to improve and enhance working with ERP data.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI, zero copy connector, erp]
breadcrumb: [Now Assist for Zero Copy Connector, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Use Now Assist for Zero Copy Connector agentic workflows

Use Zero Copy Connector for ERP generative AI and agentic workflows to improve and enhance working with ERP data.

Zero Copy Connector for ERP agentic workflows and AI agents are available starting with the Zurich Patch 4 release.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative and agentic AI in Now Assist for Zero Copy Connector.

<table id="table_cxs_mpl_vfc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Explore ERP models

</td><td>

Answers questions about working with ERP database tables and models configured in the ERP Data Product Application.

</td><td>

1.  ERP action invoker AI agent
2.  ERP data fetcher AI agent
3.  ERP output formatter AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

## Role masking

Required role: sn\_erp\_integration.erp\_admin.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

