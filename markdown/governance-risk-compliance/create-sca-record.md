---
title: Create a scenario analysis record using simulation
description: Create a Scenario analysis record to assess how a critical service performs under adverse conditions using statistical modelling. Use the guided Playbook experience to move through scoping, scenario selection, simulation, results review, and treatment decision.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-sca-record.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, Playbook, statistical modelling, create record]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a scenario analysis record using simulation

Create a Scenario analysis record to assess how a critical service performs under adverse conditions using statistical modelling. Use the guided Playbook experience to move through scoping, scenario selection, simulation, results review, and treatment decision.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_oper\_res.manager

## About this task

Users with the sn\_oper\_res.user role can view records and playbook stages in read-only mode. To create, edit, or progress an analysis, the sn\_oper\_res.manager or sn\_oper\_res.admin role is required. Scenario analysis runs only in Operational Resilience Workspace via the **Playbook** tab; there is no alternative form-based flow.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

    The Scenario Analyses list view in the Operational Resilience Workspace shows records in every state, including Draft and Completed. Default columns are Number, Name, Priority, State, and Owner. Select a record number \(for example, SA0001038\) to open the record detail.

    \[Omitted image "sca-list-view-all-scenario-analysis.png"\] Alt text: All scenario analysis list view with Number, Name, Priority, State, and Owner columns, showing Draft and Completed records.

2.  To create a scenario analysis record, select **New**.

    The Scenario Analysis form is displayed. You can fill in the form and create a Scenario Analysis record. For more information on the form, see [Create a scenario analysis record using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sca-record.md).

3.  Enter the name of the scenario analysis record in the **Name** field.

4.  Enter a description of the scenario context in the **Description** field.

5.  Enter a **Goal** statement that describes what the analysis aims to confirm.

6.  Assign an **Owner** for the scenario analysis.

    The creator of the scenario analysis is assigned as its owner. The form is shown in the example.

    \[Omitted image "sca-create-form-filled-method-profile.png"\] Alt text: Create New Scenario Analysis form with Method set to Statistical Modelling and the Annual loss model driven by risk events profile selected.

7.  Set the required **Method** field to one of the two available options.

    -   **Statistical Modelling** — Uses models and historical data to estimate outcome probabilities.

        **Note:** The **Statistical Modelling** method of scenario analysis is only available with the IRM Advanced license.

    -   **Manual** — Uses an SME-driven assessment template without simulation.
    **Note:** The **Method** field defines which of the two scenario analysis flows you use; it is a choice, not an optional step. Select **Statistical Modelling** for a Monte Carlo simulation, or **Manual** for a qualitative SME assessment.

    When you choose **Manual**, the **Statistical model profile** field is hidden, the playbook omits the Reference Data and Results steps, and the Scenario Testing step uses an SME-driven assessment template instead of a simulation. All other playbook steps are identical.

    **Statistical Modelling** is selected by default.

    Steps for using the simulation method are described in [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md). The manual method is described in [Run a scenario analysis using the manual method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/run-sca-manual-method.md).

8.  Verify that the **Annual loss model driven by risk events** is shown in the **Statistical model profile** field.

    The Statistical model profile is set by Operational Resilience and it controls how the simulation runs. It links an Annual loss model to the assessment question templates used to collect input parameters. One profile ships with the base system: **Annual loss model driven by risk events**. The profile links a risk-event reference table to the input and output assessment templates that the simulation uses.

    **Note:** The **Statistical model profile** field is a reference picker, not a drop-down. Only one profile can be selected per analysis.

9.  Select **Save**.

    The record is created in the **Draft** state and the selections are displayed in the **Details** tab.

10. Select the **Playbook** tab to begin the guided analysis.


## Result

The scenario analysis record is created and the **Playbook** tab is available to begin the guided analysis.

## What to do next

For defining the scope of scenario analysis, see [Define the scope and dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-scope-service-dep.md).

