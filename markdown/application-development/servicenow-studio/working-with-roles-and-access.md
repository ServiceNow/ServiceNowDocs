---
title: Working with roles and access in app development tools
description: Access to ServiceNow Studio, Creator Studio, and ServiceNow IDE depends on the roles and permissions your admin sets. However, there are some scenarios in which you might want to update the roles allowed to access each tool.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing access to ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Working with roles and access in app development tools

Access to ServiceNow Studio, Creator Studio, and ServiceNow IDE depends on the roles and permissions your admin sets. However, there are some scenarios in which you might want to update the roles allowed to access each tool.

Each development tool that you can access through the experience switcher has roles that it is available for and not available for. To access every development tool, you need to have the roles required for each tool individually. For example, if you have the delegated\_developer role, you can work in ServiceNow Studio. However, if you don't also have admin and sn\_creatorstudio.user or sn\_creatorstudio.restricted\_user roles, you won't see the experience switcher because you don't have access to the other tools.

**Note:** If you're expecting to see the experience switcher and don't see it, please contact your admin. Custom configurations may affect the experiences you can see.

|Experience|Available for|NOT available for|
|----------|-------------|-----------------|
|Access to the pro-coding experience in ServiceNow IDE|admin|sn\_creatorstudio.restricted\_user, sn\_creatorstudio.user|
|Access to the platform developer coding experience in ServiceNow Studio|delegated\_developer, admin, sn\_g\_app\_creator.app\_creator|sn\_creatorstudio.restricted\_user, sn\_creatorstudio.user|
|Access to the no-code experience in Creator Studio|delegated\_developer, admin, sn\_creatorstudio.user, sn\_creatorstudio.restricted\_user|Not applicable.|

**Important:** No matter what your role is \(including admin and delegated developer roles\), if you have one of the Creator Studio roles, you won't be able to access ServiceNow Studio or ServiceNow IDE.

For more information, see [Creator Studio roles and personas](../../creator-studio/reference/roles-creator-studio.md), [ServiceNow Studio personas and roles](sn-studio-personas-roles.md), and [ServiceNow IDE roles](../../servicenow-ide/reference/servicenow-ide-roles.md#).

## Role assignment examples

As an admin, you can assign permissions to use ServiceNow Studio, Creator Studio, and ServiceNow IDE. Some roles give access to more than one tool and could be used in the following scenarios:

-   If you want to assign access to ServiceNow Studio and Creator Studio, assign your user the **delegated\_developer** role. This will give them access to both tools. However, this role does not give access to ServiceNow IDE.
-   If you want users to stay in Creator Studio, assign them the **sn\_creatorstudio.user** or **sn\_creatorstudio.restricted\_user** roles. These roles give access to Creator Studio but not ServiceNow Studio.
-   If you want to assign access to ServiceNow IDE, your user must have admin permissions or other roles specific to ServiceNow IDE. If your user also has the **delegated\_developer** role, they will not be able to access ServiceNow IDE. For more information, see [ServiceNow IDE roles](../../servicenow-ide/reference/servicenow-ide-roles.md#).

**Parent Topic:**[Managing access to ServiceNow Studio](manage-access-to-servicenow-studio.md)

