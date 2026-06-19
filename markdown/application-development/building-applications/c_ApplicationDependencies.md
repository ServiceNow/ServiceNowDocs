---
title: Dependencies for custom applications
description: Every custom application record includes a related list identifying its dependencies on other applications. Dependencies are references from your custom application to functionality provided by other applications or plugins installed on the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/c\_ApplicationDependencies.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Dependencies for custom applications

Every custom application record includes a related list identifying its dependencies on other applications. Dependencies are references from your custom application to functionality provided by other applications or plugins installed on the instance.

The ServiceNow AI Platform tracks dependencies automatically so that when your application is installed on another instance, the platform can:

-   Verify that required components are present.
-   Prompt the administrator to install missing components before installation proceeds.

Without accurate dependency information, your application may fail on instances where those supporting components are missing.

The platform determines dependencies based on the components your application references outside its own scope. Common examples include:

-   A business rule that calls a script include from another application.
-   A flow that uses an action provided by an installed spoke.
-   Any application metadata that explicitly references components outside the application scope.

To remove a dependency, navigate to the application record and locate the Dependencies related list. Before deleting a dependency record, confirm that the application no longer references any components from that application or plugin. Removing a required dependency causes errors on instances where the supporting component is not installed.

\[Omitted image "app-dependencies.png"\] Alt text: Remove dependencies from the custom app record by accessing the Dependencies related list.

