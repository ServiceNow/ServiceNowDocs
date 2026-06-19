---
title: Run a scenario analysis using the manual method
description: Run a scenario analysis on subject-matter-expert \(SME\) judgment instead of statistical simulation. The manual method reuses the guided playbook but omits the Reference Data step and the quantitative Results step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/run-sca-manual-method.html
release: australia
topic_type: task
last_updated: "2026-05-31"
reading_time_minutes: 4
keywords: [Scenario Analysis, Operational Resilience, manual method, SME assessment, Scenario analysis manual template]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Run a scenario analysis using the manual method

Run a scenario analysis on subject-matter-expert \(SME\) judgment instead of statistical simulation. The manual method reuses the guided playbook but omits the **Reference Data** step and the quantitative **Results** step.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

Use the manual method when a quantitative financial-loss projection is not required and an SME records the impact of a scenario qualitatively. When you set the **Method** field to **Manual**, the analysis uses an SME assessment template instead of a statistical simulation. The **Scope**, **Scenarios**, **Treatment Decision**, **Operational Vulnerabilities**, and **Issues** steps are the same as in the statistical modelling flow. The method is a choice you make on the **Details** tab when you create the scenario analysis record; it is not an extra step in the flow. Choose **Statistical Modelling** or **Manual** based on your requirement. For the statistical modelling flow, see [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md).

**Note:** The manual method omits the **Reference Data** step and the quantitative **Results** step. Because the answers are entered manually and no simulation runs, the manual method does not produce calculated financial-loss metrics. For an overview of both methods, see [Scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-ov.md).

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and create a scenario analysis record.

2.  On the **Details** tab, enter a **Name**, **Description**, and **Goal** for the analysis.

3.  Set the **Method** field to **Manual**.

    When you select the manual method, the base system **Scenario analysis manual template** is populated as the assessment template. You can select your own published template instead.

4.  Select **Save**.

    The record is saved and the playbook experience opens at the **Scope** step.

5.  On the **Scope** step, add the critical business service to analyze, and then select **Mark as complete**.

    **Note:** Only one service can be added per scenario analysis in this release. After you mark the step complete, the scope is locked.

6.  On the **Dependencies** step, add the dependencies to include, and then select **Mark as complete**.

    You can add dependencies that are related to the service in scope, or add other dependencies that are not in scope. After you mark the step complete, the selected dependencies cannot be changed.

7.  On the **Scenarios** step, add one or more scenarios to test, and then select **Mark as complete**.

    **Note:** The manual method does not include a **Reference Data** step. After you complete the **Scenarios** step, the playbook moves directly to **Scenario Testing**.

8.  On the **Scenario Testing** step, open the manual assessment template and answer the questions.

    The base system **Scenario analysis manual template** groups its questions into the following sections:

    -   **Services and Dependencies** — Service impact and criticality, and dependencies and infrastructure, including single points of failure.
    -   **Preparedness &amp; Response** — Whether defined rules, backups, and remote-working capabilities exist.
    -   **Impact Analysis** — Financial, transaction, customer, duration, and reputational impact.
    -   **Business Continuity and Disaster Recovery** — Continuity and recovery readiness. These questions apply when the BCM workspace is added.
9.  Select **Submit**, and then select **Mark as complete** on the **Scenario Testing** step.

    **Note:** No simulation runs for the manual method, and no quantitative **Results** step is presented. The playbook moves directly to **Treatment Decision**.

10. On the **Treatment Decision** step, select a risk response, enter the mandatory reason, and then select **Mark as complete**.

    Select a response of **Accept**, **Mitigate**, **Avoid**, or **Transfer**. A reason is required before you can complete the step.

11. Log any operational vulnerabilities and issues that are identified during the analysis.

    On the **Operational Vulnerabilities** and **Issues** steps, create the records you want to associate with the analysis, or skip the steps. These steps remain editable until you complete the analysis.

    **Note:** Skipping the optional step does not affect the analysis completion.

12. Select **Complete analysis**, and then confirm.

    The record moves to the **Completed** state and the whole record becomes read-only.


## Result

The scenario analysis is complete and recorded with the SME assessment and treatment decision. Because the manual method does not run a simulation, the analysis does not include calculated financial-loss metrics. For information about the statistical modelling method, see [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md).

