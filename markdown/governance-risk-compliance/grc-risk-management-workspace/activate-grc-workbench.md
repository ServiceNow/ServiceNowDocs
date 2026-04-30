---
title: Activate GRC: Workbench
description: The GRC: Workbench plugin is not activated by default, it is available as a separate subscription within the GRC Suite.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Activate GRC: Workbench

The GRC: Workbench plugin is not activated by default, it is available as a separate subscription within the GRC Suite.

## Before you begin

Role required: admin

## About this task

To create entity classes, entity dependencies, and risk dependencies activate the GRC: Workbench, and the GRC: Risk Management plugin \[com.sn\_risk\].

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)

**Related topics**  


[List of plugins](activate-grc-workbench.md)

