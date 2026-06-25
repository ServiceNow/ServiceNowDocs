---
title: Configure AI Desktop Actions
description: You can enable the AI Desktop Actions application if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-agentic-desktop.html
release: australia
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 1
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Configure AI Desktop Actions

You can enable the AI Desktop Actions application if you have the admin role.

## Before you begin

To get started with AI Desktop Actions, you must have:

-   A ServiceNow Pro Plus or Enterprise Plus license.
-   An instance on Zurich Patch 4+.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.

Role required: administrator

## About this task

AI Desktop Actions isn’t a standalone application that you can install directly. To enable AI Desktop Actions on your instance, you must install other Now Assist applications, such as Now Assist for IT Service Management \(ITSM\) or Now Assist for Customer Service Management \(CSM\).

-   Review the [AI Desktop Actions](https://store.servicenow.com/store/app/dc9057f4873932d0221e8409dabb35a5) application listing in ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Perform these steps in your ServiceNow instance.

For more information about the components installed, see [Components installed with AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/components-installed-with-agentic-desktop.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for and select a Now Assist application, such as Now Assist for IT Service Management \(ITSM\) or Now Assist for Platform.

3.  Select **Install**.


## What to do next

-   **Defined desktop action**

    Download and install the AI Desktop Actions installer on your system to automate repetitive tasks that involve fixed steps in your desktop and web environment. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

-   **Adaptive desktop action**

    Install the Chrome browser extension and configure allowed websites to automate repetitive tasks that involve adaptive steps for web applications. For more information, see [Install the Google Chrome extension for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-wa-install-browser-extension.md) and [Configure allowed websites for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-wa-configure-allowed-websites.md).


