---
title: Field Service Agent Efficiency components
description: Several types of components are installed with the Field Service Agent Efficiency feature, including tables, roles, script includes, and business rules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Agent Efficiency components

Several types of components are installed with the Field Service Agent Efficiency feature, including tables, roles, script includes, and business rules.

## Tables

Field Service Agent Efficiency adds the tables listed in the following table.

<table id="table_sl2_2jr_gdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent efficiency determination rulesn\_agent\_effcy\_det\_rule

</td><td>

Stores information about determination rules and conditions to define the Agent Efficiency criteria for work order tasks.

</td></tr><tr><td>

Agent efficiency criteriasn\_agent\_effcy\_criteria

</td><td>

Stores information about Agent Efficiency criteria and the table to which they are applicable.

</td></tr><tr><td>

Agent efficiency valuesn\_agent\_effcy\_value

</td><td>

Stores information about Agent Efficiency for various criteria.

</td></tr></tbody>
</table>## Roles

Field Service Agent Efficiency adds the roles listed in the following table.

<table id="table_ifv_gnr_gdc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Efficiency Managersn\_agent\_efficiency\_manager

</td><td>

Define and update Agent Efficiency values for agents.

</td></tr><tr><td>

Agent Efficiency Readsn\_agent\_efficiency\_read

</td><td>

View efficiency determination rules, Agent Efficiency criteria, and Agent Efficiency values.

</td></tr><tr><td>

Agent Efficiency Adminsn\_agent\_efficiency\_admin

</td><td>

Create and update Agent Efficiency criteria, efficiency determination rules, and Agent Efficiency values.

</td></tr></tbody>
</table>## Script Includes

Field Service Agent Efficiency adds the script includes listed in the following table.

<table id="table_irp_2ls_gdc"><thead><tr><th>

Script include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

FSMAgentEfficiencyCalculatorImpl

</td><td>

Field Service Agent Efficiency calculator implementation for FSMAgentEfficiencyCalculatorExtPnt.

</td></tr><tr><td>

FSMAgentEfficiencyCalculatorImplSNC

</td><td>

Verifies whether Field Service Agent Efficiency has been activated, and calculates and updates work duration based on the Agent Efficiency value.

</td></tr><tr><td>

FSMAgentEfficiencyConstants

</td><td>

Holds constants for Field Service Agent Efficiency.

</td></tr><tr><td>

FSMAgentEfficiencyUtil

</td><td>

Contains a customized script to fetch Field Service Agent Efficiency criteria and values.

</td></tr><tr><td>

FSMAgentEfficiencyUtilSNC

</td><td>

Contains default methods to fetch Field Service Agent Efficiency criteria and values.

</td></tr><tr><td>

FSMAgentEfficiencyValidatorImpl

</td><td>

Validates Field Service Agent Efficiency determination rules, criteria, and values.

</td></tr><tr><td>

MatchingDimensionAgentEfficiency

</td><td>

Contains a custom script to rank agents by their efficiency and assign work order tasks for Dynamic Scheduling.

</td></tr></tbody>
</table>## Business Rules

Field Service Agent Efficiency adds the business rules listed in the following table.

<table id="table_sym_hqs_gdc"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate Agent Efficiency Record

</td><td>

Agent efficiency value \[sn\_agent\_effcy\_value\]

</td><td>

Validates Field Service Agent Efficiency criteria and values.

</td></tr><tr><td>

Validate criteria changes

</td><td>

Agent efficiency criteria\[sn\_agent\_effcy\_criteria\]

</td><td>

Validates updated Agent Efficiency criterion.

</td></tr><tr><td>

Validate determination rule changes

</td><td>

Agent efficiency determination rule\[sn\_agent\_effcy\_det\_rule\]

</td><td>

Validates Agent Efficiency determination rules.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

