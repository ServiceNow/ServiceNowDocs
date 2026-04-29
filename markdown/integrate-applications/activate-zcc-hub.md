---
title: Activate Zero Copy Connector Hub
description: Access the Zero Copy Connector Hub on your instance by activating the Zero Copy Connector Hub plugin \(sn\_data\_fabric\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Zero Copy Connectors, Workflow Data Fabric]
---

# Activate Zero Copy Connector Hub

Access the Zero Copy Connector Hub on your instance by activating the Zero Copy Connector Hub plugin \(sn\_data\_fabric\).

## Before you begin

Role required: admin

## About this task

Follow the steps below to activate the Zero Copy Connector Hub on your instance. For the full experience, request the Zero Copy Connectors application \(sn\_data\_fabric\_zcc\). The Zero Copy Connector Hub is automatically activated when the Zero Copy Connectors plugin \(sn\_data\_fabric\_zcc\) is activated on your instance.

Roles are installed with Zero Copy Connector Hub.

For more information, see [Zero Copy Connectors roles](../reference/roles-zcc.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Zero Copy Connector Hub plugin \(sn\_data\_fabric\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Zero Copy Connectors](../concept/configuring-zcc.md)

