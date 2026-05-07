---
title: Supported APIs
description: APIs supported in this version of the ServiceNow MCP Registry application are listed here.Retrieves a paginated list of registered MCP servers.Retrieve all available versions for a specific MCP server.Retrieve detailed configuration for a specific MCP server version, including complete package definitions, transport configurations, and metadata.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-02-13"
reading_time_minutes: 2
breadcrumb: [ServiceNow MCP Registry, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Supported APIs

APIs supported in this version of the ServiceNow MCP Registry application are listed here.

## Get MCP Servers

Retrieves a paginated list of registered MCP servers.

The ServiceNow MCP Registry provides HTTP API endpoints for discovering and retrieving MCP server metadata. The list servers endpoint is the primary discovery interface for browsing the registry catalog.

### Endpoint

HTTP Method: `GET`

Route: `/api/sn_mcp_registry/v1/servicenow_mcp_registry/servers`

### Sample response

```
{
  "result": {
    "metadata": {
      "count": 8,
      "nextCursor": null
    },
    "servers": [
      {
        "_meta": {
          "io.modelcontextprotocol.registry/official": {
            "isLatest": true,
            "active": "active",
            "type": "servicenow",
            "updatedAt": "2026-02-15 18:10:04",
            "publishedAt": "2026-02-15 18:08:28"
          }
        },
        "server": {
          "title": "Figma",
          "description": "Design and collaboration platform",
          "name": "com.figma.mcp@mcp-server-remote",
          "version": "latest",
          "repository": {
            "url": "https://github.com/figma/mcp-server-guide",
            "source": "github"
          },
          "remotes": [
            {
              "type": "streamable-http",
              "url": "https://mcp.figma.com/mcp"
            }
          ]
        }
      },
      {
        "_meta": {
          "io.modelcontextprotocol.registry/official": {
            "isLatest": true,
            "active": "active",
            "type": "servicenow",
            "updatedAt": "2026-02-15 18:06:59",
            "publishedAt": "2026-02-15 18:06:59"
          }
        },
        "server": {
          "title": "Linear",
          "description": "Issue tracking and project management",
          "name": "com.linear.app@mcp-server-remote",
          "version": "latest",
          "repository": {
            "url": "https://github.com/jerhadf/linear-mcp-server",
            "source": "github"
          },
          "packages": [
            {
              "registryType": "npm",
              "identifier": "linear-mcp-server",
              "transport": {
                "type": "stdio"
              },
              "environmentVariables": [
                {
                  "name": "LINEAR_API_KEY",
                  "description": "Linear Personal API key from Settings > Account > Security & Access",
                  "isRequired": true,
                  "isSecret": true
                }
              ]
            }
          ],
          "remotes": [
            {
              "type": "sse",
              "url": "https://mcp.linear.app/sse"
            },
            {
              "type": "streamable-http",
              "url": "https://mcp.linear.app/mcp"
            }
          ]
        }
      }
    ]
  }
}

```

## Get all versions of an MCP server

Retrieve all available versions for a specific MCP server.

The list server versions endpoint retrieves all available versions for a specific MCP server.

### Endpoint

HTTP Method: `GET`

Route: `/api/sn_mcp_registry/v1/servicenow_mcp_registry/servers/{mcp_server_name}/versions`

### Path parameters

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|mcp\_server\_name|String|Yes|url encoded name of the mcp server. For example, `com.figma.mcp@mcp-server-remote`.|

### Sample response

```
{
  "result": {
    "serverName": "com.linear.app@mcp-server-remote",
    "totalVersions": 1,
    "versions": [
      {
        "version": "latest",
        "isLatest": true,
        "active": "1",
        "type": "servicenow",
        "description": "Issue tracking and project management",
        "publishedAt": "2026-02-15 18:06:59",
        "updatedAt": "2026-02-15 18:06:59",
        "websiteUrl": "",
        "sysId": "7df5ef86ffcb3210a476ffffffffff45",
        "repository": {
          "url": "https://github.com/jerhadf/linear-mcp-server",
          "source": "github"
        },
        "package": [
          {
            "registryType": "npm",
            "identifier": "linear-mcp-server",
            "transport": {
              "type": "stdio"
            },
            "environmentVariables": [
              {
                "name": "LINEAR_API_KEY",
                "description": "Linear Personal API key from Settings > Account > Security & Access",
                "isRequired": true,
                "isSecret": true
              }
            ]
          }
        ]
      }
    ]
  }
}

```

## Get specific MCP server version

Retrieve detailed configuration for a specific MCP server version, including complete package definitions, transport configurations, and metadata.

The endpoint retrieves detailed configuration for a specific MCP server version. This endpoint returns complete server metadata including package definitions, transport configurations, authentication requirements, and registry-managed metadata. Use the special version `latest` to get the latest version.

### Endpoint

HTTP Method: `GET`

Route: `/api/sn_mcp_registry/v1/servicenow_mcp_registry/servers/{serverName}/versions/{version}`

### Path parameters

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|serverName|String|Yes|URL-encoded server name. For example, `com.figma.mcp@mcp-server-remote`.|
|version|String|Yes|URL-encoded version string. For example, `1.0.0`. Use `latest` to retrieve the latest version.|

### Sample response

```
{
  "result": {
    "server": {
      "name": "com.linear.app@mcp-server-remote",
      "title": "Linear",
      "description": "Issue tracking and project management",
      "version": "latest",
      "remotes": [
        {
          "type": "sse",
          "url": "https://mcp.linear.app/sse"
        },
        {
          "type": "streamable-http",
          "url": "https://mcp.linear.app/mcp"
        }
      ],
      "packages": [
        {
          "registryType": "npm",
          "identifier": "linear-mcp-server",
          "transport": {
            "type": "stdio"
          },
          "environmentVariables": [
            {
              "name": "LINEAR_API_KEY",
              "description": "Linear Personal API key from Settings > Account > Security & Access",
              "isRequired": true,
              "isSecret": true
            }
          ]
        }
      ],
      "icons": null,
      "repository": {
        "url": "https://github.com/jerhadf/linear-mcp-server",
        "source": "github"
      }
    },
    "_meta": {
      "active": "1",
      "publishedAt": "2026-02-15 18:06:59",
      "updatedAt": "2026-02-15 18:06:59",
      "isLatest": false
    }
  }
}

```

