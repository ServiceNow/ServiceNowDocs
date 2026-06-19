---
title: Roles and access in app development tools
description: Access to ServiceNow Studio, Creator Studio, and ServiceNow IDE is controlled by the roles and permissions your admin assigns. Update role assignments when you need to change which tools a user can access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/working-with-roles-and-access.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing access to ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Roles and access in app development tools

Access to ServiceNow Studio, Creator Studio, and ServiceNow IDE is controlled by the roles and permissions your admin assigns. Update role assignments when you need to change which tools a user can access.

Each development tool available through the experience switcher has specific role requirements. To access all development tools, you need the roles required for each tool individually. For example, the delegated\_developer role provides access to ServiceNow Studio, but without the admin and sn\_creatorstudio.user or sn\_creatorstudio.restricted\_user roles, the experience switcher is not visible because you do not have access to the other tools.

**Note:** If you expect to see the experience switcher but do not see it, contact your admin. Custom configurations may affect which experiences are visible.

|Experience|Available for|NOT available for|
|----------|-------------|-----------------|
|Pro-coding experience in ServiceNow IDE|admin|sn\_creatorstudio.restricted\_user, sn\_creatorstudio.user|
|Platform developer coding experience in ServiceNow Studio|delegated\_developer, admin, sn\_g\_app\_creator.app\_creator|sn\_creatorstudio.restricted\_user, sn\_creatorstudio.user|
|No-code experience in Creator Studio|delegated\_developer, admin, sn\_creatorstudio.user, sn\_creatorstudio.restricted\_user|Not applicable.|

**Important:** Regardless of your role — including admin and delegated\_developer — if you have a Creator Studio role, you cannot access ServiceNow Studio or ServiceNow IDE.

For more information, see [Creator Studio roles and personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/roles-creator-studio.md), [ServiceNow Studio personas and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-personas-roles.md), and [ServiceNow IDE roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-roles.md).

## What are some role assignment examples?

As an admin, you can assign permissions to use ServiceNow Studio, Creator Studio, and ServiceNow IDE. Some roles provide access to more than one tool:

-   To grant access to ServiceNow Studio and Creator Studio, assign the **delegated\_developer** role. This role provides access to both tools but does not include access to ServiceNow IDE.
-   To restrict users to Creator Studio only, assign the **sn\_creatorstudio.user** or **sn\_creatorstudio.restricted\_user** role. These roles provide access to Creator Studio but not ServiceNow Studio.
-   To grant access to ServiceNow IDE, the user must have admin permissions or other roles specific to ServiceNow IDE. Users with the **delegated\_developer** role cannot access ServiceNow IDE. For more information, see [ServiceNow IDE roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-roles.md).

**Parent Topic:**[Managing access to ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-access-to-servicenow-studio.md)

