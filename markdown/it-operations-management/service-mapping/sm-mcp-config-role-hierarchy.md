---
title: Configure roles for the Service Mapping MCP tools
description: Configure the role containment chain and assign the required roles to users so they can connect to the Now Assist CMDB MCP Server and call the Service Mapping MCP tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 3
keywords: [MCP Server, Service Mapping, role hierarchy, sn\_sm\_gen\_ai.sm\_mcp\_user, service\_mapping\_user, access control, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure roles for the Service Mapping MCP tools

Configure the role containment chain and assign the required roles to users so they can connect to the Now Assist CMDB MCP Server and call the Service Mapping MCP tools.

## Before you begin

Before activating the Now Assist CMDB MCP Server, confirm the following requirements are met.

-   Verify that Australia Patch 3 is installed.
-   You have the MCP Platform Manager version 1.4.0 \(or later\) plugin activated.
-   You have the Now Assist CMDB MCP Server \(sn\_cmdb\_gen\_ai.now\_assist\_cmdb\_mcp\_server\) application installed.

Role required: admin

## About this task

For information about the Service Mapping tools, see [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md).

The REST API ACL for the Service Mapping MCP tools enforces the sn\_sm\_gen\_ai.sm\_mcp\_user role. This role is not automatically added to the standard Service Mapping role hierarchy after deployment. You must configure the containment records manually, because role hierarchy assignments cannot be included in a scoped update set.

The following table describes the roles involved and the access each one grants.

|Role|Type|Granted rights|
|----|----|--------------|
|service\_mapping\_user|Standard Service Mapping role|Read access to application service maps and topology data. Assigned to end users who query service data via the MCP Server.|
|sn\_sm\_gen\_ai.sm\_mcp\_user|MCP access role|Enforced by the REST API ACL on all five Service Mapping MCP tools. Users must have this role \(directly or via containment\) to call the tools.|
|sn\_mcp\_server.viewer|MCP platform role|Grants the ability to discover and invoke tools on an MCP server. Required by sn\_sm\_gen\_ai.sm\_mcp\_user.|
|sn\_sm\_gen\_ai.sm\_mcp\_admin|MCP admin role|Grants elevated access for administering the Service Mapping MCP tools.|

\[Omitted image "sm-mcp-roles.png"\] Alt text: service\_mapping\_user contains sn\_sm\_gen\_ai.sm\_mcp\_user, which contains sn\_mcp\_server.viewer. The sn\_sm\_gen\_ai.sm\_mcp\_admin role separately contains sn\_sm\_gen\_ai.sm\_mcp\_user.

## Procedure

1.  Configure the role containment chain.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Roles** and open the **service\_mapping\_user** role record.

    2.  In the **Contains Roles** related list, add **sn\_sm\_gen\_ai.sm\_mcp\_user**.

        The service\_mapping\_user role contains the sn\_sm\_gen\_ai.sm\_mcp\_user role.

    3.  Open the **sn\_sm\_gen\_ai.sm\_mcp\_user** role record.

    4.  In the **Contains Roles** related list, add **sn\_mcp\_server.viewer**.

        Users with the sn\_sm\_gen\_ai.sm\_mcp\_user role can discover and invoke tools on the Now Assist CMDB MCP Server.

    5.  Open the **sn\_sm\_gen\_ai.sm\_mcp\_admin** role record.

    6.  In the **Contains Roles** related list, verify that **sn\_sm\_gen\_ai.sm\_mcp\_user** is present.

        If the role is not present, add it. This ensures that users with the admin role can also call the tools.

2.  Assign the required roles to each end user who needs to query application service data through Claude Desktop.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and open the record of a user who needs access to the Service Mapping MCP tools.

    2.  Scroll to the **Roles** related list and select **Edit**.

    3.  Add the **service\_mapping\_user** role.

        This role inherits sn\_sm\_gen\_ai.sm\_mcp\_user and sn\_mcp\_server.viewer through the containment chain you configured in the previous step. All three roles are required for end-to-end tool invocation.

    4.  Select **Save**.


## Result

The role hierarchy is configured and users are assigned the required roles. Users assigned the service\_mapping\_user role can connect an MCP-compatible AI client and call all five Service Mapping MCP tools. Users assigned sn\_sm\_gen\_ai.sm\_mcp\_admin retain the same tool access plus elevated administrative rights.

## What to do next

[Activate the Now Assist CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-mcp-server.md)

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

