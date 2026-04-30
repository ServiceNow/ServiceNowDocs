---
title: Global scope
description: The global scope is a special application scope that identifies applications developed prior to application scoping, or applications intended to be accessible to all other global applications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application scope, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Global scope

The global scope is a special application scope that identifies applications developed prior to application scoping, or applications intended to be accessible to all other global applications.

Applications in the global scope do not append a unique namespace identifier to the application name. Global applications can have naming conflicts and data collisions when developers create multiple global applications with the same name.

Since all global applications are in the same scope, they bypass scope protections. Global applications allow other global applications access to their tables to

-   Read records
-   Run API requests
-   Create configuration records

Typically, only applications provided by ServiceNow are in the global scope. However, any custom applications created before application scope was implemented are also in the global scope. Additionally, developers with the sn\_g\_app\_creator.app\_creator role can create applications in the global scope. For more information, see [Allow global application development in Guided Application Creator](../../guided-app-creator/task/gac-activate-global.md).

Applications in the global scope are eligible for upload to the application repository, but not to the ServiceNow Store.

**Related topics**  


[Publish an application to the application repository](../task/t_PublishAppsToTheAppRepository.md)

[Publish an application to the ServiceNow Store](../task/t_PublishAppsToTheServiceNowStore.md)

