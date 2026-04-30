---
title: Application scope
description: Application scoping protects applications by identifying and restricting access to application files and data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application scope

Application scoping protects applications by identifying and restricting access to application files and data.

Administrators can specify what parts of an application are accessible to other applications from:

-   The Custom application record
-   Each application Table record

For example, suppose that you create a conference room booking application in its own application scope. By default, the application can access and change its own tables and business logic but other applications can't unless you give them explicit permission. The application scope ensures:

-   The conference room booking application does not interrupt core business services.
-   Other applications do not interfere with its normal functioning.

By default, all custom applications have a private scope that uniquely identifies them and their associated artifacts with a namespace identifier. The application scope prevents naming conflicts and allows the contextual development environment to determine what changes, if any, are permitted. Application developers specify an application scope when they create an application.

**Tip:** Global apps can alter data that you don't intend to alter. You should leverage scoped apps to create new tables, and consider transitioning old ones to scoped apps. This allows you to split responsibilities with Delegated Development. To learn more about delegated development, see [Exploring Delegated Development](c_DelegatedDevelopment.md).

Selecting the **Can Edit Application in Studio** option does not affect any custom or global applications in development on an instance. If you are the owner and choose to publish the application, you can restrict the development of customizations in Studio of. If you set **Can Edit Application in Studio** to false and then publish it, those who download the application to their own instances won't be able to edit the application in Studio. But they will have access to [Legacy - Source Control integration](c_SourceControlIntegration.md) features inside of Studio.

![Create custom application.](../image/application-scope-image.png)

**Related topics**  


[Runtime access to applications tables](c_RuntimeAccessToAppTables.md#)

