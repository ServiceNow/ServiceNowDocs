---
title: AI risk posture
description: Aggregated risk posture displays inherent risk, residual risk, and control effectiveness for AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-airc-risk-posture.html
release: zurich
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [use]
breadcrumb: [Governance posture and compliance, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# AI risk posture

Aggregated risk posture displays inherent risk, residual risk, and control effectiveness for AI assets.

## Overview of AI risk posture

Risk posture views in AI Control Tower help you understand the level of risk associated with AI assets and how that risk changes when control effectiveness is considered.

At the portfolio level, risk posture views summarize how AI assets are distributed by risk level and highlight concentrations of higher-risk assets. At the AI system level, aggregated risk rating views show the relationship between inherent risk, control effectiveness, and resulting residual risk for a specific AI system.

Risk heat maps add more context by showing how counts of risks are distributed across inherent risk levels and control effectiveness levels. These views help you identify where ineffective or partially effective controls are associated with higher-risk conditions.

A global filter at the top of the Risk posture page lets you switch the widgets on this page between **AI System**, **AI Model**, and **Dataset** asset types. Selecting an asset type updates the AI system by aggregated risk score chart and the risk heat map to show results for that asset type only. By default, the page displays results for **AI System**.

## AI system by aggregated risk score

AI systems are classified by aggregated risk score using a donut chart. The risk scores are qualitatively classified as High, Medium, and Low.

AI systems are distributed across risk rating levels through two primary visualizations: inherent risk and residual risk.

Inherent risk: Risk level of an AI system before controls, mitigations, or safeguards are applied. This baseline view identifies the potential risk exposure that exists in the AI environment without intervention. The chart categorizes systems into four risk levels: Low, Medium, High, and Critical.

Residual risk: Risk level after controls, mitigations, and safeguards are implemented. This view demonstrates the effectiveness of the risk management program by showing how control measures reduce overall exposure. By comparing inherent and residual risk charts, you can measure the impact of governance controls.

\[Omitted image "image.aict-aggregated-risk-score"\] Alt text: Donut charts showing AI systems distributed across Low, Medium, High, and Critical risk levels for inherent and residual risk.

## Risk heat map

The Risk heat map widget displays identified risks for AI assets. By default, the widget applies the Residual risk filter, but you can filter the heat map by Inherent risk. Segmentation changes based on the selected filter. Risks appear under the respective combination of risk and control effectiveness, or impact and likelihood, depending on the selected risk classification filter. You can filter the risk heat map by Risk Assessment Methodology \(RAM\) when more than one methodology is available.

\[Omitted image "aict-risk-heat-map.png"\] Alt text: Heat map grid showing AI asset counts by inherent risk level and control effectiveness, with color coding from green to red.

## How data is determined

AI systems by aggregated risk score:

-   Risk ratings come from risk assessments performed against the risks linked to each AI system.
-   A background job rolls up the individual assessment results into a single risk rating per AI system.
-   The chart then counts how many AI systems fall into each rating level \(for example, Low, Medium, High, Critical\).

Risk heat map: Each cell shows the count of risk assessment instances at that intersection. This is the standard Advanced Risk heat map, scoped to AI governance entities.

