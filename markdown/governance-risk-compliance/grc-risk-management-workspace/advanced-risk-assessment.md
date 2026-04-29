---
title: Advanced Risk Assessment
description: Use the ServiceNow Governance, Risk, and Compliance \(GRC\) Advanced Risk Assessment feature to create an integrated risk platform. This integrated platform supports various kinds of risk assessment methodologies. It enables you to integrate risk assessment as part of your overall decision-making process.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Risk Management, Governance, Risk, and Compliance]
---

# Advanced Risk Assessment

Use the ServiceNow® Governance, Risk, and Compliance \(GRC\) Advanced Risk Assessment feature to create an integrated risk platform. This integrated platform supports various kinds of risk assessment methodologies. It enables you to integrate risk assessment as part of your overall decision-making process.

Advanced Risk Assessment offers the following benefits:

-   Digitizes the complete risk management life cycle, including risk identification, risk analysis, risk evaluation, risk treatment, and monitoring.
-   Customizes the risk assessment process based on the unique needs of your organization. This customization includes configuring the assessment criteria, the context, and the overall risk scoring logic.
-   Supports both qualitative and quantitative risk assessment methods.
-   Automatically aggregates the bottom-up risk assessment scores across the risk.
-   Embeds the risk assessment process in the workspace for first-line users. This embedding helps users make informed decisions based on risks that are associated with actions.

**Note:** To know if your current license entitles you to Advanced Risk Assessments, contact ServiceNow.

## Steps of risk assessment

Before understanding Advanced Risk Assessment in detail, it is important to understand the key steps of risk management:

1.  Risk identification: Find an uncertainty or risk that might prevent your organization from achieving its objectives​.
2.  Risk analysis: Understand the cause and consequence of the risk.
3.  Risk evaluation: To determine if additional action is required, compare the results of the risk analysis with the established risk criteria.
4.  Risk treatment: Define an action plan​ to address the risk.
5.  Risk monitoring: Track the risk posture of the organization and communicate it to relevant stakeholders.

![Steps of risk management.](../image/ara_concept.png "Steps of risk management")

Risk assessment consists of risk identification, risk analysis, and risk evaluation. Advanced risk assessment is performed based on factors or questions and their responses. It can be performed for an entity such as an organization. To use advanced risk assessment, you must enable the **Migrate to Advanced Risk Assessments** property located under the Administration module. The assessor and approver for the risk assessment must have the sn\_grc.business\_user role. Advanced risk assessment enables you to do a detailed assessment of the risks where the inherent risks, mitigating controls, and residual risks are assessed. If you don't have the complete GRC setup for entities, risk statements, controls, and so on, then you can still assess the risks on any ServiceNow record or object. An example of object assessment is assessing change management. During risk assessment, the following risks are assessed.

-   Inherent risks: Inherent risks are risks that don't have controls. For example, driving at a high speed on a highway is inherently more of a risk than driving at a moderate speed. The score of this inherent risk is derived by multiplying the impact of the risk and the likelihood of the risk.
-   Control effectiveness: Controls can mitigate the impact or likelihood of a risk. For example, highways have speed limit monitors. If a risk materializes, the controls mitigate the impact. Controls can be preventive, detective, or corrective.
    -   Preventive controls are designed to prevent errors, inaccuracies, or fraud before these issues occur.
    -   Detective controls are intended to discover the existence of errors, inaccuracies, or fraud.
    -   Corrective controls are designed to correct errors or irregularities that have been detected.
-   Residual risks: Residual risks are the leftover risks that remain after the implementation of controls. For example, despite the safety measures in place, if there’s still an accident, then the damage caused by the accident is a residual risk. A residual risk score can be calculated using any of the following methods:
    -   A matrix between inherent and residual effectiveness.
    -   A mathematical formula such as the inherent score minus the control score.
    -   Answers to factors.
-   Target risks: Target risks are the desired risk an organization want to achieve in the future. By evaluating the desired level of likelihood and impact of identified risks, organizations can establish target risk levels for each risk. For example, when assessing a risk, you consider various aspects such as inherent risk, the effectiveness of controls, and residual risks. However, it's equally important to capture the desired risk level that will be attained after your risk response is implemented. The target risk represents the optimum level of risk that you aim to achieve after your action plan is successfully executed. It enables you to measure the benefits your organization gets in relation to the cost of implementing those actions.

-   **[Workflow of Advanced Risk Assessment](workflow-ara.md)**  
To use Advanced Risk Assessment, you must set up the risk assessment methodology \(RAM\), define the assessment scope, and perform the assessment.
-   **[Factors in Advanced Risk Assessment](factors.md)**  
Factors are questions that you can use to analyze risks. Factors appear on a risk assessment instance.
-   **[Types of risk rating methodologies](qual-vs-quant.md)**  
Risks are scored during an assessment and then a rating is derived. Ratings are of three kinds: qualitative, semi-quantitative, and quantitative.
-   **[Any object assessment using Advanced Risk Assessment](any-object-assessment.md)**  
If you don't have the complete GRC setup for entities, risk statements, controls, and so on, even then, you can still assess the risks on any ServiceNow record or object. An example of object assessment is assessing change management or assessing a citation.
-   **[Delegation of risk assessment](../../grc-workspace-risk/concept/delegation-of-risk-assessment.md)**  
If a risk assessor is unavailable to perform a risk assessment, the assessor can appoint a delegate to perform the risk assessment for a specified time period. The ServiceNow AI Platform enables you to appoint your delegates.
-   **[Understanding the risk assessment instance](understanding-risk-assessment-instance.md)**  
A risk assessment instance is where a risk assessor can assess risks and objects by responding to questions or factors.
-   **[Managing risk responses](../../grc-workspace-risk/concept/risk-response.md)**  
A risk response is the strategy used to deal with risks after the risks are assessed.
-   **[Risk score rollup in Advanced Risk Assessment](risk-rollup-ara-concept.md)**  
In Advanced Risk Assessment, risk scores are calculated across risk statement hierarchy, entity hierarchy, or a combination of both. These methods enable stakeholders to monitor their risk posture and provide visibility of the overall aggregated risk score.
-   **[Privacy risk management](risk-assessment-as-lite-user.md)**  
As users of Privacy Management, you can perform advanced risk assessments with a limited set of features even if you do not have the complete license for Integrated Risk Management.
-   **[Manage risk assessment scheduler](risk-assessment-scheduler.md)**  
Create a risk assessment scheduler and assign it to the risk manager. A risk manager can then identify the entities and the risks within the entities for bulk initiation of risk assessments.
-   **[Integration of advanced risk assessments with risks and controls](integrate-ara-with-risks-and-controls.md)**  
When customers migrate to advanced risk assessments, the system replaces the legacy risk life cycle and shows a new section called Assessment Summary on the Risk form. This section is useful for the risk managers as it provides the overall visibility of the assessment results.
-   **[Risk appetite and tolerance in Advanced Risk](../../grc-workspace-risk/concept/risk-appetite-tolerance.md)**  
You can define a risk appetite and tolerance within your organization by using the Advanced Risk application. A risk appetite and tolerance enable your organization to define the boundaries for acceptable and unacceptable risks.
-   **[Target risk assessment in Advanced Risk](target-risk-assessment.md)**  
You can perform a target risk assessment to define your desired future risk level using the Advanced Risk application. The target risk assessment enables you to assess your target risk posture and monitor progress toward its achievement.

**Parent Topic:**[Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md)

