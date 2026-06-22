---
title: Install base characteristics
description: Customer service managers can create the characteristics of the Install base items, while administrators can capture and track the characteristics of the Install base items with the Customer Service Management application. These characteristics can provide information about the service requirements and verify timely maintenance services for the Install base item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/attributes-and-configuration-of-install-base-management.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Install base items, Configure Install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Install base characteristics

Customer service managers can create the characteristics of the Install base items, while administrators can capture and track the characteristics of the Install base items with the Customer Service Management application. These characteristics can provide information about the service requirements and verify timely maintenance services for the Install base item.

## Overview of characteristics

Install base characteristics enable flows like case management, field service management, planned maintenance, and reactive service requirements to occur on a schedule. Some Install base characteristics are configurable and vary from product to product. The product model characteristics are non-configurable and are directly taken from the product model that is associated with the Install base item.

With the sn\_customerservice\_manager role, you can create the characteristics for the Install base items. With the administrator role, you can download the Install base characteristics plugin \[com.snc.install\_base\_characteristics\] to capture and view all the Install base characteristics on the Install base form. To activate the plugin, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_ActivateAPlugin.md).

The Install base characteristics data model represents how the characteristics of an Install base item are stored. To learn about the different fields and tables that they're stored in, see [Data model for the Install base item characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/install-base-item-characteristics-data-model.md).

## Roles

With the admin role, you can track the characteristics to provide the required product information to administrators, agents, business stakeholders, and customers. You can also track the services that are associated with an Install base item at the time of purchase. With this role, you can capture the configurable and non-configurable characteristics to view the configuration specifications for an Install base item.

With the sn\_customerservice\_manager role, you can create a set of configurable characteristics for an Install base item on the Customer Service Management \(CSM\) application. It enables you to view the Install base item details and its associated services. After you create an install base characteristic, the characteristic appears in the related list on the Install base item form. For more information, see [Create the Install base characteristics for an Install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-install-base-characteristics.md).

There are different functional and granular roles to provide varying levels of permissions to users. For information on the different access levels, see [Security roles for the Install base characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/security-roles-for-install-base-attributes.md).

## Install Base characteristics

The characteristics are stored in the Install Base Characteristics table \[sn\_install\_base\_item\_characteristic\]. However, both the Install base and product model characteristics are displayed in the Install base characteristics and product model related lists on the Install base form. You can use the text search option on the Customer Service platform and portals to search for the characteristics on the Install Base characteristics table.

You can view the Install base characteristics on the Customer Service, Consumer Service, and Business Location Service Portal \(BLSP\).

Under the **Support** header on the portals home page, you can view the information about the Install base characteristics that are associated with the parent Install base item. The characteristics that are associated with the child items aren’t visible on the portals. For more information about the Install base items from the Customer Service Portal, see [View install base information from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/view-install-base-info.md).

