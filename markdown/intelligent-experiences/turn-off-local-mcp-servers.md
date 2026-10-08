---
title: Turn off local MCP servers
description: Turn off local MCP servers for users or user groups so that Cowork can't run MCP server actions directly on user devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/turn-off-local-mcp-servers.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [local MCP servers, MCP servers, capability overrides]
breadcrumb: [Reference, ServiceNow Cowork, Enable AI experiences]
---

# Turn off local MCP servers

Turn off local MCP servers for users or user groups so that Cowork can't run MCP server actions directly on user devices.

## Before you begin

Role required: sn\_app\_cowork.admin

## About this task

Users can connect local MCP servers that run on their own device rather than through a remote server URL. A local MCP server runs outside the Cowork sandbox. After a user connects one, performs actions on the device without requiring approval for each one, and its configuration persists when Cowork restarts.

Administrators control whether users can connect local MCP servers.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Cowork** &gt; **Policies** &gt; **Cowork Agent Policy**.

2.  Open the policy assigned to the users or user groups you want to restrict.

3.  Select the **Capability Overrides** tab, and then select **New**.

4.  In the **Policy** field, select the policy you opened.

5.  In the **Capability** field, select the capability.

6.  In the **Override Value** field, enter ``.

7.  In the **Description** field, enter a description of the override.

8.  In the **Domain** field, select the domain.

9.  Confirm that **Active** is selected.

10. Select **Submit**.


## Result

Users covered by the policy can't connect local MCP servers.

**Parent Topic:**[ServiceNow Cowork reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-reference.md)

