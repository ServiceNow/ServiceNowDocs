---
title: Set the default notice period for the Manage contract repository agentic workflow
description: Configure system properties to set the default notice period for the Manage contract repository agentic workflow.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Set the default notice period for the Manage contract repository agentic workflow

Configure system properties to set the default notice period for the Manage contract repository agentic workflow.

## Before you begin

Role required: sn\_cm\_core.contract\_admin or sn\_cm\_core.contract\_config

## About this task

When the contract renewal notice period and termination of contract renewal notice period are not available in a contract, the Manage contract repository agentic workflow uses the default notice period along with other contract details to set the contract milestone reminders.

**Note:** The default notice period in the base system is 60 days.

## Procedure

1.  Navigate to the **All** menu and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  In the Name column, search for `sn_cm_gen_ai.contract_notice_period_in_days`.

3.  Select the **sn\_cm\_gen\_ai.contract\_notice\_period\_in\_days** property.

4.  Update the **Value** field to set the default notice period.

    The default value is **60**.

5.  Select **Update**.


**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

