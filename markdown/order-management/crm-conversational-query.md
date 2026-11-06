---
title: CRM conversational query
description: CRM conversational query is an AI agent in ServiceNow Otto that retrieves, updates, and creates CRM records from plain-language requests without opening a form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/crm-conversational-query.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Opportunity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# CRM conversational query

CRM conversational query is an AI agent in ServiceNow Otto that retrieves, updates, and creates CRM records from plain-language requests without opening a form.

You can access the agent in the following ways:

-   ServiceNow Otto panel: from the CRM home page.
-   Model Context Protocol \(MCP\) client \(for example, Claude\): through the Sales CRM MCP server. This server is preconfigured and appears as **Sales CRM** in MCP Server Console. It's installed automatically with the Sales Common plugin when you install a Sales CRM application, such as Opportunity Management or Lead Management. You don't have to create a server or add tools. For information about connecting an MCP client to the server, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md). For information about connecting an MCP client to the Sales CRM MCP server, see .

The agent supports the following operations on opportunity records and related entities, including contacts, tasks, touchpoints, meetings, line items, and competitors:

-   Retrieve: view pipeline snapshots, opportunity details, tasks, touchpoints, contacts, accounts, and opportunity lines.
-   Update: change field values on opportunities and related records. You can update multiple fields in one request and use relative dates, such as "end of next month".
-   Create: add opportunities, contacts, tasks, touchpoints, and competitors.

**Related topics**  


[Manage opportunity records using an AI interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/manage-opportunity-records.md)

[Configuring AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/configuring-ai-capabilities-sales-crm.md)

