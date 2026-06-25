---
title: Application scope
description: Application scoping protects applications by identifying and restricting access to application files and data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/c\_ApplicationScope.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
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

**Tip:** Global apps can alter data that you don't intend to alter. You should leverage scoped apps to create new tables, and consider transitioning old ones to scoped apps. This allows you to split responsibilities with Delegated Development. To learn more about delegated development, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

**Related topics**  


[Runtime access to applications tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_RuntimeAccessToAppTables.md)

