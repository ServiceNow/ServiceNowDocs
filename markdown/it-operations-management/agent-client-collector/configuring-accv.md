---
title: Configuring Agent Client Collector for Visibility
description: Plan and configure your Agent Client Collector for Visibility \(ACC-V\) implementation.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Configuring Agent Client Collector for Visibility

Plan and configure your Agent Client Collector for Visibility \(ACC-V\) implementation.

## Configuration overview

ACC-V requires installation of the ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.

Configuring Agent Client Collector for Visibility requires the following:

-   Discovery plugin \(com.snc.discovery\) must be installed and activated.
-   Agent Client Collector Framework \(ACC-F\) must be installed on the ServiceNow instance.
-   Agent must be installed on the target host.
-   Ensure that you have upgraded to Quebec patch 3 or later.
-   Ensure that you have local\_system\_account privileges.
-   ITOM Discovery or ITOM Visibility SKUs \(SU-based licensing\) is required.

You can then download and install the Agent Client Collector for Visibility \(ACC-V\) application from the ServiceNow Store or from the instance \[sn\_acc\_visibility\]. See [Agent Client Collector Installation](acc-installation.md) for details.

**Note:** The ServiceNow Store regularly releases new applications and updates to applications that are created by the ServiceNow Store. If you already have the application, you can download the latest version to enhance your existing experience. Since different features are available or enhanced each time an application is released in the Store, the content and features available are indicated by version number in this document.

