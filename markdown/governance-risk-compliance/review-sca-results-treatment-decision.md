---
title: Review results and decide the treatment
description: Review the simulation output metrics, then select a treatment strategy to address the identified risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/review-sca-results-treatment-decision.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Scenario Analysis, Operational Resilience, simulation results, treatment decision, Accept, Mitigate, Avoid, Transfer]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Review results and decide the treatment

Review the simulation output metrics, then select a treatment strategy to address the identified risk.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

The **Results** step surfaces the quantitative output of the simulation. Review the metrics to assess whether losses breach the service's impact tolerances before selecting a treatment strategy. The **Treatment Decision** step is available after results are marked complete.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

2.  In the Playbook stage panel, select **Results**.

3.  Under the **Simulation Results** tab, select the **Simulation Output** card.

    The **Simulation Results** tab displays one row per scenario, with columns for Simulation Status, Net Loss Tolerance, and Findings. Select a scenario row to open the Simulation Output detail view, which shows the full set of computed metrics per scenario: Average Annual Loss, Typical \(Midpoint\) Annual Loss, Variation \(Std Deviation\), 90th/95th/99th Percentile Loss, Tail Risk Average, and Probability of exceeding loss tolerance.

    \[Omitted image "sca-results-output-questions-with-values.png"\] Alt text: Simulation assessment output for the annual loss model showing numbered questions with computed values pre-filled.

    The output assessment displays each metric in a numbered question format with the computed value pre-filled, including **Average Annual Loss**, **Typical \(Midpoint\) Annual Loss**, **Variation \(Std Deviation\)**, **90th Percentile Loss**, **95th Percentile Loss**, **99th Percentile Loss**, **Tail Risk Average**, and **Probability of exceeding loss tolerance**.

4.  Assess whether losses breach the impact tolerances set on the selected service, then select **Mark as complete**.

    **Note:** Until you select **Mark as complete** on this step, you can return to **Scenario Testing** and re-enter different values. Once this step is marked complete, the simulation inputs are locked.

    The **Results** step shows a completed status in the stage panel.

    \[Omitted image "sca-results-stage-complete-state.png"\] Alt text: Results step in the Complete state with the simulation output card showing Completed and the linked output assessment template.

5.  In the Playbook stage panel, select **Treatment Decision**.

    The simulation results, including the **Probability of exceeding loss tolerance**, are visible on this step to inform your decision.

6.  On the Treatment Decision step, select one of the four treatment-strategy cards.

    -   **Accept** — Proceed as-is when the risk is low or within tolerance.
    -   **Mitigate** — Reduce likelihood or impact through controls and improvements.
    -   **Avoid** — Eliminate the risk entirely when impact is unacceptable.
    -   **Transfer** — Shift the risk to a third party, for example through insurance or outsourcing.
    \[Omitted image "sca-treatment-decision-cards.png"\] Alt text: Treatment Decision step with four selectable cards — Accept, Mitigate, Avoid, Transfer — and the required Reason text field.

7.  Enter a **Reason** for the selected treatment.

8.  Select **Mark as complete**.

    The **Treatment Decision** step shows a completed status in the stage panel. The optional **Operational Vulnerabilities** and **Issues** steps are now available. An information banner is displayed at the top of the record: `Navigate to the Operational Vulnerabilities and Issues steps to complete the Scenario Analysis`. A **Complete analysis** button also appears in the form so that the analysis can be closed without recording vulnerabilities or issues.

    \[Omitted image "sca-treatment-decision-completion-notification.png"\] Alt text: Scenario analysis record after Treatment Decision is marked complete, showing the navigation banner and the Complete analysis button.


## Result

The simulation results have been reviewed and a treatment decision has been recorded. The optional **Operational Vulnerabilities** and **Issues** steps are now available. For more information on adding operational vulnerabilities and issues, see [Log operational vulnerabilities and issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-op-vul-and-issues.md).

