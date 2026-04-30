---
title: Plan Template form
description: Use the Plan Template form in BCM UIB Workspace to input details regarding the business continuity plan.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the BCP template, Configuring plan template, Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Plan Template form

Use the Plan Template form in BCM UIB Workspace to input details regarding the business continuity plan.

## Plan Template form

For the description of the field values, see the table.

<table id="table_kbt_tw4_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the plan template. For example, Workplace Recovery Plan.

</td></tr><tr><td>

Description

</td><td>

Brief description about the plan template.

</td></tr><tr><td>

Primary Element Recovered

</td><td>

Primary object type or an element identified to be recovered in the plan. For example, Locations.

</td></tr><tr><td>

Plan authoring type

</td><td>

Various stages or sections of a plan that you can choose from when creating a continuity plan with this template. These choices appear as tabs in the BCP workspace as you advance through the process of filling in the plan details.-   **All** \(Default\): All choices such as Documentation, Loss Scenarios, Recovery Tasks, and Recovery Teams are presented in the plan that uses this template. These options are visible as tabs within the workspace.
-   **Documentation**: Plan that uses this template shows the documentation option alongside chosen dependencies. The documentation tab, and tabs for recovery tasks and recovery teams, are accessible for viewing in the workspace.
-   **Loss Scenarios**: Loss scenarios together with recovery tasks, recovery teams, and other chosen dependencies in the plan that uses this template.
-   **Recovery tasks**: Recovery tasks and recovery teams associated with the plan type that uses this template.

</td></tr><tr><td>

Document sections

</td><td>

Documentation sections to be included in the plan. Available options are:-   **BCP-Assumptions**
-   **BCP-Objectives**
-   **BCP-Scope**
-   **BIA-Overview**
-   **SN-BCP Checklist**
-   **SN-Overview**

</td></tr><tr><td>

Loss scenarios

</td><td>

Loss scenarios to be included in the plan. Available options are:

-   **Loss of facilities housing critical comp**
-   **Loss of Linux Servers**
-   **Loss of Datacenters**
-   **Loss of Workplace**
-   **Loss of Business Applications**
-   **Loss of Personnel**
-   **Vendor Disruption**
-   **Loss of Windows Servers**

 You can also create a loss scenario and add it to the template. For more information on creating a loss scenario, see [Add loss scenarios](../task/add-loss-scenario-recovery-task-bcp-uib-ws.md).

</td></tr><tr><td>

Group recovery tasks

</td><td>

Option to group recovery tasks. When selected, tasks are pre-organized into groups based on the chosen **Group by** criteria values. Available options are:-   **Assignment group**
-   **Automated flow**
-   **Completion deadline**
-   **Configuration item**
-   **Created by**
-   **Description**
-   **Documentation**
-   **Plan**
-   **Owner**
-   **Recovery strategy**
-   **Recovery team**
-   **Related plan**
-   **Scope**
-   **Short description**
-   **Tag**
-   **Tag assets**
-   **Task classification**
-   **Task group**
-   **Updated by**

</td></tr></tbody>
</table>**Parent Topic:**[Configure the business continuity plan template](../task/configure-a-bcp-template-uib-ws.md)

