---
title: Domain separation and Build Agent
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Build Agent. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ba-domain-separation.html
release: zurich
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Domain separation and Build Agent

Domain separation is supported for Build Agent. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

Build Agent creates standard ServiceNow metadata, such as tables, business rules, and access control lists, that participates in domain separation when domain separation is active on the instance. Domain separation is a platform-level feature configured by a ServiceNow AI Platform administrator, not by Build Agent.

Build Agent creates scoped applications with their own namespace. When domain separation is active, the platform manages domain visibility of application data automatically through the `sys_domain` field.

## How domain separation works in Build Agent

Domain separation configuration occurs at two layers.

-   **Instance level**

    A platform administrator activates the Domain Support - Domain Extensions plugin \(com.glide.domain.msp\_extensions\) and configures the domain hierarchy through Domain Admin. The configuration is outside the scope of Build Agent.

-   **Application level**

    Build Agent creates the application metadata that operates within a domain-separated environment. After you install the application, a platform administrator configures domain separation settings for any new tables and assigns roles to the appropriate domains.

-   **ServiceNow Fluent SDK level**

    The ServiceNow Fluent SDK supports setting the `sys_domain` field directly on records and on APIs that support domain separation. You can also read and write `sys_override` fields to apply domain-specific overrides through the ServiceNow SDK. In addition to tables, you can create other metadata objects in specific domains.


Build Agent supports creating the following in a domain-separated environment.

-   Tables that inherit domain separation when they extend a domain-separated parent table
-   Business rules and scripts that run within the domain context of the current session
-   Fluent SDK records and APIs that set the `sys_domain` field and use `sys_override` fields in domain-separated environments

The following general guidelines apply to data model behavior when working with Build Agent:

-   When Build Agent creates a table that extends a base system table with `sys_domain`, for example `task` or `cmdb_ci`, the domain column is automatically inherited. Don't redeclare it.
-   GlideRecord queries in scripts that Build Agent creates are automatically filtered by domain. Queries that must run across domains require elevated privileges configured by a platform administrator.
-   Reference fields that point to a domain-separated table display only records visible in the current domain.

## Roles and responsibilities

The following roles and responsibilities apply when administering domain separation for applications that Build Agent creates.

-   **Instance owner**
    -   Controls which domains can access the application, configures domain-default field values.
    -   Manages domain-specific overrides for business rules.
    -   Determines which business logic applies globally vs. per domain.
-   **Tenant domain administrator**
    -   Creates, updates, and deletes records within their domain and any child domains.
    -   Configures domain-specific values such as categories, assignment groups, and approval workflows.
    -   Can't modify application metadata including business rules, access control lists, or table structure unless the application explicitly permits it.

## Special conditions

Build Agent domain separation support includes the following conditions and exceptions.

-   Build Agent creates application metadata but can't configure domain separation settings directly. A ServiceNow AI Platform administrator must configure domain hierarchy, table participation, and visibility rules on the instance.
-   Flows that Build Agent creates execute in the domain context of the triggering record. Flows that must operate across domains, such as an escalation from a tenant domain to a global domain, require additional design and platform administrator configuration.
-   Metadata created in global scope is visible across all domains by default. Scoped applications provide better domain isolation.
-   When using the Fluent SDK, you can set `sys_domain` on records and APIs that support domain separation. The `sys_override` field is also supported, which lets you apply domain-specific field value overrides through the SDK without modifying the base record.

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/domain-sep-landing-page.md)

