---
title: Understanding the risk assessment instance
description: A risk assessment instance is where a risk assessor can assess risks and objects by responding to questions or factors.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Understanding the risk assessment instance

A risk assessment instance is where a risk assessor can assess risks and objects by responding to questions or factors.

After the risk assessment methodology \(RAM\) is created and the risk assessment scope is defined, the assessments are initiated by the risk administrator. The assessor receives a notification to assess the risks. To perform the risk assessment, an assessor must have the sn\_grc.business\_user role. The assessment is used to arrive at a risk score for an entity.

**Note:** You must manually assign the advanced risk assessment roles to the sn\_grc.business\_user role. To understand how you can adjust granting of roles and groups, refer to see the [How to adjust granting of roles and groups to use background jobs \[KB0963693\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963693) article in the Now Support Knowledge Base.

The questions that a risk assessor answers are configured in the RAM. An assessment can contain manual factors and automated factors. Manual factors need human input as responses. For automated factors, the responses are automatically calculated. Automated factors are automatically executed based on the schedule that is defined in their configuration.

After an assessment is completed, then based on the defined reassessment frequency, a reassessment is automatically triggered. A reassessment is triggered only if the existing risk assessment instance is in the Monitor state. If an assessment is in the Monitor state, then whenever automated factors run according to their schedule, the assessment scores will change and the factors will contribute new scores to the rollup.

If the risk assessor determines that an assessment must be reassigned to another relevant assessor, then the assessor can reassign the assessment. The assessor can also modify the responses after responding to the factors.

If an assessment is taken more than once, and if the option to copy the previous assessment responses is enabled in the RAM, then the responses from the previous assessments get automatically copied to the current assessment.

**Note:** Automated factor responses and overridden scores aren’t copied from previous assessments.

## Components of a risk assessment instance

Based on the configurations in the RAM, the risk assessment instance form also displays the following related lists:

-   Previous Assessments: The previous five assessments for the risk that is currently being assessed.
-   Risk Events: The number of risk events that are associated with the risk.
-   Risk Indicators: The number of risk indicators that passed and failed for this risk.
-   Open Issues: The number of open issues for the risk and their state and owners.
-   Risk Response Tasks: The number of risk response tasks that are created for the assessment.
-   Related controls: The controls that are related to the risk. This related list appears only when the control environment is being assessed.

    **Note:** Customers on previous releases might not be able to see the updated count for passed and failed indicators. To resolve this issue, run the Update indicator and Controls Count fix script.


An assessor has the option to not assess the mitigating controls. The option to opt out of controls is useful in cases where there is a risk but there are no controls to mitigate it. For example, consider a scenario where a pandemic is a risk but there are no vaccines to control it. In such a case, the risk is assessed but the controls can be left out of the assessment. When an assessor decides to opt out of assessing mitigating controls and residual risks, the score is set to **Not applicable**.

If the control assessment is configured to assess individual controls, and the controls are associated with the risk being assessed, then the option to opt out of controls does not appear. This happens because the controls are defaulted.

If the residual assessment is for inherent risks and controls, and if the risk assessor opts out of control assessment, then the residual risks are not applicable. This condition is created because if there are no controls, that automatically means there are only inherent risks and no residual risks.

## Stages of risk assessment

The risk assessment life cycle goes through the following states:

1.  Ready to assess: A new assessment instance is created.
2.  Inherent assessment: The inherent risk assessment is performed.
3.  Control assessment: The control assessment is performed.
4.  Residual assessment: The residual risk assessment is performed.
5.  Target assessment: The target risk assessment is performed.
6.  Respond: You respond to the risks.
7.  Awaiting approval: The risk assessment is awaiting approval from the approvers if they have been identified.
8.  Monitor: The risk assessment is complete and is being monitored.

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

