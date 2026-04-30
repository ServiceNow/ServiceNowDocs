---
title: Risk hierarchy and scoring
description: Starting with New York, risk managers can create hierarchies that include different types of risk \(operational risk, IT risk, or strategic risk\). Once the underlying risks are assessed, the risk scores are automatically rolled up across the risk statement hierarchy, providing better tactical and strategic decision-making.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
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

![Sara head of Operational Risk, Sophia head of IT risk and the taxonomies defined for IT risk, and the Chief risk officer are looking at all the roll up scores.](../image/risk-hierarchy-managers.png "Hierarchical risk taxonomy showing integrated view of risk")

## Translate quantitative risk scores to qualitative values

The **Tolerance Status** and the **Calculated Score** are based on the Calculated Annual Loss Expectancy \(ALE\) of the underlying risks:

-   Sum of calculated ALE
-   Average calculated ALE
-   Maximum calculated ALE
-   Minimum calculated ALE

**Note:** Only risks in the **Monitor** state can contribute to the risk statement scores.

![screen shows calculations on the Risk Rollup and Tolerance tab](../image/risk-rollup-tolerance-tab.png "Risk Rollup and Tolerance tab")

-   **[Association of entities at any level of a risk statement](../concept/associate-entity-types-at-any-level-of-risk-stmt.md)**  
You can associate entities, entity types, and indicator templates, at any level of the risk statement hierarchy. Creating this association is useful for risk managers while assessing risks.

**Parent Topic:**[Manage risks, risk statements, and risk frameworks](r_RiskRegister.md)

**Related topics**  


[Workflow of a risk using Advanced Risk](../concept/risk-lifecycle-using-advanced-risk.md)

[Manage risks linked to the same risk statement](../concept/manage_risks_linked_to_same_risk_stmnt.md)

