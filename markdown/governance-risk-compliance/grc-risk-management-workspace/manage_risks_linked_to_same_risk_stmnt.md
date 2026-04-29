---
title: Manage risks linked to the same risk statement
description: You can create and associate multiple risks to the same risk statement and entity combination. This association benefits the risk managers and the entity owners.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage risks, risk statements, and risk frameworks, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Manage risks linked to the same risk statement

You can create and associate multiple risks to the same risk statement and entity combination. This association benefits the risk managers and the entity owners.

Before the latest release, users could only associate one risk for a single entity and risk statement combination. This ability was useful for customers who have a mature risk program with a well-defined and standardized risk taxonomy. However, it did not meet the requirements of customers who do not have a standardized risk taxonomy. Such customers usually have only two or three levels of risk statement hierarchy while their actual risks are still local for each business unit or lines of business. Also, when the first line identifies new risks, they associate those risks to an enterprise risk hierarchy. This allows the new risk scores to aggregate and impact the overall risk hierarchy. With the current release, a new option called **Inherit from risk statement** is introduced on the Risk form. If this option is selected, the risk creation happens in the previous manner. This means that there can be only one instance of risk statement and entity combination. However, if this option is not selected, the system allows the risk statement hierarchy to be used as categorization and sub-categorization hierarchy and associates multiple risks to the same risk statement and entity combination. This option also enables the first line to associate their newly identified risks to the risk hierarchy at a level they want to. When this new option is not selected, the system assumes that the name and description of the risk is overridden and must not be the same as the risk statement name and description.

This feature benefits the risk manager as it allows the risk managers to define the risk taxonomy according to the needs of their organization. It also benefits the entity owners to identify risks for their entity and link them to enterprise risk taxonomy.

To understand this feature, see the following image and consider the example. Most customers have risk statements defined until Corruption. Anything lower than Corruption such as accepting a bribe is defined as a risk as it is difficult to harmonize these risks across the organization. This feature of linking multiple risks to the same risk statement and entity enables customers to prevent the creation of orphan risks with no one acting on them.

![Risk statement and risk creation hierarchy](../image/risk_stmnt_hieracrchy.png "New risk statement hierarchy")

**Parent Topic:**[Manage risks, risk statements, and risk frameworks](../reference/r_RiskRegister.md)

**Related topics**  


[Workflow of a risk using Advanced Risk](risk-lifecycle-using-advanced-risk.md)

[Risk hierarchy and scoring](../reference/risk-hierarchy-scoring.md)

