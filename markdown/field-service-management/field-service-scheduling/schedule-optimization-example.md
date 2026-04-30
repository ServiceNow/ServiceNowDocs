---
title: Example- Schedule Optimization
description: This example shows three different ways admins can configure the optimization engine to schedule tasks.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Example- Schedule Optimization

This example shows three different ways admins can configure the optimization engine to schedule tasks.

Admins can configure Schedule Optimization to run overnight in batches to schedule a larger number of tasks or throughout the day at selected intervals based on events. Admins can also enable dispatchers to initiate Schedule Optimization from Dispatcher Workspace by configuring on-demand optimization.

In this example, the organization is ensuring that agents complete as many tasks as they can during their shift without spending a lot of time traveling between tasks. A policy is configured to maximize assignments and minimize travel time. On-demand optimization is enabled for the dispatchers who are assigned to this group of agents.

## Admin Core Configurations for Schedule Optimization

|Field|Value|
|-----|-----|
|Qualifier type for Schedule Optimization|Assignment Group|
|Number of seconds used for task scheduling resolution|1|
|Maximum number of location points allowed in a map provider call|300|

<table id="table_bfm_1xy_c1c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Maximum Assignments

</td></tr><tr><td>

Active

</td><td>

true

</td></tr><tr><td>

Constraints

</td><td>

Default values

</td></tr><tr><td>

Overall objectives

</td><td>

Maximize travel time \(weight 1\)

 Maximize task assignments \(weight 1\)

 Maximize assignments to earlier shifts \(weight 1\)

</td></tr></tbody>
</table>|Field|Value|
|-----|-----|
|Name|West coast config|
|Active|True|
|Travel estimate provider|Beans.ai|
|Default policy|Maximum Assignments|
|Straight line estimate config|West Coast|
|Tasks|State is one of: Pending dispatch or Scheduled|
|On Demand applicable policy|West Coast Dispatcher|

## Batch Optimization Configurations

|Field|Value|
|-----|-----|
|Name|West Coast weekly|
|Schedule start date|2023-12-01|
|Run frequency|Every 7 days|
|Batch start time|22:00|
|Batch end time|3:00|

|Field|Value|
|-----|-----|
|Name|West Coast-Next 7 days|
|Active|True|
|Scheduling attribute configuration|West Coast config|
|Rank|1|
|Assignment horizon offset|00|
|Assignment horizon range|Days 7|
|Optimization Batch|West Coast weekly|
|Start date|2023-12-01|
|Batch start time|22:00|
|Batch end time|3:00|
|Assignment group|San Diego North|

**Note:** Select schedule now when the form is complete

## Intraday Optimization Configurations

<table id="table_bgg_sxy_c1c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

West Coast

</td></tr><tr><td>

Active

</td><td>

True

</td></tr><tr><td>

Default scheduling attribute configuration

</td><td>

West Coast config

</td></tr><tr><td>

Default

</td><td>

False

</td></tr><tr><td>

Flow

</td><td>

Schedule intraday jobs \(default\)

</td></tr><tr><td>

Default processing window

</td><td>

Workday 9:00-5:00

</td></tr><tr><td>

Assignment group

</td><td>

San Diego South - Enable On Demand = True

 San Diego North - Enable On Demand = True

</td></tr></tbody>
</table>## On-demand Optimization configurations

|Field|Value|
|-----|-----|
|On Demand applicable policy|West Coast Dispatcher|

<table id="table_pxx_n1r_d1c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

San Diego South - Enable On Demand = True

 San Diego North - Enable On Demand = True

</td></tr></tbody>
</table>