---
title: Pass variables between tasks
description: Pass variables from one step of the fulfillment process to another.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Pass variables between tasks

Pass variables from one step of the fulfillment process to another.

## Before you begin

Role required: admin

## About this task

Variables can be processed by any workflow or execution plan that is associated with the requested items.

**Note:** To pass a variable between tasks, select the **Global** check box when you [create a Service Catalog variable](t_CreateAVariableForACatalogItem.md).

For example, consider the following tasks within the fulfillment process for a New PC catalog item.

## Procedure

1.  Procure a PC.

2.  Install corporate standard software.

3.  Set up email account.

4.  Deliver and set up PC for requester.

    Step 4 may require a piece of information from step 3 \(the email account credentials for setting up email on the PC\). If steps 3 and 4 are executed by different fulfillment groups, you can use variables to make this information visible in the tasks for steps 3 and 4. You can then pass the information between groups so that the second group can access the email account credentials.


**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

