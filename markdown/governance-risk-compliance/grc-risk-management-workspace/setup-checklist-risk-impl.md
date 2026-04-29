---
title: Setup checklist for the Risk Management application
description: This checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform instance. When you have completed these tasks, the base system is ready for operation.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Risk Management implementation, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Setup checklist for the Risk Management application

This checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform® instance. When you have completed these tasks, the base system is ready for operation.

## Before you begin

Role required: sn\_risk.admin

## Procedure

1.  Create and print a PDF of the checklist topic and check off tasks as you complete them.

2.  To generate a PDF, select the **Save As PDF** ![Save as PDF icon](../../grc-cam/image/save-as-pdf.png)icon and at the top of the topic and select **Selected topic**.

<table id="table_ns4_rt4_rcc"><thead><tr><th>

Item

</th><th>

Checklist

</th></tr></thead><tbody><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

A user with the sn\_risk.admin role, can -   define and modify the risk criteria
-   configure the risk properties
-   create assessments
-   modify the existing assessments
-   assign roles
 For details, see [Risk Management Administration](../concept/Administration.md).

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

A user with the sn\_risk.admin role, can also assign roles. For details, see [Roles installed with Risk Management](../reference/r_RolesInstallWRisk.md)

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

A risk manager, with the sn\_risk.manager role, needs to manage numerous risk statements. To achieve this goal, the risk framework must be defined. For details, see [Create a risk framework and associate risk statements to it](t_CreateRiskFrame.md).

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

A risk manager, with the sn\_risk.manager role, must create a risk statement to group risks logically. For details, see [Create a risk statement](t_CreateRiskState.md)

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

A risk administrator or a risk manager can create a risk assessments using the Risk Assessment Designer. For details, see [Create a risk assessment using the Risk Assessment Designer](create-assessment-using-assessment-designer.md).

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Risk administrators and risk managers can create risk indicators. Risk indicators monitor changes in the levels of risk exposure and contribute to the early warning signs that enable organizations to report risks, prevent crises and mitigate them in time. For details, see [Create a risk indicator](create-risk-indicator.md).

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Risk administrators and risk managers can create entities manually, rather than generating them from the entity types. For details, see [Create independent entities](../../grc-common/task/create-a-profile.md)

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Risk administrators and risk managers must create and edit entity types and map them to existing ServiceNow® tables for which you must track compliance. Entities are assigned to control objectives and risk statements, which generate controls and risks for every entity type. For details, see [Generate risks and controls from entity types](../../grc-common/task/t_CreateProfileTypes.md)

</td></tr></tbody>
</table>
**Parent Topic:**[Risk Management implementation](../concept/risk-impl-overview.md)

