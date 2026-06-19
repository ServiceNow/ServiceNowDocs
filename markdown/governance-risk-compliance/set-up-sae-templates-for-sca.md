---
title: Verify the Smart Assessment templates setup
description: Verify that the input and output Smart Assessment templates are set up and published in the Assessment Workspace before running an advanced scenario analysis. The Statistical model profile in the advanced scenario analysis uses these templates to present plain-language questions and display simulation results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/set-up-sae-templates-for-sca.html
release: australia
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, Smart Assessment Engine, SAE template, statistical modelling profile]
breadcrumb: [Building a scenario analysis using simulation, Scenario analysis using simulation, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Verify the Smart Assessment templates setup

Verify that the input and output Smart Assessment templates are set up and published in the Assessment Workspace before running an advanced scenario analysis. The Statistical model profile in the advanced scenario analysis uses these templates to present plain-language questions and display simulation results.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

The advanced scenario analysis references the following Smart Assessment templates from the Statistical model profile:

-   Input assessment template — Questions presented to analysts, such as minimum loss, maximum loss, and tolerance thresholds.
-   Output assessment template — How simulation results are displayed, such as average expected loss and probability of breaching the loss tolerance.

Statistical Model Profile defines the end-to-end configuration for a modelling flow — including which input and output templates are used, which statistical model is applied, and which reference table it draws from.

Both templates are managed through the Smart Assessment Engine \(SAE\) to support dynamic field configurations. For more information, see [Building a scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

    The example shows the Smart Assessment templates, part of the demo data, for the advanced and legacy scenario analysis experience.

    \[Omitted image "sa-temp-for-sca.png"\] Alt text: Smart Assessment templates for advanced scenario analysis.

2.  Verify that the input and output Smart Assessment templates are set up and published by your administrator.

    The input assessment template as shown in the example defines the questions that auto-populate from the selected reference data and that analysts can override before submitting. The questions are written in plain language — for example, "What is the maximum credible financial loss?" — and map to the simulation model's mathematical parameters in the statistical modelling profile.

    \[Omitted image "sa-temp-for-sca-input-risk.png"\] Alt text: Input risk template for advanced scenario analysis.

    The output assessment template defines how the Monte Carlo simulation results are displayed to analysts. The output template renders the simulation outputs, such as the average expected loss, the maximum expected loss, the probability that the loss tolerance will be exceeded, and other financial impact metrics. The example shows the output risk template configuration.

    \[Omitted image "sa-temp-for-sca-output-risk.png"\] Alt text: Output risk template for advanced scenario analysis.

    Rather than requiring analysts to interpret technical terms such as VAR 99th percentile, Severity MU, or Tail Risk Average, the profile maps these to plain-language questions. When a template is selected, the relevant questions are automatically surfaced and analysts fill in their responses using the available reference data. This keeps the experience intuitive for business users while ensuring the model receives the precise inputs it needs.

3.  Confirm that the Statistical Model Profile links the correct input and output templates and reference table.

    This configuration is prebuilt; each model parameter maps to a plain-language question that analysts answer using reference data.

    The input assessment template and output assessment template — both are automatically linked to the Statistical modelling profile and are treated as fixed. Deleting or modifying the mapped parameters breaks the model.

    You may update the question text for clarity, but the underlying parameters must remain intact. Do not add or remove any parameter in the question-parameter mapping; the fixed set of questions must remain mapped to its parameters, otherwise the simulation model does not work. You can change only the wording of the questions.

    **Note:** This restriction applies only to the statistical modelling templates. For the manual method, you can create any published template with no restrictions.

    For information on the manual method, see [Run a scenario analysis using the manual method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/run-sca-manual-method.md).

    \[Omitted image "sca-ip-asmt-temp.png"\] Alt text: Input template.\[Omitted image "sca-op-asmt-temp.png"\] Alt text: Output template.\[Omitted image "sca-smp-table-ip-op-asmt.png"\] Alt text: Parameter mappings.

    After both the input and output Smart Assessment templates are published, the Statistical model profile can reference them, and analysts can run the advanced scenario analysis using the guided playbook experience. For more information, see [Create a scenario analysis record using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sca-record.md).


