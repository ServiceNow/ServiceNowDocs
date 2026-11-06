---
title: Turn off local MCP servers
description: Turn off local MCP servers for users or user groups so that Arc can't run MCP server actions directly on user devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/turn-off-local-mcp-servers.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [local MCP servers, MCP servers, capability overrides]
breadcrumb: [Reference, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Turn off local MCP servers

Turn off local MCP servers for users or user groups so that Arc can't run MCP server actions directly on user devices.

## Before you begin

Role required: sn\_app\_arc.admin

## About this task

Users can connect local MCP servers that run on their own device rather than through a remote server URL. A local MCP server runs outside the Arc sandbox. After a user connects one, it performs actions on the device without requiring approval for each one, and its configuration persists when Arc restarts.

Administrators control whether users can connect local MCP servers.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Arc** &gt; **Policies** &gt; **Arc Agent Policy**.

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

**Parent Topic:**[ServiceNow Arc reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-reference.md)

