---
title: Configure AI Desktop Actions
description: You can enable the AI Desktop Actions application \(sn\_desktop\_agents\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 1
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Configure AI Desktop Actions

You can enable the AI Desktop Actions application \(sn\_desktop\_agents\) if you have the admin role.

## Before you begin

To get started with AI Desktop Actions, you must have:

-   A ServiceNow Pro Plus or Enterprise Plus license.
-   An instance on Yokohama Patch 11+ or Zurich Patch 4+.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.

Role required: administrator

## About this task

AI Desktop Actions isn’t a standalone application that you can install directly. To enable AI Desktop Actions on your instance, you must install other Now Assist applications, such as Now Assist for IT Service Management \(ITSM\) or Now Assist for Customer Service Management \(CSM\).

-   Review the [AI Desktop Actions](https://store.servicenow.com/store/app/dc9057f4873932d0221e8409dabb35a5) application listing in ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Perform these steps in your ServiceNow instance.

By enabling the AI Desktop Actions application \(sn\_desktop\_agents\), you can view the AI Desktop Actions and download modules in your ServiceNow instance.

The following items are installed with AI Desktop Actions:

-   Roles
-   Tables

For more information, see [Components installed with AI Desktop Actions](../reference/components-installed-with-agentic-desktop.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for and select a Now Assist application, such as Now Assist for IT Service Management \(ITSM\) or Now Assist for Platform.

3.  Select **Install**.


## What to do next

Download and install the AI Desktop Actions installer on your system to automate repetitive tasks in your desktop environment. For more information, see [Download AI Desktop Actions installer](download-agentic-desktop-installer.md).

