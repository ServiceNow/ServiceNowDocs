---
title: Manage a service
description: Using the Service Creator, department managers can request a new service category, designate editors and service fulfillers for that category, and create and publish services.
locale: en-US
release: zurich
product: Service Creator
classification: service-creator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Creator, Building pro-code applications, Developing your application, Building applications]
---

# Manage a service

Using the Service Creator, department managers can request a new service category, designate editors and service fulfillers for that category, and create and publish services.

## Before you begin

Role required: none

## About this task

Editors create and modify services. Service fulfillers complete the tasks generated from service requests.

A service category request involves assigning a service category manager, which is typically the department manager who makes the request. After the request is submitted, a catalog administrator approves the request to publish the service category. When the category is published, the service category manager can assign service category editors and service fulfillers, and create services to offer in the service catalog.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Select the **Departmental Services** category.

    The Departmental Services category is part of the demo data available with service creator. If this category does not exist, a catalog administrator must add the Service Category Request catalog item to an existing category.

3.  Select the **Service Category Request** item.

4.  Change the default values, as necessary \(see table\).

5.  Click **Submit**.

    ![Service Creator Request Category](../image/ServiceCreatorRequestCategory.png)

    |Field|Description|
    |-----|-----------|
    |Department|Department this category request is for. By default this value is the department of the current user. Changing this value also changes the Category name and Category manager values.|
    |Category name|Name for the new service category. By default, ServiceNow uses a name based on the Department value.|
    |Category manager|Designated manager for the new service category. By default, ServiceNow uses the manager for the selected department.|
    |Needed by|Date that the new service category should be available.|
    |Comments|Additional comments describing the service category. This information appears as a journal entry on the Service Category form.|


