---
title: Configure the catalog items for your service
description: Filter the catalog items that you want to show in the Submit Catalog Item task for your service.
locale: en-US
release: zurich
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring your service, Configure, Universal Task, Employee Service Management]
---

# Configure the catalog items for your service

Filter the catalog items that you want to show in the Submit Catalog Item task for your service.

## Before you begin

Role required: sn\_uni\_task.admin

## About this task

You can add filters to manage the catalog items that are available to a user. For instance, some catalog items might be restricted based on the location or service type of the request.

## Procedure

1.  Navigate to **All** &gt; **Universal Task** &gt; **Administration** &gt; **Catalog Task Configuration**.

2.  Click **New**.

3.  Select your service-specific table as the parent table.

    **Note:** You can select only the service-specific tables that have been configured for Universal Task with the Submit Catalog Item task type.

4.  To filter the items that you show in the Submit Catalog Item task, add the **Catalog item filter** field.

5.  Enter the **Order** value.

6.  Add a parent table **Condition** for the catalog item, if any.

    For example, in the following configuration, the catalog item filter is applicable only if the assignment group of the parent table \[incident\] is Change Management. ![Condition field sample.](../images/ut-condition-field.png)

    You can create multiple conditions to configure your catalog items. The conditions with lower order values get precedence over higher order values.

7.  Click **Submit**.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Configure Universal Task for your service](config-ut-for-service.md)

**Next topic:**[Configure the roles to view employee forms](ut-config-empform-view-roles.md)

