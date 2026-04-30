---
title: Cost Management Demo Data
description: The demo data available with Cost Management provides samples of the data types to illustrate its use.
locale: en-US
release: xanadu
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# Cost Management Demo Data

The demo data available with Cost Management provides samples of the data types to illustrate its use.

Demo data should be loaded only in a development or test instance to prevent conflict with production data.

## High-Level Data Review

The Cost Overview module has a number of commonly requested reports.

![Business Service Overview](../image/FMBsOverview.jpg.png "Business Service Overview")

## Business Service Overview

The business service owner would like to know how much it costs to maintain the service over some period of time. This requires gathering the dependent CI costs and representing them at the business service level. For CI costs to roll up to business services, relationships must exist between CIs and services.

The demo data contains a number of services that have costs from their dependent CIs. In the **Cost Overview** homepage, the **Business Service Cost 12 Month** report shows an overview of this information:

![Cost Report](../image/FmBsCostGauge.jpg "Cost Report")

## Allocation Overview

Expense allocation rules costs allow you to allocate costs to one or more business entities such as a user, group, department, company, or cost center. The purpose of the allocation is to represent the cost that the business is responsible for. This is not considered charge-back or billing, but could be used as a source for billing. The primary purpose of expense allocation is to represent the consumer of the process that has incurred some expense.

The following diagram shows the distribution of expenses to cost centers.

![Report example](../image/FmExpAllocGauge.jpg "Report example")

## Budget Overview

The amount of money allocated to cost centers can be tracked against a planned budget. A budget represents a collection of cost centers, a duration, and the amount of money that is expected to be allocated to the cost centers during that period. The administration budget contains three cost centers and has incurred $173,610.83 so far during this period.

![Budget Demo](../image/FmBudgetDemo.jpg "Budget Demo")

**Parent Topic:**[Cost Management](../reference/r_CostManagement.md)

