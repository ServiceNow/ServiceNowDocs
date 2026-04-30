---
title: Configuring denormalized tables in Field Service Management
description: Denormalized databases collapse information stored in multiple tables into a single table. This collapsing of relevant data improves Field Service Management load time.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Configuring denormalized tables in Field Service Management

Denormalized databases collapse information stored in multiple tables into a single table. This collapsing of relevant data improves Field Service Management load time.

## Data in Field Service Management

The data for Field Service Management is typically stored in a normalized database. In normalized databases, tables can extend other tables, creating parent tables and child tables. The Field Service Management normalized databases use tables and records to manage data and processes, such as work orders, agents, and equipment. This normalized data structure that stores and organizes information is helpful for humans to add and manage the data in the tables, but it’s not the quickest or most efficient way for computers to process the data in the tables.

## Denormalized tables

Denormalized databases collapse multiple tables into a single table, taking what was once in multiple table cells across multiple tables and puts them into one table. This collapsing of relevant data from multiple tables rows allows Field Service Management to query and return information faster since the data being fetched can be accessed from a single table instead of multiple tables.

## Denormalized tables in Field Service Management

The way that denormalized tables work for Field Service Management, is when you load an application like Dispatcher Workspace, all of the tables used to retrieve data from are queried up front and the information is stored in a denormalized table. Then when you’re working in Dispatcher Workspace, when information is needed to execute a request, the denormalized table is queried, instead of the multiple tables that were necessary to query before. If the necessary data is not present in the denormalized table, then the data is retrieved from the original table source.

Denormalized tables just make it easier for information to be delivered to dispatchers. The way you add data and manage tables in Field Service Management remains the same. There is no change to how you update or add information to tables.

When data is added to denormalized tables, the process is divided into 4 jobs. For example, if you have 1600 agents the processing of those agent's data will be divided into four jobs each with 400 agents. You can change the number of jobs that process data, but you must contact ServiceNow to do this.

You can change the number of weeks' worth of data that's stored in denormalized tables. For more information, see [Update the data stored in denormalized tables](../task/denormalized-data-weeks.md). For information related to the data model used to create denormalized tables, see [Data model for denormalized tables in Field Service Management](../reference/flat-table-model.md).

The following features use denormalized tables:

-   Appointment booking
-   Dynamic scheduling
-   Dispatcher Workspace

**Important:**

Never change any of the data directly in a denormalized table. This can cause Field Service Management to break and should never be performed, even by a professional developer.

## Denormalized table properties

There are three system properties that control table denormalization for Field Service Management. For more information, see the properties listed below on [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).

Denormalized tables are enabled by default. You must disable the property sn\_fsm.wm\_weekly\_resource\_span to turn off denormalized tables.

**Warning:** Only system administrators should change these values.

-   sn\_fsm.wm\_weekly\_resource\_span
-   sn\_fsm.wm\_weekly\_resource\_span.number\_of\_ weeks\_in\_past
-   sn\_fsm.wm\_weekly\_resource\_span.number\_of\_weeks\_in future

