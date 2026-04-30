---
title: Customize hierarchical node map levels for Lead-to-Cash Process Management
description: Customize the number of node levels to display in the Lead-to-Cash Process Management hierarchical node map visualization.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing the sales process dashboard, Configuring Lead-to-Cash Process Management, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Customize hierarchical node map levels for Lead-to-Cash Process Management

Customize the number of node levels to display in the Lead-to-Cash Process Management hierarchical node map visualization.

## Before you begin

Role required: admin

## About this task

By default, the Lead-to-Cash Process Management hierarchical node map shows three node levels. Although there is no upper limit on the number of node levels you can display, the node map can display a maximum of 250 nodes at a time.

## Procedure

1.  Select **All** and in the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for sn\_l2c\_cockpit.node\_default\_levels and select it.

3.  If a message appears about the application scope, select **here** to be able to edit the record."

4.  In the **Value** field, specify an integer for the number of node levels you want to display on the hierarchical node map.

5.  Select **Update**.


**Parent Topic:**[Customizing the sales process dashboard](../concept/customizing-sales-process-dashboard.md)

