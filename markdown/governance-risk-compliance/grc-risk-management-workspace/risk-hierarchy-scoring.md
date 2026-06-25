---
title: Risk hierarchy and scoring
description: Starting with New York, risk managers can create hierarchies that include different types of risk \(operational risk, IT risk, or strategic risk\). Once the underlying risks are assessed, the risk scores are automatically rolled up across the risk statement hierarchy, providing better tactical and strategic decision-making.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/risk-hierarchy-scoring.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage risks, risk statements, and risk frameworks, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Risk hierarchy and scoring

Starting with New York, risk managers can create hierarchies that include different types of risk \(operational risk, IT risk, or strategic risk\). Once the underlying risks are assessed, the risk scores are automatically rolled up across the risk statement hierarchy, providing better tactical and strategic decision-making.

## Risk Hierarchy

Risk managers and administrators create and view hierarchies on the risk statement form:

-   Define a parent risk statement using the **Parent** field
-   Add children risk statements using the **Risk Statements** related list

**Note:** Risk users can view the hierarchies established by the managers and administrators.

Depending on the risk areas, different people in the organization own and manage their own risks. However, top-level risk scores take into account the score of all the risks below it. Therefore, managing all the different risk areas in a central location provides an integrated view of your organizations total risk posture.

\[Omitted image "risk-hierarchy-managers.png"\] Alt text: Sara head of Operational Risk, Sophia head of IT risk and the taxonomies defined for IT risk, and the Chief risk officer are looking at all the roll up scores.

## Translate quantitative risk scores to qualitative values

The **Tolerance Status** and the **Calculated Score** are based on the Calculated Annual Loss Expectancy \(ALE\) of the underlying risks:

-   Sum of calculated ALE
-   Average calculated ALE
-   Maximum calculated ALE
-   Minimum calculated ALE

**Note:** Only risks in the **Monitor** state can contribute to the risk statement scores.

\[Omitted image "risk-rollup-tolerance-tab.png"\] Alt text: screen shows calculations on the Risk Rollup and Tolerance tab

-   **[Association of entities at any level of a risk statement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/associate-entity-types-at-any-level-of-risk-stmt.md)**  
You can associate entities, entity types, and indicator templates, at any level of the risk statement hierarchy. Creating this association is useful for risk managers while assessing risks.

**Parent Topic:**[Manage risks, risk statements, and risk frameworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/r_RiskRegister.md)

**Related topics**  


[Workflow of a risk using Advanced Risk]()

[Manage risks linked to the same risk statement]()

