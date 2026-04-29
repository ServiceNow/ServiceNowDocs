---
title: Attribute packs
description: Use an attribute pack to capture the attributes that you define against a set of records in a configuration item \(CI\) in the Telecommunications Network Inventory application. You can capture the additional information about the network asset in the inventory form that belongs to the CI.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Attribute packs

Use an attribute pack to capture the attributes that you define against a set of records in a configuration item \(CI\) in the Telecommunications Network Inventory application. You can capture the additional information about the network asset in the inventory form that belongs to the CI.

## Introduction to attribute packs

An attribute pack is a collection of attributes that you can associate with a subset of a CI. A pack is an extra set of attributes. These attributes are defined as standard ServiceNow AI Platform tables and columns.

You create an attribute pack table and configure the mapping between a pack table and CI. When you create or update the CI record, you can add the pack table and provide the additional information about the inventory object.

By using an attribute pack, you can manage a CI and its attributes more granularly. For example, if you consider a server as a CI, an attribute pack for a server could include such attributes as a hostname or IP address. These attributes provide additional information about the server that helps you to manage and track it throughout its life cycle. To learn more about how to use an attribute pack in the inventory form, see [Using an attribute pack in an inventory form](telecommunication-network-inventory-pack.md#section_ybf_dg3_gxb) section.

Use an attribute pack to customize the attributes according to the requirements of your organization or a subset of CIs. This customization enables your organizations to scale your present and future inventory management needs.

## Using an attribute pack in an inventory form

To use an attribute pack in an inventory form, you, as the administrator, must perform the following tasks:

-   Create a pack table with the attributes that you define. To learn more, see [Create table](../task/create-pack-table.md).
-   Configure the mapping between the pack table and the inventory object that you want to use it with. To learn more, see [Configure an attribute pack table against a configuration item](../task/configure-packs-for-a-ci-form.md).

After you create and configure a pack table, you can use it in a CI record. To learn more, see [Attribute pack for CI records](using-pack-table-ci-record.md).

