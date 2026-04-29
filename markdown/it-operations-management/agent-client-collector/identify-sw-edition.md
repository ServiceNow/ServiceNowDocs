---
title: Identify software editions on Windows devices
description: Determine which edition of software is in use on Windows devices in your environment, to maintain an accurate software inventory. Software products commonly support multiple editions, making it difficult to identify which edition is in use.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Identify software editions on Windows devices

Determine which edition of software is in use on Windows devices in your environment, to maintain an accurate software inventory. Software products commonly support multiple editions, making it difficult to identify which edition is in use.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  In the navigation pane, enter `sn_acc_vis_content_software_registry_edition_config.list`.

    The **Software Edition Configurations** page appears.

2.  Select **New** to set edition configuration for a Windows device.

    The **Software Edition Configuration - New record** page appears. For details on the fields displayed on the page, see [Software edition configuration fields](../reference/software-edition-configuration.md).

3.  Select **Submit**.

    The configured product appears on the **Software Edition Configurations** page, and is automatically added to the `EditionRegistryConfig.json` file after the daily scheduled job runs.

4.  In the navigation pane, enter `cmdb_sam_sw_install.list`.

    The **Software Installations** page opens.

5.  Find the relevant software entry, and confirm the edition in the **Edition override** column.

    The edition appears only after the **Software Installed** or **SAM Discovery** policy runs. By default, these policies runs once daily.


**Parent Topic:**[Deploying Agent Client Collector on endpoints](../concept/acc-endpoint-deployment.md)

