---
title: Scenario analysis
description: Conduct a scenario analysis to assess how a critical service performs under adverse conditions. Starting with Operational Resilience, version 22.3.1, you can use the advanced scenario analysis with simulation in the Operational Resilience Workspace, apply statistical modelling to quantify financial impact, and record a treatment decision.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/scenario-analysis-ov.html
release: australia
topic_type: concept
last_updated: "2026-05-28"
reading_time_minutes: 3
breadcrumb: [Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Scenario analysis

Conduct a scenario analysis to assess how a critical service performs under adverse conditions. Starting with Operational Resilience, version 22.3.1, you can use the advanced scenario analysis with simulation in the Operational Resilience Workspace, apply statistical modelling to quantify financial impact, and record a treatment decision.

## What is a scenario analysis

A scenario analysis evaluates the impact of adverse-event scenarios on the services that support your business. You run scenarios against a service and its dependencies. You can then use the results to make a treatment decision and log operational vulnerabilities or issues.

Releases before Operational Resilience, version 22.3.1 supported the legacy scenario analysis flow, which had the following limitations:

1.  Complex navigation — Steps opened simultaneously as tabs with no guided sequence, making it difficult for analysts to track progress or determine next steps.
2.  Limited output — The result was a "Breached/Not breached" outcome with minimal contextual data, providing little actionable insight.
3.  Manual, repetitive effort — Analysts manually answered each question for every scenario event, with no data-driven assistance to populate or guide responses.

## Benefits of using simulation and the guided experience

Starting with Operational Resilience, version 22.3.1, the advanced scenario analysis with the Playbook experience offers the following benefits:

1.  Structured Playbook guidance: Replaces the fragmented, manually driven legacy process with a structured, data-driven Playbook that guides analysts from scope definition to treatment decision.
2.  Monte Carlo statistical modelling: Quantifies financial risk exposure through simulated annual loss projections, providing more accurate and reliable risk assessments than manual methods.
3.  Data-driven financial impact analysis: Uses an Annual Loss Model and historical risk-event reference data to produce a quantified financial impact and calculate the probability of breaching a service's loss tolerance.

## Statistical model profile

When you create a scenario analysis record, select **Statistical Modelling** — used for advanced scenario analysis — or **Manual** in the **Method** field. The Statistical model profile bridges the simulation engine and the analyst experience by mapping mathematical parameters to plain-language assessment questions.

**Note:** The **Statistical Modelling** method of scenario analysis is only available with the IRM Advanced license.

The base configuration includes an annual loss model driven by risk events, which references input and output templates managed through the Smart Assessment Engine \(SAE\).

Before selecting a method, verify with your administrator that Smart Assessment templates have been created and published in the Assessment Workspace, using the purpose *Scenario Analysis \(advanced\)* or *Scenario Analysis - Manual*. For more information, see the following topics:

-   [Verify the Smart Assessment templates setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-sae-templates-for-sca.md)
-   [Create a scenario analysis record using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sca-record.md)
-   [Building a scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md)

## States for the analysis

A scenario analysis record moves through different states. A newly created record starts in the **Draft** state. When you select **Complete analysis** and confirm the prompt, the record moves to **Completed** and becomes read-only.

## Known limitations

The following limitations apply to the advanced scenario analysis:

-   Owner and assessor roles — The owner and assessor must be the same person.
-   Single service per analysis — Only one critical business service can be scoped per scenario analysis record.
-   Model capabilities — The Monte Carlo model is tightly coupled to the configuration. You cannot swap distribution types \(for example, triangular or normal\) or introduce custom models.
-   Reference data — Only risk events are supported as reference data inputs.

## Legacy scenario analysis

The advanced scenario analysis is enabled by default. For an overview of the legacy experience, see [Legacy scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/legacy-scenario-analysis-ov.md). To switch to the legacy flow, see [Enable the legacy scenario analysis flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-scenario-analysis-legacy-flow.md).

