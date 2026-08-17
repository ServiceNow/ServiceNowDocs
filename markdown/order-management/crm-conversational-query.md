---
title: CRM conversational query
description: CRM conversational query is an AI agent embedded in ServiceNow Otto. You can ask questions and issue commands in plain language and the agent performs the action without you opening a form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/crm-conversational-query.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 1
breadcrumb: [Opportunity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# CRM conversational query

CRM conversational query is an AI agent embedded in ServiceNow Otto. You can ask questions and issue commands in plain language and the agent performs the action without you opening a form.

The agent is accessible via MCP clients \(such as Claude\) through the Sales CRM MCP server, which is published in Sales common. For information on how to connect to an MCP server from an MCP client, refer [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md).

The agent supports the following operations on opportunity records and related entities, including contacts, tasks, touchpoints, meetings, line items, and competitors:

-   Retrieve: view pipeline snapshots, opportunity details, tasks, touchpoints, contacts, accounts, and opportunity lines.
-   Update: change field values on opportunities and related records. Multi-field updates \(up to five fields in one prompt\) and relative date expressions such as "end of next month" are supported.
-   Create: add opportunities, contacts, tasks, touchpoints, and competitors.
-   Delete: remove junction or child records such as opportunity competitors and associated contacts. Parent records such as the opportunity itself, the contact record, or the product are never deleted.

