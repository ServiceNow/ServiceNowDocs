---
title: Synchronizing applications in the ServiceNow IDE
description: Synchronizing an application in the ServiceNow IDE downloads and transforms application metadata into ServiceNow Fluent code.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Develop applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Synchronizing applications in the ServiceNow IDE

Synchronizing an application in the ServiceNow IDE downloads and transforms application metadata into ServiceNow Fluent code.

ServiceNow Fluent supports two-way synchronization, which allows changes to metadata to be synced from other ServiceNow AI Platform user interfaces into source code. When you build and install an application, changes to source code are compiled into metadata across the instance. This process enables collaborating with users of different skill sets because developers can modify the ServiceNow Fluent code while others modify the application metadata across the platform.

In the ServiceNow IDE, when metadata in an application is changed, you're prompted to sync the application to get the latest changes. If metadata changes are detected in application, syncing is required before you can install the application across the instance.

**Note:** If you ignore the notification to sync an application, you aren't prompted to do so again for the remainder of the session. If you try to install the application or refresh the browser, you are prompted to sync again.

You can sync an application on demand from the Now SDK view \(![Now SDK](../image/servicenow-ide-sdk-icon.png)\) or from the command palette with the `Fluent: Sync Fluent App with changed metadata` command.

![The Sync command in the Now SDK view.](../image/servicenow-ide-sync.png)

## Synchronization process in the ServiceNow IDE

The following list explains the stages of the synchronization process for applications in the ServiceNow IDE:

1.  Before the first time an application is synced:
    -   You should initialize a repository.
    -   You should stage any changes to the application to retain them when the application is synced.
2.  The first time that an application is synced:
    -   New metadata that isn't defined in source code is transformed into source code in the `src/fluent/generated` directory.
    -   Changes to metadata that is defined in source code are downloaded into source code in the `src/fluent` and `src/fluent/generated` directories.
    -   Changes to existing metadata XML that hasn't been converted into source code are downloaded into the `metadata` directory.
3.  Subsequent times that an application is synced:
    -   Only the changes made since the last time the application was synced are downloaded and transformed.
    -   Optionally, you can synchronize all metadata in the application with the `Fluent: Force Sync of Fluent App with all metadata` command from the command palette. Before running this command, you should stage any changes to retain them.

**Parent Topic:**[Developing applications with the ServiceNow IDE](developing-applications-servicenow-ide.md)

**Related topics**  


[ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

