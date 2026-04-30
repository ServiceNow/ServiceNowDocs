---
title: Manage risk assessment scheduler
description: Create a risk assessment scheduler and assign it to the risk manager. A risk manager can then identify the entities and the risks within the entities for bulk initiation of risk assessments.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Manage risk assessment scheduler

Create a risk assessment scheduler and assign it to the risk manager. A risk manager can then identify the entities and the risks within the entities for bulk initiation of risk assessments.

In most organizations, the second line of risk managers coordinates the risk assessments. This second line of risk managers identifies the entities and the risks within those entities for risk assessment. They also identify who must assess the identified risks. This process is like a risk assessment campaign the risk managers must manage until the first line of risk managers reach the level of maturity where this is no longer required and the first line of risk managers can self-assess and report these risks. Because of this cycle of risk assessment, the risk managers are expected to create individual risk assessment scopes and initiate risk assessments​. This repetitive activity results in loss of time for risk managers. To address this issue, a new form called Risk Assessment Scheduler has been introduced in the Quebec release. The risk assessment scheduler enables the risk manager to select the:

-   Risk assessment methodology
-   Entities that must be assessed
-   Assessors of the assessment
-   Frequency with which the risks must be reassessed.

Based on this information, the system automatically creates the risk assessment scope and initiates the risk assessments for those entities at the defined frequency. All the risks that are mapped to the entity are considered to be in scope for assessment​.

The following figure shows the states, the descriptions, and the expected outcomes of each of the actions for the risk scheduler form:

![The complete life cycle of the risk assessment scheduler](../image/risk_assessment_scheduler.png "Workflow and actions of the risk assessment scheduler")

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

**Related topics**  


[Schedule risk assessments in the Risk Workspace](../../grc-workspace-risk/task/schedule-risk-assessment-workspace.md)

