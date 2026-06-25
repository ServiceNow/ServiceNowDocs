---
title: Building a scenario analysis using simulation
description: Use the scenario analysis process to assess how critical services perform under adverse conditions using statistical simulation. Starting with Operational Resilience, version 22.3.1, Operational Resilience application, you can follow a guided playbook to perform a scenario analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/scenario-analysis-playbook-experience.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
keywords: [Scenario Analysis, Operational Resilience, Playbook, statistical modelling, Annual Loss Model, Statistical Model Profile, simulation, treatment decision, lifecycle event]
breadcrumb: [Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Building a scenario analysis using simulation

Use the scenario analysis process to assess how critical services perform under adverse conditions using statistical simulation. Starting with Operational Resilience, version 22.3.1, Operational Resilience application, you can follow a guided playbook to perform a scenario analysis.

The playbook flow guides you from scoping a service and dependencies through to a treatment decision and, optionally, logging vulnerabilities and issues.

**Note:** For the objectives, benefits, and known limitations of advanced scenario analysis, see [Scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-ov.md).

Each scenario analysis runs in one of two methods, set in the **Method** field on the record:

-   **Statistical Modelling** — Default. Runs the simulation as described in [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md).
-   **Manual** — Uses an SME-driven assessment template on the Scenario Testing step instead of a simulation as described in [Run a scenario analysis using the manual method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/run-sca-manual-method.md). Omits the Reference Data and Results steps. All other playbook steps \(Scope, Scenarios, Treatment Decision, Operational Vulnerabilities, Issues\) are identical.

## Playbook interface

When you open a scenario analysis record in Operational Resilience Workspace, the **Playbook** tab appears in the form. This tab is the primary interface for running the complete scenario analysis.

|UI Component|Description|
|------------|-----------|
|**Playbook** tab|Tab displayed in the form when a Scenario Analysis record is opened in Operational Resilience Workspace. This is the primary interface for running the end-to-end analysis.|
|Playbook header|Title of the current activity set. A check mark inside the header indicates the activity set is complete.|
|Stage panel|Panel located on the Playbook form that displays the full list of playbook steps. For each step, the number of activities completed and a status circle is displayed. A check inside the circle indicates that step is complete.|
|Activity stream|Content area displayed when a step is selected in the stage panel. Each step surfaces its own content, including a service selector, dependency list, scenario picker, reference data, simulation assessments, and results.|

## Steps for scenario analysis

The scenario analysis playbook contains required and optional stages. Scenario testing consists of two sub-steps — Input Assessment and Results — that appear as separate items in the stage panel. You must complete both before the playbook advances to Treatment decision.

The playbook guides you through the following steps:

1.  Create a scenario analysis record \([Create a scenario analysis record using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sca-record.md)\)
2.  Add service and dependencies as part of the scope: \([Define the scope and dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-scope-service-dep.md)\)
3.  Add scenarios and review reference data \([Add scenarios and review reference data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-scenarios-review-refdata.md)\)
4.  Complete scenario testing \([Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md)\)
5.  Review results and make a treatment decision \([Review results and decide the treatment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/review-sca-results-treatment-decision.md)\)
6.  Log operational vulnerabilities and issues \(optional\) \([Log operational vulnerabilities and issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-sca-op-vul-and-issues.md)\)
7.  Complete the scenario analysis \([Mark the scenario analysis as complete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-analysis.md)\)

The following table describes each stage in the scenario analysis playbook.

<table><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Scope** – **Services**

</td><td>

Service that you want to analyze. You can add only one service per analysis; to change the service you must create a new record.

</td></tr><tr><td>

**Scope** – **Dependencies**

</td><td>

Dependencies such as systems, people, third parties, and locations that support the selected service. Once you mark them as complete, this selection is locked and cannot be changed.

</td></tr><tr><td>

**Scenarios**

</td><td>

Adverse-event scenarios from the library \(for example, Cloud service outage, Network connectivity failure, and so on\).

</td></tr><tr><td>

**Reference Data**

</td><td>

Historical risk-event records that the statistical model uses as reference data. The Risk events list is empty by default.

 Select **Add** to choose the desired risk events. Selected records are captured as a snapshot on the scenario analysis record; events that match your filter and are created after you mark the step as complete, are not added retroactively, and the snapshot does not refresh when the source record is updated.

 Once marked complete, you cannot add any further risk events.

</td></tr><tr><td>

**Scenario Testing**

</td><td>

Simulation assessment that includes a questionnaire. For more information, see [Start simulation and run scenario testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/complete-sca-scenario-testing.md).

</td></tr><tr><td>

**Results**

</td><td>

Simulation output metrics. Contains **Simulation Results**.

 You can adjust the answers in Scenario Testing until you select **Mark as complete** on the Results step.

</td></tr><tr><td>

**Treatment Decision**

</td><td>

Decision to treat the identified risk. Offers the following options: **Accept**, **Mitigate**, **Avoid**, or **Transfer**.

</td></tr><tr><td>

**Operational Vulnerabilities**

</td><td>

\(Optional\) Operational weaknesses logged from the analysis results.

</td></tr><tr><td>

**Issues**

</td><td>

\(Optional\) Issues logged for a separate remediation tracking.

</td></tr></tbody>
</table>## Statistical model profile

The Statistical model profile is set by an administrator and controls how the simulation runs. It links an Annual Loss Model \(or other statistical model\) to the assessment question templates used to collect input parameters. The profile translates technical model parameters into plain-language questions that business users can answer without needing to know the underlying mathematics.

One statistical model profile is shipped with the base version: **Annual loss model driven by risk events**.

**Note:** The **Statistical model profile** field on the Create Scenario Analysis form is a reference picker, not a drop-down. You can select only one profile per analysis.

|UI Component|Description|
|------------|-----------|
|**Name**|Name that identifies the Statistical Model Profile.|
|**Statistical Model**|Mathematical model used to run the simulation. Currently, only Annual Loss Model is supported.|
|**Input Assessment Template**|Smart Assessment template that collects Lambda, Mu, and Sigma values from the SME.|
|**Output Assessment Template**|Smart Assessment template that surfaces the computed results to the analyst.|
|**Table**|ServiceNow table from which reference data is drawn to auto-populate assessment answers \(for example, risk events\).|
|**Active**|Status that indicates whether the profile is available for selection when creating a new Scenario Analysis.|

## Scenario analysis profile — parameter and questions

A Scenario Analysis Profile links a Statistical Model Profile to the input and output assessment templates and maps model parameters to plain-language questions. The profile translates Lambda, Mu, Sigma, and other Monte Carlo parameters into questions that business users can understand and answer.

|Parameter|Mapped question|Direction|
|---------|---------------|---------|
|loss\_frequency\_lambda|How many loss incidents do you expect to occur over the chosen time horizon \(typically one year\)?|Input|
|simulation\_runs|How many simulation runs are required?|Input|
|severity\_mu|What is the typical financial loss per incident over the chosen time horizon?|Input|
|severity\_sigma|What are the variable losses \(sigma\)?|Input|
|min\_loss|What is the minimum credible financial loss that could result from a single incident?|Input|
|max\_loss|What is the maximum credible financial loss that could result from a single incident?|Input|
|selected\_percentile|Provide the level of risk sensitivity you want to analyze.|Input|
|loss\_tolerance|Service impact tolerance for financial loss \(sourced from the linked service\).|Input|
|mean\_expected\_loss|What is the model's calculated Average Annual Loss?|Output|
|var\_50\_percentile|What is the model's Typical \(Midpoint\) Annual Loss?|Output|
|std\_deviation|What is the model's standard deviation of annual losses?|Output|
|var\_90\_percentile|What is the selected percentile for tail risk \(90th\)?|Output|
|var\_95\_percentile|What is the modeled annual loss at the 95th percentile?|Output|
|var\_99\_percentile|What is the modeled annual loss at the 99th percentile?|Output|
|max\_loss \(output\)|What is the Maximum Annual Loss \(USD\) observed across runs?|Output|
|tail\_risk\_average|What is the Tail Risk Average \(USD\)?|Output|
|prob\_exceed\_tolerance|What level of financial loss has the probability of being exceeded?|Output|

\[Omitted image "sca-statistical-model-profile-mappings.png"\] Alt text: Statistical Model Profile record 'Annual loss model driven by risk events' with the Question Parameter Mappings related list showing each parameter mapped to its input or output assessment question.

The parameter column on the Statistical Model Profile record is fixed. You can re-map an existing parameter to a different assessment question or update an existing question but the number of questions and parameters remains same. You cannot add new parameters or remove existing ones because the parameters are tightly coupled to the annual loss model that ships with the base version.

**Note:** The Monte Carlo simulation uses a log-normal severity distribution and a Poisson frequency distribution. These distributions are set and you cannot configure them.

## How the simulation runs

When you select **Start Simulation**, the simulation is dispatched synchronously to the Triton inference server. The default number of simulation runs is 100,000; you can reduce this number through the simulation count question on the input assessment. On completion, the playbook displays a "Simulation Completed Successfully" banner.

Re-running the simulation with the same inputs may produce different output values within the same statistical range. Every "Start Simulation" request submits a fresh run to the engine.

## Simulation results

After the simulation runs, the output assessment surfaces quantitative metrics. These values help stakeholders understand the financial and operational impact of the scenario.

|UI Component|Description|
|------------|-----------|
|**Average Annual Loss**|Mean financial loss expected each year based on the simulation.|
|**Typical \(Midpoint\) Annual Loss**|Most likely single-year loss outcome from the model.|
|**Variation \(Std Deviation\)**|Variation such as how much loss values vary from the average. Higher values indicate greater uncertainty.|
|**90th Percentile Loss**|Loss exceeded in only 10% of simulated outcomes — high-risk scenario.|
|**95th Percentile Loss**|Loss exceeded in only 5% of simulated outcomes — very high-risk scenario.|
|**99th Percentile Loss**|Extreme tail-risk loss value exceeded in only 1% of outcomes.|
|**Tail Risk Average**|Average loss in the worst outcomes beyond the selected percentile \(conditional value at risk\).|
|**Probability of exceeding loss tolerance**|Key output value. Indicates how likely the scenario is to breach the service's defined impact tolerance.|
|**Simulation Results** tab|Quantitative output metrics from the simulation run.|

**Note:** Each input question that the back-fill automation auto-populates shows a **Last responded by System** badge under the answer. The badge stays in place if you overwrite the value; it is for informational purpose only.

## Treatment decision

The Treatment Decision step shows selectable cards, one per treatment strategy, with a required **Reason** field for the card grid. Selecting a card highlights it and writes the chosen strategy to the Treatment field on the underlying record. After submitting the treatment decision, the optional **Operational Vulnerabilities** and **Issues** steps are available.

|UI Component|Description|
|------------|-----------|
|**Accept**|Option to proceed without taking remediation actions.|
|**Mitigate**|Option to create actions to reduce the likelihood or impact of the risk.|
|**Avoid**|Option to change or discontinue the service or dependency to eliminate the risk.|
|**Transfer**|Option to shift the risk to a third-party, for example through insurance or outsourcing.|
|**Reason**|Free-text field for entering the justification for the selected treatment strategy. Provided for all four treatment choices.|

## Workflow Studio Playbook

Playbook are created in Workflow Studio and displayed in workspace pages built in UI Builder. For more information, see the following topics:

-   [Exploring Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&version=australia)
-   [Getting started with Playbooks](https://www.servicenow.com/docs/access?context=getting-started-processes&version=australia)

**Related topics**  


[Verify the Smart Assessment templates setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-sae-templates-for-sca.md)

[Create a scenario analysis record using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sca-record.md)

