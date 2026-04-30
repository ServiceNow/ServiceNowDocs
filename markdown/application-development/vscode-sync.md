---
title: Synchronization between Visual Studio Code and a ServiceNow instance
description: You can synchronize your applications between Visual Studio Code and your ServiceNow instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Synchronization between Visual Studio Code and a ServiceNow instance

You can synchronize your applications between Visual Studio Code and your ServiceNow instance.

## Synchronization

Changes made to your applications in Visual Studio Code are stored on your local file system only until you synchronise with your instance.

Synchronization accounts for the following changes:

-   File modifications on the instance or in the local file system
-   File creation on the instance or in the local file system
-   File deletion on the instance or in the local file system

You can sync your currently selected record or all records in the current application.

-   **[Sync the current file between a Visual Studio Code workspace and a ServiceNow instance](../task/sync-current-file.md)**  
Identify conflicting files and merge or overwrite the changes, between the current file in your Visual Studio Code workspace and your instance.
-   **[Synchronize the current project between a Visual Studio Code workspace and a ServiceNow instance](../task/synchronize-files.md)**  
Synchronize files between the Visual Studio Code workspace \(client/local\) and the instance \(server\) bi-directionally.

**Parent Topic:**[ServiceNow Extensions for Visual Studio Code](vs-code.md)

