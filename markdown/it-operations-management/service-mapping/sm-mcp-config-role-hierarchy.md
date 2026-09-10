---
title: Configure roles for the Service Mapping MCP tools
description: Assign the required roles to users so they can connect to the CMDB MCP Server and call the Service Mapping MCP tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [MCP Server, Service Mapping, role hierarchy, sn\_sm\_gen\_ai.sm\_mcp\_user, service\_mapping\_user, access control, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI in Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure roles for the Service Mapping MCP tools

Assign the required roles to users so they can connect to the CMDB MCP Server and call the Service Mapping MCP tools.

## Before you begin

Before assigning roles, confirm the following requirements are met.

-   You have the latest version of the MCP Platform Manager plugin activated.
-   You have at least version 1.1.1 of the CMDB MCP Server \[sn\_cmdb\_mcp\_server\] application installed.

Role required: admin

## About this task

For information about the Service Mapping tools, see [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md).

The Service Mapping MCP tools use a two-tier role model for access control. The sn\_sm\_gen\_ai.sm\_mcp\_user role grants access to the five read-only query tools. The sn\_sm\_gen\_ai.sm\_mcp\_admin role grants access to all six tools, including the create\_top\_down\_service write tool.

Both roles ship with the required platform roles already included. No manual role containment configuration is needed. Assign sn\_sm\_gen\_ai.sm\_mcp\_user for read-only access and sn\_sm\_gen\_ai.sm\_mcp\_admin for write access.

**Note:** If you configured role containment manually in a previous release, no action is needed. The shipped containment does not conflict with existing records.

The following table describes the roles involved and the access each one grants.

|Role|Type|Granted rights|
|----|----|--------------|
|sn\_sm\_gen\_ai.sm\_mcp\_admin|MCP admin role|Access to all six Service Mapping MCP tools, including the create\_top\_down\_service write tool. Contains sn\_sm\_gen\_ai.sm\_mcp\_user and service\_mapping\_admin.|
|sn\_sm\_gen\_ai.sm\_mcp\_user|MCP access role|Access to the five read-only Service Mapping MCP tools. Enforced by the REST endpoint ACL. Contains service\_mapping\_user and sn\_mcp\_server.viewer.|
|service\_mapping\_admin|Standard Service Mapping role|Administrative access to Service Mapping configuration. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_admin.|
|service\_mapping\_user|Standard Service Mapping role|Read access to application service maps and topology data. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_user.|
|sn\_mcp\_server.viewer|MCP platform role|Grants the ability to discover and invoke tools on an MCP server. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_user.|

\[Omitted image "sm-mcp-roles-sep26.png"\] Alt text: sn\_sm\_gen\_ai.sm\_mcp\_admin contains sn\_sm\_gen\_ai.sm\_mcp\_user and service\_mapping\_admin. sn\_sm\_gen\_ai.sm\_mcp\_user contains service\_mapping\_user and sn\_mcp\_server.viewer.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and open the record of a user who needs access to the Service Mapping MCP tools.

2.  Scroll to the **Roles** related list and select **Edit**.

3.  Add the appropriate role based on the access level the user needs.

    |Access level|Role to assign|
    |------------|--------------|
    |**Read-only \(five query tools\)**|sn\_sm\_gen\_ai.sm\_mcp\_user|
    |**Read and write \(all six tools, including create\_top\_down\_service\)**|sn\_sm\_gen\_ai.sm\_mcp\_admin|

    Each role includes the required platform roles automatically. No additional roles need to be assigned.

4.  Select **Save**.


## Result

The user is assigned the required role. Users with sn\_sm\_gen\_ai.sm\_mcp\_user can call the five read-only tools. Users with sn\_sm\_gen\_ai.sm\_mcp\_admin can also call create\_top\_down\_service. Both roles include the required platform roles automatically.

## What to do next

[Activate the CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-mcp-server.md)

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

