---
title: Retail MCP Server roles and data access
description: Access to the Retail MCP Server is controlled at two levels: roles determine who can invoke each tool, and the caller's own record access determines what data each tool returns or changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-mcp-server-access-control.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [Retail MCP Server, roles, ACL, invoke\_from\_ai, data visibility]
breadcrumb: [Retail MCP Server, ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Retail MCP Server roles and data access

Access to the Retail MCP Server is controlled at two levels: roles determine who can invoke each tool, and the caller's own record access determines what data each tool returns or changes.

## Roles that can invoke the tools

The Retail MCP Server creates no roles. Each tool has an access control of type `flow_action` with the `invoke_from_ai` operation, named after the tool. A caller without one of the listed roles is denied, and the tool doesn't run.

|Role|Tools|
|----|-----|
|sn\_retail.associate\_contributor, sn\_retail.associate\_fulfiller|Get my retail store, Get store devices|
|sn\_rtl\_stre\_servcs.contributor|Create store break-fix case, Create store inquiry case, Get my store services cases, Update store services case|

These roles aren't granted, by design:

-   sn\_retail.support\_agent. A support agent assists retail customers and partners rather than working in a store. An administrator can add this role to the access control if needed.
-   Store Services HQ agent roles, such as sn\_rtl\_stre\_servcs.agent and sn\_rtl\_stre\_servcs.breakfix\_agent, and their manager variants. HQ agents work cases in the agent workspace; these tools expose only store-side actions.

## Data visibility

Each tool runs as the calling user and reads and writes data through secure queries, so the platform's existing access controls apply to the caller. A tool returns only the stores, devices, and cases the caller can read in the platform, and a write is refused if the caller can't write the case. The Retail MCP Server adds no record-level access controls of its own. Store and case tools identify the caller from the session, never from an identifier the assistant supplies.

## What the update tool can change

Update store services case is the only tool that changes existing records. It supports these actions, and nothing else:

|Action|Effect|Allowed when the case is|
|------|------|------------------------|
|`get_actions`|None \(read only\)|Any state|
|`comment`|Adds a comment|New, Open, or Awaiting Info|
|`accept_resolution`|Adds a comment and sets the case to Closed|Resolved|
|`reject_resolution`|Adds a comment and sets the case to Open|Resolved|
|`close`|Sets the case to Closed with a resolution code and close notes chosen by the system|New, Open, or Awaiting Info|

Callers can't set the state directly, or the priority, assignee, assignment group, or resolution code. Closed and Cancelled cases reject every action. The rules match the ones the portal and mobile app apply.

**Parent Topic:**[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-overview.md)

**Related topics**  


[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-overview.md)

[Retail MCP Server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-tools.md)

[Respond to resolutions through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/breakfix-respond-resolution.md)

