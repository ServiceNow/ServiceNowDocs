---
title: Configuring Agent Client Collector for Visibility - Content
description: Plan and configure your Agent Client Collector for Visibility - Content \(ACC-VC\) implementation.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Configuring Agent Client Collector for Visibility - Content

Plan and configure your Agent Client Collector for Visibility - Content \(ACC-VC\) implementation.

## Configuration overview

ACC-VC requires installation of the ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.

Configuring Agent Client Collector for Visibility - Content requires the following:

-   Discovery plugin \(com.snc.discovery\) must be installed and activated.
-   Agent Client Collector Framework \(ACC-F\) must be installed on the ServiceNow instance.
-   Agent must be installed on the target host.
-   Ensure that you have upgraded to Quebec patch 3 or later.
-   In a Linux or macOS environment, ensure that you are logged in as a servicenow user.

    In a Windows environment, ensure that you are logged in as a Local System user.

-   ITOM Discovery or ITOM Visibility SKUs \(SU-based licensing\) is required.

You can then download and install the Agent Client Collector for Visibility - Content \(ACC-VC\) application from the ServiceNow Store or from the instance \[sn\_acc\_visibility\]. See [Agent Client Collector Installation](acc-installation.md) for details.

**Note:** The ServiceNow Store regularly releases new applications and updates to applications that are created by the ServiceNow Store. If you already have the application, you can download the latest version to enhance your existing experience. Since different features are available or enhanced each time an application is released in the Store, the content and features available are indicated by version number in this document.

