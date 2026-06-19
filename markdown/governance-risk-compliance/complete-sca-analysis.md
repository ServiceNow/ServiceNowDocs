---
title: Mark the scenario analysis as complete
description: Complete the Scenario analysis after all required playbook steps are finished to lock the record and make the results available for reporting and governance review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/complete-sca-analysis.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Scenario Analysis, Operational Resilience, complete analysis, governance, reporting]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Mark the scenario analysis as complete

Complete the Scenario analysis after all required playbook steps are finished to lock the record and make the results available for reporting and governance review.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

The **Complete analysis** button is active only after all required steps are marked complete. Optional steps **Operational Vulnerabilities** and **Issues** do not block completion.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

2.  Confirm that all required steps show a completed status in the stage panel.

    The example shows a record with all the steps completed.

    \[Omitted image "sca-complete-analysis-button-active.png"\] Alt text: Scenario Analysis header with the Complete analysis button enabled and stages marked complete in the stage panel.

    **Note:** The **Complete analysis** button is active only when all required steps are marked complete. The optional **Operational Vulnerabilities** and **Issues** steps do not block completion.

3.  Select **Complete analysis** in the top-right of the form.

    To capture additional vulnerabilities or issues for the same scope after completion, you can create them directly from the Operational Vulnerabilities or Issues list in the workspace and link them back to this scenario analysis using the **Source record** field.

    An information banner `Scenario Analysis successfully completed` is displayed at the top of the record. The record state transitions to **Completed**. The **Operational Vulnerabilities** and **Issues** steps remain visible in read-only mode after completion; the **New**, **Add**, and **Mark as complete** actions on those steps are removed.

    \[Omitted image "sca-all-stages-complete-state.png"\] Alt text: Scenario analysis record with every stage in the stage panel showing the Complete badge after the analysis is completed.


## Result

The Scenario analysis record is complete. Simulation results, treatment decision, and any captured vulnerabilities or issues are saved to the record and available for reporting and governance review in Operational Resilience Workspace. The **Operational Vulnerabilities** and **Issues** stages remain visible in read-only mode after completion; you cannot add new vulnerabilities or issues from the playbook after the record reaches the **Completed** state.

