---
title: Restructuring RPA Hub tables
description: Starting with the Utah release, the Robotic Process Automation \(RPA\) tables are restructured to an application file, so that changes that you make to these tables are captured in the update sets and can be moved seamlessly across environments. With this process, you don't have to re-create the data records in the targeted environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrate data, RPA Hub, Workflow Data Fabric]
---

# Restructuring RPA Hub tables

Starting with the Utah release, the Robotic Process Automation \(RPA\) tables are restructured to an application file, so that changes that you make to these tables are captured in the update sets and can be moved seamlessly across environments. With this process, you don't have to re-create the data records in the targeted environment.

The table architecture that supports the RPA Hub application has been restructured to extend the Application file \(sys\_metadata\). This action automatically captures all the data into the update sets.

If you are upgrading from Tokyo or older to Australia, the bot process definitions change to the new structure, that is the bot process configuration.

The following diagram shows the tables of RPA Hub before restructuring.

![RPA Hub tables before restructuring.](../image/bot-process-restructure-before.png "RPA Hub tables before restructuring")

The following diagram shows the tables of RPA Hub after restructuring.

![RPA Hub tables after restructuring.](../image/bot-process-config-restructure.png "RPA Hub tables after restructuring")

For detailed information about the script that restructures the tables during an upgrade, see the [Restructuring RPA Hub tables to sys\_metadata in Utah](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

**Parent Topic:**[Migrating data in RPA Hub](migrating-data-rpa-hub.md)

