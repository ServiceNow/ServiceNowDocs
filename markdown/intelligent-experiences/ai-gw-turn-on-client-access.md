---
title: Turn on client access control for your instance
description: Set a system property so that AI stewards can turn on access management and create client access policies for MCP servers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-turn-on-client-access.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [client access control, access management, system property]
breadcrumb: [Control client access, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Turn on client access control for your instance

Set a system property so that AI stewards can turn on access management and create client access policies for MCP servers.

## Before you begin

Role required: aig\_admin

## About this task

Client access control is off by default. While it's off, the **Access management** policy category doesn't appear on MCP server records, and AI Gateway doesn't limit clients to specific tools on any MCP server.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Search for and open the **sn\_awh\_config.gateway\_access\_control\_enabled** property.

3.  In the **Value** field, enter `true`.

4.  Select **Update**.


## Result

The **Access management** policy category appears on the **Policies** sub-tab of each MCP server's **AI Gateway** tab. Access management stays off for each server until an AI steward turns it on.

**Important:** If you later set the property to `false`, access management is turned off for all MCP servers connected through AI Gateway, and clients can use any active tool again. Setting the property back to `true` doesn't turn access management back on. An AI steward must turn it on again for each server.

## What to do next

To start limiting clients on an MCP server, see [Create a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-create-client-access-policy.md) and [Turn access management on or off for an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-access-management.md).

