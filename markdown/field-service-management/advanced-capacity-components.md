---
title: Capacity and Reservations Management components
description: Several types of components are installed with the Advanced Capacity and Reservations Management feature, including tables, and script includes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/advanced-capacity-components.html
release: australia
product: Field Service Management
classification: field-service-management
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations components, Components installed with additional plugins, Reference, Field Service Management]
---

# Capacity and Reservations Management components

Several types of components are installed with the Advanced Capacity and Reservations Management feature, including tables, and script includes.

## Tables

Advanced Capacity and Reservations Management adds table listed below.

<table id="table_h1q_d3c_vmb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory Resource Demand Channel\[wm\_terr\_res\_demand\_channel\]

</td><td>

Stores resource and demand channel association details including recurrence and time period for a technician for the specified territory. This information is used while either manually or automatically assigning a task to a technician.

</td></tr></tbody>
</table>## Roles

The Advanced Capacity and Reservations Management adds the role listed in the following table. To find them, navigate to **All** &gt; **Roles**.

|Roles|Description|
|-----|-----------|
|fsm\_adv\_cap\_mgmt.wm\_capacity\_planner|Provides read, write, and create access to capacity-related tables, along with access to the Capacity Console.|

## Script includes

The Advanced Capacity and Reservations Management adds the script includes listed in the following table. To find them, navigate to **All** &gt; **Script Includes**

|Name|Description|
|----|-----------|
|CapacityConsoleConstants|Aggregate all constants in one place for the Capacity Console. Customers can override constants from `CapacityConsoleConstantsSNC`.|
|CapacityConsoleConstantsSNC|Aggregate all constants in one place for the Capacity Console.|
|CapacityConsoleData|Contains all the business logic for the Capacity Console. Customers can override this logic using `CapacityConsoleDataSNC`.|
|CapacityConsoleDataSNC|Contains all the business logic for the Capacity Console.|
|CapacityConsoleUtil|Contains all utility functions for the Capacity Console.|
|CapacityConsoleUtilSNC|Contains all utility functions for the Capacity Console.|
|FSMCapacityAdvancedFilterDefinition|Custom implementation of all advanced filters used in the Capacity Console.|

## Configuration

The Advanced Capacity and Reservations Management adds the configuration listed in the following table. To find it, navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**

|Configuration|Description|
|-------------|-----------|
|Enable/disable association of territory resources with demand channel|Allows you associate technicians with demand channels for appropriate assignment of tasks. This configuration is applicable only when Territory model and Workforce Optimization is enabled.|

## Scheduled job

The Advanced Capacity and Reservations Management adds the scheduled job listed in the following table. To find it, navigate to **All** type `sysauto_script.list` and press Enter.

|Scheduled job|Description|
|-------------|-----------|
|FSM Resource Demand Channel Migration - On Demand|Run this scheduled job optionally to associate technicians with demand channels.|

**Parent Topic:**[Field Service Capacity and Reservations Management components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/capacity-management-components.md)

