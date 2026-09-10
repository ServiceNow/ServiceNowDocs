---
title: Enhance Event Management performance
description: The Event Management Performance Accelerator plugin helps maintain Event Management performance at a high level. This plugin is optional.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/improve-event-mgmt-performance.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Enhance Event Management performance

The Event Management Performance Accelerator plugin helps maintain Event Management performance at a high level. This plugin is optional.

## Before you begin

Role required: admin

## About this task

The **em\_alert\_history** and **em\_impact\_status** tables can grow very large, negatively impacting Event Management performance. The Event Management Performance Accelerator plugin includes fix scripts that populate missing data, update key fields to maintain data accuracy, and create indexes to enhance performance. These actions help optimize large datasets and reduce the impact on query speed and overall system responsiveness.

When upgrading from an earlier version with more than 5 million records in either the **em\_alert\_history** or **em\_impact\_status** tables, you must activate this plugin manually. When there are fewer than 5 million records, it activates automatically. You can customize this number by modifying the **evt\_mgmt.plugin\_activation.table\_max\_size** property.

To evaluate the Event Management Performance Accelerator plugin on a subproduction instance, install the plugin in Application Manager. For instructions, see [Install an app or plugin](https://www.servicenow.com/docs/r/platform-administration/application-manager/installing-applications-in-application-manager.html).

## Procedure

1.  Activate the Event Management Performance Accelerator plugin.


