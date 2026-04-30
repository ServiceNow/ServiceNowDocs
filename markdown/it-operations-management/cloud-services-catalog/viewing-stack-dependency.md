---
title: View stack dependency
description: Explore the details of the configuration items, services, and other tasks that are associated with the stacks and resources by using View Dependency.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring the My Stacks tab, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# View stack dependency

Explore the details of the configuration items, services, and other tasks that are associated with the stacks and resources by using View Dependency.

## Before you begin

Role required: admin

## About this task

A stack can be dependent on multiple stacks, and multiple stacks can depend on a single stack. Stacks that comprise multiple configuration items \(CIs\) and services make up the stack dependencies in the Cloud Services Catalog application. The dependency map provides a simple and detailed graphical representation of these complex settings. You can navigate through the references to understand the event impact that one branch has on another.

## Procedure

1.  On the Managed Stacks page, select a stack to open the stack operations page.

2.  On the View Full Details ribbon, select **View dependency**.

3.  In **Search for CI**, enter a CI to view the dependency map.

4.  On the form, fill in the fields.

    The following example shows the settings for viewing the stack dependencies. The settings include Save Custom Settings, Load Custom Settings, Predefined Filters, Dependency Type, and Max Levels.

    ![View of stack dependencies.](../image/viewing-stack-dependency.png "Viewing stacks dependencies")

5.  Undo all the CI filter selections and reset the map setting by selecting **Reset**.


**Parent Topic:**[Exploring the My Stacks tab](../concept/manage-stacks.md)

