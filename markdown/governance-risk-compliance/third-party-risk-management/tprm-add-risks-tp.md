---
title: Manually add a risk to a third party or engagement
description: If you’re using both Risk Management and Third-party Risk Management, you can associate risks and risk statements with third parties and engagements. These associations influence risk posture and scoring.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [TPRM with Risk Management, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Manually add a risk to a third party or engagement

If you’re using both Risk Management and Third-party Risk Management, you can associate risks and risk statements with third parties and engagements. These associations influence risk posture and scoring.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

When you associate a risk with a third party or engagement, the risk becomes part of the entity’s risk profile and can be included in scoring calculations. This does not automatically trigger assessments unless configured through TPRM rules.

Controls are automatically generated when you associate a policy with an entity type or an entity type with a control objective. A control is created for each entity listed in the entity type for the control objective. Controls can also be manually created.

For more information on creating risk statements and risks in Risk Management, see [Create a risk statement](../../grc-risk/task/t_CreateRiskState.md), [Create a risk manually](../../grc-risk/task/t_CreateRisk.md), and [Generate a risk from a risk statement](../../grc-risk/task/t_GenRiskFromRiskFrameProfile.md).

To understand the difference between a control objective and a control, see [Relationship between risks, risk events, and risk statements](../../grc-risk/reference/manage-risk-events.md#).

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**.

2.  Select the list icon \(![List icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\) and then navigate to **Third parties** &gt; **All third parties** or **Engagements** &gt; **All engagements**.

3.  Select the third party or engagement that you want.

4.  Navigate to the **Risks** tab of the third party or engagement.

5.  Assign a risk to the engagement by selecting **New**.

6.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create new risk form](../../grc-vendor-risk/reference/tprm-risk-record-form.md).

7.  Select **Submit**.

    For more information on managing risks, see [Manage risks, risk statements, and risk frameworks](../../grc-risk/reference/r_RiskRegister.md).

    The risk is created and all related lists are visible.


-   **[Create new risk form](../../grc-vendor-risk/reference/tprm-risk-record-form.md)**  
Use the create new risk form to capture all the information that you need to associate a control with a third party or engagement using the Third-party Risk Management application. As a third-party risk admin, you can create a control.

**Parent Topic:**[Integrating Third-party Risk Management with Risk Management](../concept/rm-assessment-integration.md)

**Related topics**  


[Integrating Third-party Risk Management with Risk Management](../concept/rm-assessment-integration.md)

[Create new risk form](../../grc-vendor-risk/reference/tprm-risk-record-form.md)

[Define the risk appetite for a risk](../../grc-workspace-risk/task/define-risk-appetite-on-risk.md)

[Create a risk statement](../../grc-risk/task/t_CreateRiskState.md)

[Define the risk appetite for a risk statement](../../grc-workspace-risk/task/define-risk-appetite-on-risk-statement.md)

