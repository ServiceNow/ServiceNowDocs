---
title: Synchronizing Fluent apps in ServiceNow Studio
description: Synchronizing an application in ServiceNow Studio downloads and transforms application metadata into ServiceNow Fluent code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/servicenow-studio-classic/synchronizing-fluent-apps.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Synchronizing Fluent apps in ServiceNow Studio

Synchronizing an application in ServiceNow Studio downloads and transforms application metadata into ServiceNow Fluent code.

ServiceNow Fluent supports two-way synchronization, which syncs metadata changes from other ServiceNow AI Platform user interfaces into source code. When you build and install an application, the build compiles source code changes into metadata across the instance. This process enables you to collaborate with users of different skill sets because developers can modify the ServiceNow Fluent code while others modify the application metadata across the platform.

In ServiceNow Studio, when metadata in an application changes, you are prompted to sync the application to get the latest changes. If metadata changes exist in an application, you must sync the application before you install it across the instance.

**Note:** If you ignore the notification to sync an application, you are not prompted to do so again for the remainder of the session. If you try to install the application or refresh the browser, you are prompted to sync again.

Sync an application on demand from the status bar, or from the command palette with the `Fluent: Sync Fluent App with changed metadata` command.

\[Omitted image "sn-studio-status-bar.png"\] Alt text: Sync changes from the status bar.

## How does synchronization work in ServiceNow Studio?

The following list explains the stages of the synchronization process for applications in ServiceNow Studio:

1.  Before the first time an application is synced:
    -   Initialize a repository.
    -   Stage any changes to the application to retain them when the application is synced.
2.  The first time that an application is synced:
    -   New metadata that is not defined in source code is transformed into source code in the `src/fluent/generated` directory.
    -   Changes to metadata that is defined in source code are downloaded into source code in the `src/fluent` and `src/fluent/generated` directories.
    -   Changes to existing metadata XML that has not been converted into source code are downloaded into the `metadata` directory.
3.  Subsequent times that an application is synced:
    -   Synchronization downloads and transforms only the changes made since the last time the application was synced.
    -   To synchronize all metadata in the application, run the `Fluent: Force Sync of Fluent App with all metadata` command from the command palette. Before running this command, stage any changes to retain them.

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

