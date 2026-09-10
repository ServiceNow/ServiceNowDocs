---
title: Working with MCP server records
description: The MCP servers tab on the AI Control Tower Inventory page provides a centralized view of MCP servers registered in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/working-with-mcp-server-records.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 1
breadcrumb: [Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Working with MCP server records

The MCP servers tab on the AI Control Tower Inventory page provides a centralized view of MCP servers registered in your ServiceNow instance.

MCP servers are AI assets that expose tools, resources, and capabilities to AI agents through a standardized protocol. Registering MCP servers in the inventory enables AI Control Tower to govern, classify, and monitor their usage alongside other AI assets. The **MCP servers** tab displays only assets of type MCP server.

## MCP servers inventory list

The MCP servers inventory list displays the following columns for each registered server:

|Column|Description|
|------|-----------|
|Display name|The display name of the MCP server. Servers sourced from external registries may display their registry path as the display name, for example: io.github.pipeworx-io/dictionary.|
|Asset type|Always MCP server for entries on this tab.|
|State|The lifecycle stage of the MCP server. Common values include Deployed. See MCP server States for the full list.|
|Status|The approval status of the MCP server. Possible values are Approved and empty \(not yet reviewed\). See MCP server Statuses for details.|
|Managed status|Indicates whether the MCP server is under active governance. Possible values are Managed and Unmanaged.|
|Risk classification|The assessed risk level of the MCP server. The default value is To be determined until a risk assessment is completed.|
|Updated|The date and time the record was last modified.|

## Refine results panel

Use the Refine results panel to filter the MCP servers list by one or more criteria simultaneously.

The following filter groups are available in the Refine results panel:

|Filter group|Available values|
|------------|----------------|
|Managed status|Managed, Unmanaged|
|Risk classification|Critical, Unacceptable, High, Medium, Low \(select Show all for additional values\).|
|State|Ideation, Design, Build, Available, Deployed \(select Show all for additional values\).|
|Status|In review, Ready for deployment \(scroll or select Show all for additional values\).|

