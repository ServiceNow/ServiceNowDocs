---
title: Start simulation and run scenario testing
description: Complete the simulation assessment questionnaire to provide the statistical model with the input values required to run the simulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/complete-sca-scenario-testing.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, scenario testing, simulation assessment, Annual Loss Model, Start Simulation]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Start simulation and run scenario testing

Complete the simulation assessment questionnaire to provide the statistical model with the input values required to run the simulation.

## Before you begin

Role required: **sn\_oper\_res.admin**, **sn\_oper\_res.manager**

## About this task

A Simulation Assessment record is generated automatically for the selected service. The assessment is owned by the analyst or subject-matter expert assigned to complete it. The assessment opens with the **Scenario Understanding** section, which collects the input values required by the statistical model.

**Note:** This task describes the **Statistical Modelling** method. If the scenario analysis uses the **Manual** method, the **Scenario Testing** step presents an SME assessment template instead of a simulation, and the playbook omits the **Reference Data** and **Results** steps. For more information, see [Scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-ov.md).

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Scenario Analysis** and open the Scenario Analysis record form.

2.  In the Playbook stage panel, select **Scenario Testing**.

    The Smart Assessment template card opens up.

3.  Select the **Simulation Assessment** card for the service.

    The **Simulation Assessment** card is shown in the example.

    \[Omitted image "sca-input-assessment-card-progress.png"\] Alt text: Simulation Assessment card.

    The Simulation Assessment opens.

4.  Answer all required questions in the assessment.

    The Input assessment is shown in the example.

    \[Omitted image "sca-input-questionnaire-questions.png"\] Alt text: Simulation assessment input form.

    **Note:** If required questions are unanswered, Submit is blocked and validation highlights the missing answers.

    -   **Q1** — How many simulation runs are required? \(Simulation count input; default 100,000; back-filled by System.\)
    -   **Q2** — How many loss incidents do you expect to occur over the chosen time horizon \(typically one year\)? \(Lambda — frequency input.\)
    -   **Q3** — What is the typical financial loss per incident over the chosen time horizon? \(Severity Mu — mean severity input.\)
    -   **Q4** — What are the variable losses \(sigma\)? \(Severity Sigma — standard deviation of severity.\)
    -   **Q5** — What is the minimum credible financial loss that could result from a single incident? \(Min loss.\)
    -   **Q6** — What is the maximum credible financial loss that could result from a single incident? \(Max loss.\)
    -   **Q7** — What level of financial impact can the service tolerate? \(Loss tolerance; sourced from the linked service's impact tolerance and may display as 0 until the service tolerance is set.\)
    -   **Q8** — What is the selected percentile for tail risk metrics to be calculated in the output? \(Selected percentile, for example 90% or 99%.\)
5.  Select **Submit** on the Input questionnaire.

    A confirmation dialog opens.

6.  Select the confirmation check box, then select **Submit** to commit the answers.

    A **Successfully submitted** success dialog confirms that the questionnaire is saved.

    \[Omitted image "sca-input-questionnaire-submit-confirmation.png"\] Alt text: Submit confirmation dialog and Cancel and Submit buttons. \[Omitted image "sca-input-questionnaire-success.png"\] Alt text: Success dialog with a green check mark and the message 'Successfully submitted. The sample has been successfully processed.'

7.  Return to the **Scenario Testing** step and select **Start Simulation**.

    **Note:** The **Start Simulation** button is enabled only when all Simulation Assessment cards on the **Scenario Testing** step show Completed status. Before attempting to start the simulation, you must complete and submit the assessment.

    The simulation runs and results are returned before you can proceed. After the simulation run, a success banner **Simulation Completed Successfully** is displayed, the **Mark as complete** button on the Scenario Testing card becomes enabled, and the result values are written to the output assessment shown on the Results step. The **Reopen Assessment** button remains visible so that you can change input answers and rerun the simulation any number of times before you select **Mark as complete**.

    \[Omitted image "sca-scenario-testing-simulation-completed.png"\] Alt text: Scenario Testing step after Questionnaire is submitted, showing the Simulation Assessment card, the Reopen Assessment button, the Start Simulation button enabled, and Mark as Complete button visible but inactive.

8.  Select **Reopen Assessment** to reopen the assessment.

9.  Select **Mark as complete** to mark the scenario testing step as complete.


## Result

The simulation assessment is submitted and the simulation is running. Results are available in the **Results** step when the simulation completes. For information on reviewing results and making a treatment decision, see [Review results and decide the treatment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/review-sca-results-treatment-decision.md).

