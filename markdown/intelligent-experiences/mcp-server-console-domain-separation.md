---
title: Domain separation and MCP Server Console
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.Domain separation is supported for MCP Server Console. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mcp-server-console-domain-separation.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, MCP Server Console, Enable AI experiences]
---

# Domain separation and MCP Server Console

Domain separation is supported for MCP Server Console. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## How domain separation works in MCP Server Console

Domain separation limits the MCP tools and servers that a user can access based on their current domain. The rules follow a top-down hierarchy: a domain can view its own records, all records from descendant domains, and global records. The domain can't access records from ancestor or sibling domains.

-   To enable domain separation in your MCP instance, install the domain separation plugin.
-   The parent domain can view the servers, tools, and apps created within its child domains, and those created within its own domain.

    **Note:** A domain can view it's own records, descendent domain's and global records. But it can't view ancestor's and sibling domain records.

-   An MCP tool can be attached to a server within the same domain.
-   When a tool or server is created via the UI, it is stamped with the creating user's current `sys_domain`. This stamp is the source of truth for all visibility and scoping decisions.

**Parent Topic:**[MCP Server Console reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mcp-server-console-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

