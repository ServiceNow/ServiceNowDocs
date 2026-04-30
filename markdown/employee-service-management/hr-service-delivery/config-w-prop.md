---
title: Configure properties for Worker profile synchronization
description: Set the properties that control Worker profile synchronization.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure worker profile settings, Synchronize worker profiles, Configure, HR Service Delivery Integration with Workday, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure properties for Worker profile synchronization

Set the properties that control Worker profile synchronization.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **System Properties** and set the following property values:

    |Property|Description|
    |--------|-----------|
    |sn\_hr\_workday.worker\_service\_flow\_name|Provide name of the sub flow that is cloned from Get Worker Service. The format must be `scope-name.flow-name`.|
    |sn\_hr\_workday.worker\_page\_size|Specify the page size for Get Workers Service. The maximum page size can be `999`.|
    |sn\_hr\_workday.exclude\_contingent\_workers|Set the value to **True** to exclude the contingent workers from the Workers pull. The default value is **False**.|


