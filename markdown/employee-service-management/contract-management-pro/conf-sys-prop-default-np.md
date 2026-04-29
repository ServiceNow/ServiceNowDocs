---
title: Set the default notice period for the Manage contract repository agentic workflow
description: Configure system properties to set the default notice period for the Manage contract repository agentic workflow.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    ![Default value for agentic AI notice period.](../image/cmpro-agentic-ai-dft-np.png "System property for default notice period")

5.  Select **Update**.


## Result

The Manage contract repository agentic workflow uses the set value as default notice period when the contract renewal notice period and termination of contract renewal notice period are not available in a contract.

**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

**Related topics**  


[Activate business rules for the Manage contract repository agentic workflow](conf-repository-agentic-ai.md)

[Update the contracts AI agents handler script include](cmpro-script-includ-agenticAI.md)

[Enable notifications for AI extracted metadata and obligations](cmpro-na-me-agentic-ntf.md)

