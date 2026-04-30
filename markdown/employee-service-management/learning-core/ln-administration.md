---
title: Administration tasks in Learning Core
description: Complete the administrative tasks in Learning Core with the Learning admin \[learning\_admin\] role.
locale: en-US
release: yokohama
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Administration tasks in Learning Core

Complete the administrative tasks in Learning Core with the Learning admin \[learning\_admin\] role.

## Before you begin

Role required: learning\_admin

## Procedure

1.  Create source records for learning management systems that are integrating with Learning Core.

    For more information, see [Create a source for a learning system](set-up-int-lc.md).

    **Important:** Once you set up the Learning Core application, the source record for Cornerstone OnDemand, Pluralsight, Udemy, Sumtotal , and Saba applications are automatically created in the Source module in Enterprise Service Management Integrations Framework. These source records contain a predefined set of properties and integration services that help in pulling learning courses from Cornerstone On Demand, Pluralsight, Udemy, Sumtotal, and Saba applications into your ServiceNow instance.

2.  Configure properties for various settings used in Learning Core.

    For more information, see [Configure properties for Learning Core](config-ln-prop.md).

3.  View the consolidated report on courses in each source, the number of catalogs associated with each of the source, and the status of learning tasks by source.

    For more information, see [Reporting Solutions for Learning Core](../concept/learning-exp-db.md).


-   **[Create a source for a learning system](set-up-int-lc.md)**  
Create a source record for the third-party learning system that you want to integrate with your ServiceNow instance.
-   **[Configure properties for Learning Core](config-ln-prop.md)**  
Configure properties for various settings used in Learning Core.
-   **[Configure a learning system](create-source-ln.md)**  
Configure the learning system so that the schedule flow pulls learning content from the third-party system into a ServiceNow instance.

**Parent Topic:**[Configuring Learning Core](../concept/configuring-learning-core.md)

**Related topics**  


[Integrating Learning Core with third-party learning management systems](setup-learning-third-party-1.md)

