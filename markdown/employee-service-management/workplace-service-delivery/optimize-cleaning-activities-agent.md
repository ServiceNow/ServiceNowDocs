---
title: Optimize cleaning activities agentic workflow
description: This team of workplace agents can find open maintenance cases and optimize it for workplace maintenance activities. These agents can optimize a maintenance case based on the utilization rate of a location for which a maintenance case is created.
locale: en-US
release: xanadu
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: concept
last_updated: "2025-08-20"
reading_time_minutes: 3
breadcrumb: [Optimize cleaning activities agent overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Optimize cleaning activities agentic workflow

This team of workplace agents can find open maintenance cases and optimize it for workplace maintenance activities. These agents can optimize a maintenance case based on the utilization rate of a location for which a maintenance case is created.

## Optimize cleaning activities agentic workflow overview

This AI agentic workflow enables Workplace teams to schedule and manage cleaning and other maintenance schedules based on space utilization and optimization. This agentic AI retrieves employee reservation data and visitor registration planned for a specific office location and date. It checks the minimum and maximum space utilization threshold to see if cleaning requests are required. It deactivates the cases when a location shows a minimum utilization threshold value \(below 40\). The agents optimize the cleaning schedule based on how workplace employees plan to use a space or location. It checks space wastage to provide the optimum workplace experience to employees. For more information, see [Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md).

## AI agents used in optimize cleaning activities workflow

Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**. Select **Optimize cleaning activities** from the list of available agentic AI workflows. The team of agents optimize a location based on the space utilization threshold. This team of agents fetch open maintenance cases and optimize it based on the utilization threshold rate. The optimization is done on the floor of a selected building autonomously by the agents and it doesn't require any approvals needed from a workplace user.

**Note:** Workplace Maintenance Managers \(sn\_wsd\_maintenance.manager\) and Workplace Maintenance Administrators \(sn\_wsd\_maintenance.admin\) can configure this agentic AI workflow.

<table id="table_cgv_crg_x2c"><thead><tr><th>

AI agent Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case aggregator AI agent

</td><td>

This agent fetches all the open maintenance cases based on the maintenance plan ID. Each workplace maintenance case represents a cleaning or a maintenance case for a location for a scheduled interval. The optimization is done on a floor of a selected building. It fetches all the maintenance plan records that satisfy certain criteria. For example, it fetches a set of maintenance plans, and looks for cases that are open for the next 48 hours. The state of the cases should be in **Draft**, **Ready**, or **Awaiting for approval**. For more information, see [Create and publish maintenance plans](../../workplace-maintenance-management/task/create-publish-maintenance-plans.md).

This agent also considers workplace reservations on a floor. If a case is opened for washroom maintenance, the agent identifies the floor on which the washroom is located. It also considers the number of workplace reservations, visitor registrations, and permanent seat assignments before retrieving the space optimization threshold value.

</td></tr><tr><td>

Utilization rate AI agent

</td><td>

This agent can take a list of available maintenance cases to calculate the utilization rate for each case. This utilization rate is used to optimize the cases. It uses the Utilization rate calculator to calculate the utilization rate.

</td></tr><tr><td>

Case Optimizer AI agent

</td><td>

The Case Utilization Optimizer analyzes cases grouped by location, schedule type, and date to optimize resource utilization. It confirms cases stay within defined utilization thresholds by creating cases when utilization is too high and deactivating underutilized cases.

</td></tr></tbody>
</table>## Case Optimizer AI Agent

The Case Optimizer AI Agent analyzes cases grouped by location, schedule type, and date to optimize resource utilization. It verifies that maintenance cases stay within the defined utilization thresholds. It creates maintenance cases when the utilization threshold is too high. When the utilization threshold is low, it deactivates the maintenance cases for underutilized floors. While deactivating a maintenance case, this agent ensures minimum case availability for each maintenance schedule group. It retains at least one maintenance case before deactivating all underutilized maintenance cases. The output from the Utilization rate AI agent is given as input to this agent for space optimization.

## Case Aggregator AI Agent

This agent gets all open maintenance cases based on the maintenance plan Id. Each workplace maintenance case represents a cleaning or a maintenance case on a location for a certain time interval, also known as schedule. This agent fetches the open maintenance cases \(maintenance plan record IDs\) in the maintenance management system.

## Utilization rate AI Agent

This agent can take a list of maintenance cases available and calculate the utilization rate of each case. This utilization rate is used to optimize the cases. This agent takes a list of maintenance cases as input and calculates the utilization rate for locations for a given schedule.

