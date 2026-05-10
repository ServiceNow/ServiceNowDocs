---
title: Set up the Agent Client Collector spoke
description: Integrate the ServiceNow Agent Client Collector framework and Agent Client Collector spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Agent Client Collector spoke

Integrate the ServiceNow Agent Client Collector framework and Agent Client Collector spoke.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Agent Client Collector spoke.
-   Role required: admin

## About this task

1.  Install the Agent Client Collector Framework v2.2.0 \(sn\_agent\) plugin and the other dependant plugins. For more information, see [Agent Client Collector installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-installation.md).

    **Note:** To enable Agent Client Collector to execute commands, ensure that `ACC_ALLOW_LIST=0` for Linux environments or `ACC_ALLOW_LIST=False` for Windows environments. If you are using Windows guided installation, clear the **Enable executing command allow list** check-box. Otherwise, you cannot execute commands using the Agent Client Collector spoke.

    ![Agent Client Collector Configuration configuration for Windows environments.](../image/acc-setup-wizard.png)

2.  [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md).
3.  [Configure the websocket server on the MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-configure-web-server.md).

