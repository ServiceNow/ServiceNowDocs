---
title: Assess project risks using Advanced Risk Assessment
description: Assess the project risks by responding to predefined factors or questions. Arrive at a risk score for the project.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project Risk Assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Assess project risks using Advanced Risk Assessment

Assess the project risks by responding to predefined factors or questions. Arrive at a risk score for the project.

## Before you begin

Role required: it\_project\_manager and sn\_grc.business\_user

## About this task

A risk is assessed for inherent risks and residual risks. An inherent risk is a risk that has no mitigating controls. A residual risk is a risk that remains after the controls are accounted for. The workflow of the risk assessment is determined by the risk admin on the risk assessment methodology configurations. If the project manager wants to enable approval of the assessment, then the project manager can configure the approval flow in the Project Integration Configuration form. If an assessment for a risk has been taken before, the results of the previous assessments appear in the Previous Assessments related list.

A risk assessor can do the following:

-   Assess the risks that were added for a project.
-   Decide if the risks must be elevated to enterprise risks.

To understand how to assess risks on a risk assessment instance and how to respond to the questions, refer to [Understanding the risk assessment instance](../concept/understanding-risk-assessment-instance.md).

## Procedure

1.  Navigate to **All** &gt; **My Tasks** &gt; **Module**.

2.  Select the assessment that you want to assess.

3.  Click **Assess**.

4.  In the Inherent Assessment section, respond to the factors as appropriate and click **Save and Calculate**.

5.  In the Results section, you can override the computed score.

    1.  If you think that the computed risk score is not correct, select the **Override computed score** check box to override the computed risk score.

    2.  In the **Override inherent risk** field, select a value to override the computed risk rating.

        This field appears only when the **Override computed score** option is selected.

    3.  In the **Comments** field, enter your justification for overriding the computed risk rating.

6.  Click **Perform residual assessment**.

    1.  In the Residual Assessment section, respond to the factors as appropriate.

    2.  Click **Save and Calculate**.

7.  Click **Mark as complete**.

8.  Click **Request Approval**.

    The option to request approval appears only when the Project Integration Configurations form has the approvers identified. In that case, the workflow moves to the Awaiting Approval state. But if the option to request approval is not selected, then the workflow moves to the Monitor state.


## What to do next

[Elevate a project risk to enterprise risk](Elevating-a-risk.md).

**Parent Topic:**[Project Risk Assessment using Advanced Risk Assessment](../concept/risk-and-ppm-better-together.md)

