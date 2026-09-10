---
title: MCPClient - Scoped
description: The MCPClient script include is the entry point for interacting with approved Model Context Protocol \(MCP\) servers. It provides methods for discovering approved servers, listing and inspecting the tools they expose, and invoking those tools.Instantiates an MCPClient object.Returns the list of MCP servers the caller is authorized to access. By default, only servers with an AI Governance approval status of approved are returned.Returns metadata for a single named tool on an approved MCP server.Invokes a named tool on an approved MCP server.Lists all tools exposed by a specified approved MCP server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/MCPClientAPI.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MCPClient- Scoped

The MCPClient script include is the entry point for interacting with approved Model Context Protocol \(MCP\) servers. It provides methods for discovering approved servers, listing and inspecting the tools they expose, and invoking those tools.

This script include requires the MCP Client plugin \(sn\_wdf\_mcp\_client\) and is provided in the `sn_wdf_mcp_client` namespace. The calling user must have the sn\_mcp\_client.admin role.

Before calling this API, complete the required setup:

-   MCP server records must be created in the Model Context Protocol Server \[sn\_mcp\_server\] table, each with a valid connection alias configured for authentication.
-   The AI Governance plugin \(sn\_ai\_governance\) must be installed. MCP servers must go through the [AI Control Tower \(AICT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md) approval workflow and reach an `approved` governance status before calling invokeTool\(\) on the server.

Typical method call order:

1.  getServers\(\) — Get the list of approved MCP servers, and obtain each server's sys\_id.
2.  listTools\(\) — For a given server, list the tools that server exposes.
3.  getToolInfo\(\) — Optional. For a given server and tool, retrieve that tool's full descriptor \(its input schema and annotations\) so calling code knows what arguments to supply.
4.  invokeTool\(\) — Call a named tool on a given server with the arguments its input schema requires.

For more information about tools and MCP schema, see [Model Context Protocol - Tools](https://modelcontextprotocol.io/specification/2025-06-18/server/tools).

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/api-server.md)

## MCPClient - MCPClient\(\)

Instantiates an MCPClient object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates an MCPClient object.

```
var client = new sn_wdf_mcp_client.MCPClient();
```

## MCPClient - getServers\(Object params\)

Returns the list of MCP servers the caller is authorized to access. By default, only servers with an AI Governance approval status of `approved` are returned.

MCP Servers are retrieved from the Model Context Protocol Server \[sn\_mcp\_server\] table.

<table id="table_gsv_par_01a" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

params

</td><td>

Object

</td><td>

Optional. Query options. Default: `{}` \(default values used for all child properties\)

```
{ 
   limit: Number,
   offset: Number,
   status: "String"
}
```

</td></tr><tr><td>

params.limit

</td><td>

Number

</td><td>

Optional. Maximum number of servers to return.Default: 50

Minimum: 1

Maximum: 200

</td></tr><tr><td>

params.offset

</td><td>

Number

</td><td>

Optional. Number of servers to skip before returning results. Used for pagination.Default: 0

</td></tr><tr><td>

params.status

</td><td>

String

</td><td>

Optional. Filters results by AI Governance approval status. Valid values:

-   `approved`: Returns approved MCP servers.
-   `pending`: Returns MCP servers that are awaiting review or that aren't approved for any reason with an associated error.

Default: `approved`

</td></tr></tbody>
</table><table id="table_gsv_ret_01a" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing the list of MCP servers and metadata.```
{
   "result": {
      "meta": {Object},
      "servers": [Array]
   }
}
```

</td></tr><tr><td>

&lt;Object&gt;.result.meta

</td><td>

Result metadata.Data type: Object

```
"meta": {
   "limit": "Number", 
   "offset": "Number",
   "total": "Number"
}
```

</td></tr><tr><td>

&lt;Object&gt;.result.meta.limit

</td><td>

Maximum number of servers that could be returned in this response.Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.result.meta.offset

</td><td>

Number of servers skipped before returning results. Used for pagination.Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.result.meta.total

</td><td>

Total count of matching servers, independent of pagination.Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.result.servers

</td><td>

Array of MCP server objects.Data type: Array

```
"servers": [
   {
      "governance": {Object},
      "name": "String",
      "server_id": "String",
      "transport": "String"     
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.result.servers.governance

</td><td>

AI Governance approval status.Possible values for **aict\_status** are `approved` and `pending`.

Data type: Object

```
"governance": { "aict_status": "String" }
```

</td></tr><tr><td>

&lt;Object&gt;.result.servers.name

</td><td>

Name of the MCP server.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.servers.server\_id

</td><td>

Sys\_id of the MCP server.Table: Model Context Protocol Server \[sn\_mcp\_server\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.servers.transport

</td><td>

Communication method. The only possible value is `SSE`.Data type: String

</td></tr></tbody>
</table>This example fetches the first two approved MCP servers.

```
var client = new sn_wdf_mcp_client.MCPClient();

var result = client.getServers({ limit: 2, offset: 0 });

gs.info('Total approved servers: ' + result.meta.total);
result.servers.forEach(function(server) {
    gs.info('Server: ' + server.name + ' (' + server.server_id + ')');
});
```

Output:

```
Total approved servers: 60
Server: Atlassian Rovo (08eac8952b3dc7109fadf2a4ce91bf4a)
Server: Atlassian Rovo (135a815d2be9cf109fadf2a4ce91bf13)
```

## MCPClient - getToolInfo\(String serverId, String toolName\)

Returns metadata for a single named tool on an approved MCP server.

<table id="table_gti_par_03a" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

serverId

</td><td>

String

</td><td>

Sys\_id of the MCP server. This parameter only accepts servers that have an AI Governance approval status of `approved`.Table: Model Context Protocol Server \[sn\_mcp\_server\]

</td></tr><tr><td>

toolName

</td><td>

String

</td><td>

Name of the tool. Case sensitive.To view tool names, call [listTools\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/MCPClientAPI.md).

</td></tr></tbody>
</table><table id="table_gti_ret_03a" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

```
// Success result object
{
  "status": "String",
  "tool": {Object}
}

// Error result object
{
  "status": "String",
  "errorMessage": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the method call.Possible values:

-   success
-   error

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.tool

</td><td>

Tool metadata.Data type: Object

```
"tool": {
   "annotations": {Object},
   "description": "String",
   "inputSchema": {Object},
   "name": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.tool.annotations

</td><td>

Annotations.Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.tool.description

</td><td>

Description of the tool.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.tool.inputSchema

</td><td>

Input schema for the tool.Data type: Object

```
"inputSchema": {  
   "properties": {Object},
   "required": [Array],
   "type": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.tool.inputSchema.properties

</td><td>

Properties used in the schema.Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.tool.inputSchema.required

</td><td>

List of properties that are required.Data type: Array

```
"required": ["String"]
```

</td></tr><tr><td>

&lt;Object&gt;.tool.inputSchema.type

</td><td>

Schema type.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.tool.name

</td><td>

Name of the tool.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errorMessage

</td><td>

Returned only on failure. Possible errors: the server is invalid, the tool name is missing, or the tool is not found.Data type: String

</td></tr></tbody>
</table>This example retrieves metadata for a single tool.

```
var client = new sn_wdf_mcp_client.MCPClient();
var serverId = 'a1b2c3d4e5f6a1b2c3d4e5f6';

var info = client.getToolInfo(serverId, 'addTeamworkGraphContext');

if (info.status === 'success') {
    gs.info('Found tool: ' + info.tool.name);
    gs.info('Description: ' + info.tool.description);
} else {
    gs.warn(info.errorMessage);
}
```

Output:

```
Found tool: addTeamworkGraphContext
Description: Adds a relationship between two entities in the Teamwork Graph (e.g. linking two Jira work items, marking one as blocking another).
```

## MCPClient - invokeTool\(String serverId, String toolName, Object toolArguments\)

Invokes a named tool on an approved MCP server.

<table id="table_ivt_par_04a" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

serverId

</td><td>

String

</td><td>

Sys\_id of the MCP server. This parameter only accepts servers that have an AI Governance approval status of `approved`.Table: Model Context Protocol Server \[sn\_mcp\_server\]

</td></tr><tr><td>

toolName

</td><td>

String

</td><td>

Name of the tool. Case sensitive.Table:

Field: Name

</td></tr><tr><td>

toolArguments

</td><td>

Object

</td><td>

Optional. Arguments object passed through to the tool. Shape is tool-specific and defined by the target tool's input schema, for example `{ "inputs": { "toolArguments": {} } }`.

</td></tr></tbody>
</table><table id="table_ivt_ret_04a" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing the payload from invoking the tool.```
// Success result object
{
  "status": "String",
  "server_id": "String",
  "tool_name": "String",
  "result": {Object}
}

// Error result object
{
  "status": "String",
  "errorMessage": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the method call.Possible values:

-   success
-   error

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.server\_id

</td><td>

Sys\_id of the MCP server.Table: Model Context Protocol Server \[sn\_mcp\_server\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.tool\_name

</td><td>

Name of the tool.Table:

Field: Name

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result

</td><td>

Payload returned after invoking the tool. Shape is tool-specific.Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.errorMessage

</td><td>

Returned only on failure. Error message.Data type: String

</td></tr></tbody>
</table>This example invokes the `create_issue` tool on an approved MCP server.

```
var client = new sn_wdf_mcp_client.MCPClient();
var serverId = 'a1b2c3d4e5f6a1b2c3d4e5f6';

var response = client.invokeTool(serverId, 'create_issue', {
    "inputs": {
        "toolArguments": {
            "issue_title": "New issue for MCP"
        }
    }
});

if (response.status === 'success') {
    gs.info('Tool ' + response.tool_name + ' invoked on ' + response.server_id);
    gs.info('Result: ' + JSON.stringify(response.result));
} else {
    gs.error('Invocation failed: ' + response.errorMessage);
}
```

Output:

```
Tool create_issue invoked on a1b2c3d4e5f6a1b2c3d4e5f6
Result: {"issue_number":42,"url":"https://..."}
```

## MCPClient - listTools\(String serverId, String cursor\)

Lists all tools exposed by a specified approved MCP server.

<table id="table_lst_par_02a" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

serverId

</td><td>

String

</td><td>

Sys\_id of the MCP server. This parameter only accepts servers that have an AI Governance approval status of `approved`.Table: Model Context Protocol Server \[sn\_mcp\_server\]

</td></tr><tr><td>

cursor

</td><td>

String

</td><td>

Optional. Pagination cursor to start from. Get this value from **next\_cursor** in the previous result.Default: Starts from the first page.

</td></tr></tbody>
</table><table id="table_lst_ret_02a" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Result object containing the list of tools and the next page cursor.```
// Success result object
{
  "result": {
    "next_cursor": "String,
    "tools": [Array]
  }
}

// Error result object
{
  "result": {
    "errorMessage": "String", 
    "status": "String" 
  }
}
```

</td></tr><tr><td>

&lt;Object&gt;.result.nextCursor

</td><td>

Pagination cursor to use in the next method call.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.tools

</td><td>

Array of tool objects.Data type: Array

```
"tools": [
   {
      "description": "String",
      "inputSchema": {Object},
      "name": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.result.tools.description

</td><td>

Description of the tool.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.tools.inputSchema

</td><td>

Input schema for the tool.Data type: Object

```
"inputSchema": {  
   "properties": {Object},
   "required": [Array],
   "type": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.result.tools.inputSchema.properties

</td><td>

Properties used in the schema.Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.result.tools.inputSchema.required

</td><td>

List of properties that are required.Data type: Array

```
"required": ["String"]
```

</td></tr><tr><td>

&lt;Object&gt;.result.tools.inputSchema.type

</td><td>

Schema type.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.tools.name

</td><td>

Name of the tool.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.errorMessage

</td><td>

Returned only on failure. Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.result.status

</td><td>

Returned only on failure. The only possible value is `error`.Data type: String

</td></tr></tbody>
</table>This example lists the tools exposed by an approved MCP server.

```
var client = new sn_wdf_mcp_client.MCPClient(); 
var serverId = '08eac8952b3dc7109fadf2a4ce91bf4a'; // sys_id of an approved MCP server 

var result = client.listTools(serverId); 

if (result.status === 'error') { 
   gs.error('Could not list tools: ' + result.errorMessage); 
} else { 
   gs.info(JSON.stringify(result));
} 
```

Output:

```
{
  "result": {
    "tools": [
      {
        "name": "addTeamworkGraphContext",
        "description": "Adds a relationship between two entities in the Teamwork Graph (e.g. linking two Jira work items).",
        "inputSchema": {
          "type": "object",
          "properties": {
            "cloudId": {
              "type": "string",
              "description": "Cloud ID"
            },
            "relationshipType": {
              "type": "string",
              "enum": []
            },
            "objectIdentifier": {
              "type": "string",
              "maxLength": 500
            },
            "targetObjectIdentifier": {
              "type": "string",
              "maxLength": 500
            }
          },
          "required": [
            "cloudId",
            "relationshipType",
            "objectIdentifier",
            "targetObjectIdentifier"
          ]
        }
      }
    ],
    "next_cursor": null
  }
}
```

