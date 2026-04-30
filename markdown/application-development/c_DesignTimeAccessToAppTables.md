---
title: Design-time access to application tables
description: As the application developer, you can grant or deny other applications the permission to create configuration records, also known as application files, that extend the functionality of an application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Design-time access to application tables

As the application developer, you can grant or deny other applications the permission to create configuration records, also known as application files, that extend the functionality of an application.

The permission applies to any platform feature that extends the functionality of an application data table such as:

-   Business rules
-   UI actions
-   Client scripts

These access permissions protect the application data table at design-time. The system prevents you from creating configuration records by hiding the application data table as an option in the **Table** field. For example, a protected application table does not appear as an option when you create configuration records such as UI actions and client scripts.

Even when permission is granted to create configuration records, some configuration records have additional restrictions to protect application data from unwanted changes from other application scopes.

-   **[Default design access permissions](c_DefaultDesignAccessPermissions.md)**  
By default, new application tables prevent other application scopes from creating configuration records on application data tables. This prevents any other applications from changing the functionality of a table.
-   **[Set design-time access to application tables](../task/t_SetDesignTimeAccessToAppTables.md)**  
Set these access permissions to protect application tables at design-time.
-   **[Example denying all design access to a table](c_ExampleDenyingAllDesignAccess.md)**  
You can prevent other application scopes from creating configuration records on application data tables.
-   **[Example allowing configuration records for a table](c_ExampleGrantingAccessToConfigRecs.md)**  
You can permit other application scopes to create configuration records on application data tables.

**Parent Topic:**[Table design and runtime settings](../reference/r_TableApplicationAccessFields.md)

