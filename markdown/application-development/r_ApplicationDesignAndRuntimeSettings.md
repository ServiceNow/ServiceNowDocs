---
title: Application design and runtime settings
description: The application design and runtime settings determine whether an application can access cross-scope resources.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application design and runtime settings

The application design and runtime settings determine whether an application can access cross-scope resources.

|Field|Description|
|-----|-----------|
|JavaScript Mode|The JavaScript standard that the application supports. Select **ECMAScript 2021 \(ES12\)** to support features in ECMAScript 12th edition or **ES5 Standards Mode** to support features in ECMAScript 5th edition. Select **Compatibility Mode** to support earlier ECMAScript editions. For more information, see [Set the JavaScript mode for an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/set-javascript-mode-application.md).|
|Runtime Access Tracking|The application's handling of script access requests to resources in other applications. Select **None** to authorize all access requests to cross-scope resources without logging them. Select **Tracking** to log and authorize all access requests to cross-scope resources. Select **Enforcing** to log access requests to cross-scope resources but require an administrator to authorize each request.|
|Restrict Table Choices|The availability of cross-scope tables when designing the application. Clear the option to allow the application to see tables from other application scopes. Select the option to restrict design choices to only tables in the same application.|

-   **[Runtime access tracking](../concept/c_RuntimeAccessTracking.md)**  
Runtime access tracking allows administrators to manage script access to application resources by creating a list of script operations and targets that the system authorizes to run.
-   **[Cross-scope privilege record](c_CrossScopePrivilegeRecord.md)**  
Runtime access tracking uses cross-scope privilege records to determine which script operations and targets the system allows to run.
-   **[Application design access record](../concept/c_ApplicationDesignAccessRecord.md)**  
Administrators use application design access records to specify which other applications are available to developers during application creation.

**Parent Topic:**[Application access settings](../concept/c_ApplicationAccessSettings.md)

