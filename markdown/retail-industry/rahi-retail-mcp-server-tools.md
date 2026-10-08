---
title: Retail MCP Server tools
description: The Retail MCP Server provides six tools. Each entry lists the tool's purpose, inputs, what it returns, whether it changes data, and what it requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-mcp-server-tools.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 4
keywords: [Retail MCP Server, MCP tools, get\_my\_store, get\_store\_devices, store services case]
breadcrumb: [Retail MCP Server, ServiceNow Otto for Retail Service Management \(RSM\), Retail]
---

# Retail MCP Server tools

The Retail MCP Server provides six tools. Each entry lists the tool's purpose, inputs, what it returns, whether it changes data, and what it requires.

## Tool summary

|Tool|Changes data|Requires plugin|Invoke role|
|----|------------|---------------|-----------|
|`sn_rtl_mcp_server.get_my_store`|No|Retail Core|sn\_retail.associate\_contributor or sn\_retail.associate\_fulfiller|
|`sn_rtl_mcp_server.get_store_devices`|No|Retail Core|sn\_retail.associate\_contributor or sn\_retail.associate\_fulfiller|
|`sn_rtl_mcp_server.create_store_breakfix_case`|Yes|Retail Store Services|sn\_rtl\_stre\_servcs.contributor|
|`sn_rtl_mcp_server.create_store_inquiry_case`|Yes|Retail Store Services|sn\_rtl\_stre\_servcs.contributor|
|`sn_rtl_mcp_server.get_my_store_services_cases`|No|Retail Store Services|sn\_rtl\_stre\_servcs.contributor|
|`sn_rtl_mcp_server.update_store_services_case`|Yes, except for `get_actions`|Retail Store Services|sn\_rtl\_stre\_servcs.contributor|

## Get my retail store

Returns the stores the signed-in user belongs to. The tool takes no inputs; it identifies the user from the authenticated session. For each store, it returns the store's sys\_id and name. If the user belongs to no store, it returns an empty list with a message, not an error. The tool returns up to 100 stores.

## Get store devices

Returns the active devices \(install base items\) registered to a store, up to 100 devices. Each device is returned with its sys\_id, name, identifier \(the asset tag on the unit\), and model category. Results that match on device name are listed before matches on identifier or product. If the search term matches nothing, the tool returns the store's full device list with a message that the search didn't match.

|Input|Required|Description|
|-----|--------|-----------|
|`store`|Yes|The sys\_id of the store, from Get my retail store.|
|`search_term`|No|Words to narrow a long list. Each word is matched against device name, identifier, number, and product.|

## Create store break-fix case

Creates a break-fix case for a broken or faulty device. The tool description instructs the assistant to confirm every value with the user before creating the case. It returns the case number, sys\_id, short description, state, priority, store, device, and an attachment URL. The user can open the attachment URL in the portal to add photos or files, because files can't be sent through the tool.

|Input|Required|Description|
|-----|--------|-----------|
|`requesting_service_organization`|Yes|The sys\_id of the store, from Get my retail store.|
|`short_description`|Yes|A one-line summary of the fault.|
|`description`|No|Details of the fault.|
|`priority`|No|1 \(Critical\), 2 \(High\), 3 \(Moderate\), or 4 \(Low\).|
|`install_base`|Yes|The sys\_id of the device, from Get store devices.|

## Create store inquiry case

Creates a store inquiry case that asks HQ a question about store policy, process, or operations. It takes no device. It returns the case number, sys\_id, short description, state, priority, store, and an attachment URL.

|Input|Required|Description|
|-----|--------|-----------|
|`requesting_service_organization`|Yes|The sys\_id of the store, from Get my retail store.|
|`short_description`|Yes|A one-line summary of the question.|
|`description`|No|Details and context for the question.|
|`priority`|No|1 \(Critical\), 2 \(High\), 3 \(Moderate\), or 4 \(Low\).|

## Get my store services cases

Lists the break-fix and store inquiry cases the signed-in user raised, most recently updated first, up to 40 cases. Each case is returned with its number, case type, and short description. If no cases match, the tool returns an empty list with a message.

|Input|Required|Description|
|-----|--------|-----------|
|`case_type`|No|breakfix or inquiry. Omit to return both types.|
|`open_only`|No|true \(default\) excludes Closed and Cancelled cases. false includes them.|
|`number`|No|A case number, to return only that case.|
|`search_term`|No|Words matched against case number, short description, and description.|

## Update store services case

Reads or acts on one case the signed-in user raised. Called with the `get_actions` action, it returns the case and the actions allowed in its current state, including HQ's pending question when the case is Awaiting Info and the proposed resolution when the case is Resolved. Every other action changes the case and returns the updated case with a new list of allowed actions. For the actions allowed in each state, see [Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-access-control.md).

|Input|Required|Description|
|-----|--------|-----------|
|`case_type`|Yes|breakfix or inquiry.|
|`number`|Yes|The case number.|
|`action`|Yes|get\_actions, comment, accept\_resolution, reject\_resolution, or close.|
|`comment`|No|The comment text. Required for comment and reject\_resolution.|

**Parent Topic:**[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-overview.md)

**Related topics**  


[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-overview.md)

[Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-mcp-server-access-control.md)

