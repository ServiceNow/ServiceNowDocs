---
title: Configure roles for the Service Mapping MCP tools
description: Assign the required roles to users so they can connect to the CMDB MCP Server and call the Service Mapping MCP tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.html
release: brazil
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [MCP Server, Service Mapping, role hierarchy, sn\_sm\_gen\_ai.sm\_mcp\_user, service\_mapping\_user, access control, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI in Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure roles for the Service Mapping MCP tools

Assign the required roles to users so they can connect to the CMDB MCP Server and call the Service Mapping MCP tools.

## Before you begin

Before assigning roles, confirm the following requirements are met.

-   You have the latest version of MCP Platform Manager plugin activated.
-   You have the CMDB MCP Server \[sn\_cmdb\_mcp\_server\], version 1.1.1, application installed.

Role required: admin

## About this task

For information about the Service Mapping tools, see [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md).

The sn\_sm\_gen\_ai.sm\_mcp\_user role grants access to all six Service Mapping MCP tools, including the create\_top\_down\_application\_service write tool.

sn\_sm\_gen\_ai.sm\_mcp\_user automatically includes service\_mapping\_user and the MCP platform role sn\_mcp\_server.viewer. No manual role containment configuration is needed.

**Note:** If you configured role containment manually in a previous release, no action is needed. The shipped containment does not conflict with existing records.

The following table describes the roles involved and the access each one grants.

|Role|Type|Granted rights|
|----|----|--------------|
|sn\_sm\_gen\_ai.sm\_mcp\_admin|MCP admin role|Contains sn\_sm\_gen\_ai.sm\_mcp\_user and service\_mapping\_admin. Grants no access to the Service Mapping MCP tools beyond what sn\_sm\_gen\_ai.sm\_mcp\_user already grants; service\_mapping\_admin covers general Service Mapping administration, unrelated to the MCP tools.|
|sn\_sm\_gen\_ai.sm\_mcp\_user|MCP access role|Access to all six Service Mapping MCP tools, including create\_top\_down\_application\_service, enforced by the REST endpoint ACL. Contains service\_mapping\_user and sn\_mcp\_server.viewer.|
|service\_mapping\_admin|Standard Service Mapping role|Administrative access to Service Mapping configuration. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_admin.|
|service\_mapping\_user|Standard Service Mapping role|Read access to application service maps and topology data. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_user.|
|sn\_mcp\_server.viewer|MCP platform role|Grants the ability to discover and invoke tools on an MCP server. Included automatically under sn\_sm\_gen\_ai.sm\_mcp\_user.|

\[Omitted image "sm-mcp-roles-sep26.png"\] Alt text: sn\_sm\_gen\_ai.sm\_mcp\_admin contains sn\_sm\_gen\_ai.sm\_mcp\_user and service\_mapping\_admin. sn\_sm\_gen\_ai.sm\_mcp\_user contains service\_mapping\_user and sn\_mcp\_server.viewer.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and open the record of a user who needs access to the Service Mapping MCP tools.

2.  Scroll to the **Roles** related list and select **Edit**.

3.  Add the **sn\_sm\_gen\_ai.sm\_mcp\_user** role.

    This role grants access to all six Service Mapping MCP tools, including create\_top\_down\_application\_service. It automatically includes service\_mapping\_user and the MCP platform role sn\_mcp\_server.viewer; no additional roles need to be assigned.

4.  Select **Save**.


## Result

The user is assigned the sn\_sm\_gen\_ai.sm\_mcp\_user role and can call all six Service Mapping MCP tools, including create\_top\_down\_application\_service. The role automatically includes service\_mapping\_user and the MCP platform role sn\_mcp\_server.viewer.

## What to do next

[Activate the CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/activate-sm-mcp-server.md)

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

