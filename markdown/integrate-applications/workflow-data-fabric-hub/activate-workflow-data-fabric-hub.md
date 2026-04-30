---
title: Activate Workflow Data Fabric Hub
description: Access Workflow Data Fabric Hub on your instance by activating the Workflow Data Fabric Hub plugin \(sn\_data\_fabric\).
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-05-20"
reading_time_minutes: 1
breadcrumb: [Configuring Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Activate Workflow Data Fabric Hub

Access Workflow Data Fabric Hub on your instance by activating the Workflow Data Fabric Hub plugin \(sn\_data\_fabric\).

## Before you begin

Role required: admin

## About this task

Follow the steps below to activate Workflow Data Fabric Hub on your instance. For the full experience, request the Zero Copy Connectors application \(sn\_data\_fabric\_zcc\). Workflow Data Fabric Hub is automatically activated when the Zero Copy Connectors plugin \(sn\_data\_fabric\_zcc\) is activated on your instance.

Roles are installed with Workflow Data Fabric Hub.

For more information, see [Workflow Data Fabric Hub roles](../reference/workflow-data-fabric-roles.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Workflow Data Fabric Hub plugin \(sn\_data\_fabric\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Workflow Data Fabric Hub](../concept/configuring-wdf.md)

