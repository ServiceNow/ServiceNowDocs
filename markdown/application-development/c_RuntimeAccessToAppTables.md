---
title: Runtime access to applications tables
description: Runtime access determines if an API or web service call can run against an application table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Runtime access to applications tables

Runtime access determines if an API or web service call can run against an application table.

Access permissions can be set for the following access points.

|Access points|Description|
|-------------|-----------|
|Script API|Any supported object or method call from the scoped system API such as a GlideRecord call.|
|Web services|Any supported web service call such as a REST, JSON, or SOAP web service.|

The system does not prevent you from creating API or web service calls to the application tables, rather it determines if the API or web service call is allowed to run against the application table. API or web service calls that violate the access permissions for an application table produce an error. For example, making a web service call to a protected application table produces a 403 Forbidden HTTP error.

-   **[Default runtime access permissions](c_DefaultRuntimeAccessPermissions.md)**  
The default runtime access permissions apply to new application data tables.
-   **[Set runtime access to application tables](../task/t_SetRuntimeAccessToAppTables.md)**  
Set these access permissions to protect application tables at runtime.
-   **[Example denying all runtime access to a table](c_ExampleDenyingAllRuntimeAccess.md)**  
You can prevent script API and web service calls from other application scopes.
-   **[Example granting all runtime access to a table](c_ExampleGrantingAllRuntimeAccess.md)**  
You can permit some or all runtime script API and web service calls from other application scopes.

**Parent Topic:**[Table design and runtime settings](../reference/r_TableApplicationAccessFields.md)

