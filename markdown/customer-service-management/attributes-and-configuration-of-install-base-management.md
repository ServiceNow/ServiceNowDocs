---
title: Install base characteristics
description: Customer service managers can create the characteristics of the install base items, while administrators can capture and track the characteristics of the install base items by using the Customer Service Management application. These characteristics can provide information about the service requirements and verify timely maintenance services for the install base item.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Install base characteristics

Customer service managers can create the characteristics of the install base items, while administrators can capture and track the characteristics of the install base items by using the Customer Service Management application. These characteristics can provide information about the service requirements and verify timely maintenance services for the install base item.

## Overview

Install base characteristics enable flows like case management, field service management, planned maintenance, and reactive service requirements to occur on a schedule. Some install base characteristics are configurable and vary from product to product. The product model characteristics are non-configurable and are directly taken from the product model that is associated with the install base item.

Only users with the sn\_customerservice\_manager role can create the characteristics for the install base items. Users with the administrator role can activate the Install base characteristics plugin \[com.snc.install\_base\_characteristics\] to capture and view all the install base characteristics on the Install base form. To activate the plugin, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

The Install base characteristics data model represents how the characteristics of an install base item are stored. To learn about the different fields and tables that they're stored in, see [Data model for the Install base item characteristics](install-base-item-characteristics-data-model.md).

## Roles

With the admin role, you can track the characteristics to provide the required product information to administrators, agents, business stakeholders, and customers. You can also track the services that are associated with an install base item at the time of purchase. With this role, you can capture the configurable and non-configurable characteristics to view the configuration specifications for an install base item.

With the sn\_customerservice\_manager role, you can create a set of configurable characteristics for an install base item on the Customer Service Management \(CSM\) application. It enables you to view the install base item details and its associated services. After you create an install base characteristic, the characteristic appears in the related list on the install base item form. For more information, see [Create the install base characteristics for an install base item](../task/create-install-base-characteristics.md).

There are different functional and granular roles to provide varying levels of permissions to users. For information on the different access levels, see [Security roles for the install base characteristics](security-roles-for-install-base-attributes.md).

## Install Base characteristics

The install base characteristics are stored in the Install Base Characteristics table \[sn\_install\_base\_item\_characteristic\]. However, both the install base and product model characteristics are displayed in the Install base characteristics and product model related lists on the install base form. You can use the text search option on the Customer Service platform and portals to search for the characteristics on the Install Base characteristics table.

You can view the install base characteristics on the Customer Service, Consumer Service, and Business Location Service Portal \(BLSP\).

Under the **Support** header on the portals home page, you can view the information about the install base characteristics that are associated with the parent install base item. The characteristics that are associated with the child items aren’t visible on the portals. For more information about the install base items from the Customer Service Portal, see [View install base information from the Customer Service Portal](../task/view-install-base-info.md).

