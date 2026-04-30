---
title: Workflow of Advanced Risk Assessment
description: To use Advanced Risk Assessment, you must set up the risk assessment methodology \(RAM\), define the assessment scope, and perform the assessment.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of Advanced Risk Assessment

To use Advanced Risk Assessment, you must set up the risk assessment methodology \(RAM\), define the assessment scope, and perform the assessment.

Before using Advanced Risk Assessment, different users must perform different setup tasks. These steps define the workflow of the assessment.

1.  Set up the risk assessment methodology \(RAM\): A risk administrator with the sn\_risk.admin role sets up the system. The administrator does the following:

    -   Identification: Identifies if a risk or an object is being assessed.
    -   Assessment: Determines how to assess the issue, such as with assessment criteria, risk scoring, or reporting preferences.
    For more information, see [Configure a risk assessment methodology](../task/configure-ram.md).

2.  Define the risk assessment scope: After the RAM is defined, the entity owner defines and identifies the following:

    -   The relevant risks for the entity.
    -   The assessors and approvers for those assessments.
    -   Periodicity of those risk assessments.
    For more information, see [Create a risk assessment scope and initiate assessments](../task/create-risk-assess-scope.md) or [Create a risk assessment scope in the Risk Workspace](../../grc-workspace-risk/task/create-risk-asses-scope-workspace.md).

3.  Perform risk assessment: The risk assessor with the sn\_grc. business\_user role performs the following assessment tasks.

    -   Assesses the inherent risks and the effectiveness of mitigating controls​.
    -   Reviews the residual risk and defines the risk treatment plan.
    -   Perform a target risk assessment to define your desired future risk level.
    -   ​Triggers the review and approval workflow.
    For more information, see [Perform advanced risk assessment in the Risk Workspace](../../grc-workspace-risk/task/perform-ara-workspace.md).

4.  Monitor the assessments: After the risk assessment is approved, the assessment moves to the Monitor state. The risks assessed in the risk assessment must be monitored especially if it contains automated factors. Automated factors or questions that automatically fetch data from any of the data sources have ever-evolving risk ratings. Therefore, a risk which may currently have a low rating might have a higher rating later. This makes it imperative to monitor a completed assessment to reduce threats to your organization.

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

