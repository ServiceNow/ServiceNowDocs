---
title: Target risk assessment in Advanced Risk
description: You can perform a target risk assessment to define your desired future risk level using the Advanced Risk application. The target risk assessment enables you to assess your target risk posture and monitor progress toward its achievement.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Target risk assessment in Advanced Risk

You can perform a target risk assessment to define your desired future risk level using the Advanced Risk application. The target risk assessment enables you to assess your target risk posture and monitor progress toward its achievement.

## Overview of a target risk assessment

A target risk assessment is an assessment type to define the desired risk level the organization want to achieve in the future. By evaluating the desired level of likelihood and impact of identified risks, organizations can establish target risk levels for each risk.

For example, when assessing a risk, organizations consider various aspects such as inherent risk, the effectiveness of controls, and residual risks. However, it's equally important to capture the desired risk level that will be attained after the risk response is implemented. The target risk represents the optimum level of risk that you aim to achieve after your action plan is successfully executed. It enables you to measure the benefits your organization gets in relation to the cost of implementing those actions.

## Setting up a target assessment

A risk administrator can configure and set up a target risk assessment for your organization in the Advanced Risk application. Risk administrator can enable the option for assessing a target risk on the Risk assessment methodology \(RAM\) form. For more information, see [Configure a target assessment](../task/configure-target-assessment.md).

**Important:** You can enable target risk assessment for existing published RAMs. However, after you enabled, it can’t be turned off. Additionally, target risk assessment can only be conducted for new assessments and not for assessments that are already in progress.

## Assessing a target risk

Assessors can analyze the future state of the risk based on the defined factors, scoring logic, and rating criteria in the RAM form. Assessing the future state of risk is a structured process that shares similarities with inherent, control, and residual assessment types. Based on the target risk profile, the system also computes the future risk appetite status. It enables assessors to analyze if the target risk profile is in line with the risk appetite or not. Risk approvers can review the target risk rating and the future appetite status and approve them. Target risk assessment can be performed for both risk and object-based assessments. However, if it’s object-based, the future appetite status isn’t computed and displayed. For more information, see [Perform advanced risk assessment in the Risk Workspace](../../grc-workspace-risk/task/perform-ara-workspace.md).

**Important:** If target risk assessment is enabled for a methodology, the risk or object can only be assessed in the next experience.

## Reporting a target risk

On the heatmap, you can view the target risk profile, which provides a comprehensive understanding of the inherent, residual, and target states of the risk. When the risk assessment criteria are shared, you can analyze the risk movement from inherent state to residual state and then to its target state. By using the risk trend capability, you can assess risk changes over the past five periods to determine if it’s moving in the desired direction. For more information, see [Risk heatmap workbench](../../grc-workspace-risk/concept/risk-heatmap-workbench.md).

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

