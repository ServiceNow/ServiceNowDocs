---
title: Create Scenario Analysis form
description: Use the Create Scenario Analysis form using Playbooks in Operational Resilience Workspace. Enter the details of a scenario analysis, such as its name, goal, method, and owner, before running the guided playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-sca-record-form.html
release: australia
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 1
breadcrumb: [Create a scenario analysis record using simulation, Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Scenario Analysis form

Use the Create Scenario Analysis form using Playbooks in Operational Resilience Workspace. Enter the details of a scenario analysis, such as its name, goal, method, and owner, before running the guided playbook.

## Create Scenario Analysis form

For a description of the field values, see the following table.

<table id="table_CreateScaForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Scenario analysis panel

</td></tr><tr><td>

Number

</td><td>

Unique identification number of the scenario analysis. When you create a scenario analysis record, the application assigns a unique number, for example, SA0001038. This field is auto-filled.

</td></tr><tr><td>

Name

</td><td>

Name of the scenario analysis.

</td></tr><tr><td>

State

</td><td>

State of the scenario analysis record. A new record is created in the **Draft** state and changes to **Completed** when you mark the analysis complete. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Description of the scenario context for the scenario analysis.

</td></tr><tr><td>

Goal

</td><td>

Specific goal that the analysis aims to confirm. For example, your goal might be to understand the different levels of impact that flooding could have on a critical service.

</td></tr><tr><td>

Method

</td><td>

Method used to run the scenario analysis. This field is required and determines the rest of the playbook flow. Select one of the following options:-   **Statistical Modelling** — Uses a model and historical data to estimate outcome probabilities. This is the default option.
-   **Manual** — Uses a subject-matter-expert \(SME\) assessment template without simulation. When you select **Manual**, the **Statistical model profile** field is hidden and the playbook omits the Reference Data and Results steps.

</td></tr><tr><td>

Statistical model profile

</td><td>

Profile that controls how the simulation runs. This field is displayed only when **Method** is set to **Statistical Modelling**. The profile links an Annual loss model to the input and output assessment templates that the simulation uses. One profile ships with the base system: **Annual loss model driven by risk events**. This field is a reference picker, and only one profile can be selected per analysis.

</td></tr><tr><td>

Owner

</td><td>

Owner of the scenario analysis. By default, the user who creates the record is assigned as its owner.

</td></tr></tbody>
</table>