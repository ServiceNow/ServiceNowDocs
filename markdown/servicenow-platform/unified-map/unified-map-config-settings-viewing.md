---
title: How configuration settings for Unified Map are stored
description: General configuration settings that control Unified Map are collected in a configuration identifier. A configuration identifier is a set of properties and table-driven configurations that specify the appearance and content of an instance of a UX application. The CMDB Workspace UX application contains Unified Map.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# How configuration settings for Unified Map are stored

General configuration settings that control Unified Map are collected in a configuration identifier. A configuration identifier is a set of properties and table-driven configurations that specify the appearance and content of an instance of a UX application. The **CMDB Workspace** UX application contains Unified Map.

**Important:** Because each configuration identifier is unique to an instance of a UX application, the settings for one UX application do not affect the user experience of any other UX application. This means that your admin settings for this instance of Unified Map will not affect Unified Map users in another instance.

## Viewing Unified Map configuration settings

The configuration identifier form displays all configurations settings for Unified Map. To view the configuration identifier, navigate to **All** and then, in the filter box in the main navigation bar, enter `sn_cmdb_ws_config_identifier.list`.

On the form, each related list displays property settings or a table of configuration settings.

The base system includes a configuration identifier named **Default** that specifies all default settings.

![Overview of all configuration identifier settings.](../image/um-config-id-form.png)

## Defining custom settings for your CMDB Workspace instance

To create a custom configuration identifier for your workspace, modify the default settings and then save the updates with a new name.

**Note:** When a custom configuration identifier doesn't specify a particular property setting or table entry, the value in the default configuration identifier is used.

**Parent Topic:**[Configuring Unified Map — Admin settings](administer-unified-map.md)

