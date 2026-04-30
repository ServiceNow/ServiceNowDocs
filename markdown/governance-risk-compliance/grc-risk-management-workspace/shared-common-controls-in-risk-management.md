---
title: Common controls in Risk Management
description: By linking the risks to a common control in the Risk Management application, you can reduce the time and effort that is needed to manage and apply these centralized controls to your reliant entities. For example, a fire sprinkler system can be a common control for multiple business units \(BUs\), such as finance, security, and human resources \(HR\).
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Common controls in Risk Management

By linking the risks to a common control in the Risk Management application, you can reduce the time and effort that is needed to manage and apply these centralized controls to your reliant entities. For example, a fire sprinkler system can be a common control for multiple business units \(BUs\), such as finance, security, and human resources \(HR\).

## Overview of common controls

Every organization has multiple \(BUs\) and shared functions, such as information technology \(IT\), HR, and finance. These shared functions define the policies and controls that the BUs can use to meet the regulatory requirements or to manage the risks in their BUs. Multiple BUs can use common controls that are owned and managed by a different department or team. This process enables an organization to maintain centralized control over certain processes while each BU can take advantage of these common controls. For more information on common controls, see [Common Controls](../../grc-workspace-compliance/concept/common-controls-multiple-rel-entities.md).

To mitigate the risks in the reliant entities, a risk owner can link their risks to the common controls. By linking the risk, a risk owner can reduce the effort that is required to attest and test these common controls for the reliant entities.

## Benefits of common controls

A common control has the following benefits:

-   You spend less time and effort to manage a common control because you can test and apply a common control to all your reliant entities.
-   You only need to manage the active controls, so the overall reporting of the controls is improved.

## Common controls in a risk

If a control objective and risk statement are associated and the reliant entity of the control matches the risk entity, the risk-control association is established automatically. You can also inherit common controls to a risk when the risk entity is marked as a reliant entity in a common control. Any changes to the risk statement and the control's objective relationship can impact the risk-control association as well. The following example shows the inherit common controls option on the risk form:

![Inherit common controls.](../image/inherit-common-control.png "Inherit common controls")

**Note:** Only active relationships between risks and controls are maintained and any historic relationships are automatically deleted.

## Common controls in a risk assessment

You can inherit common controls in the risk assessment when the entity is marked as a reliant entity in the common control. The following example shows the inherit common controls option on the risk assessment form.

![Inherit common controls in a risk assessment.](../image/inhert-common-control-risk-assessment.png "Inherit common controls in risk assessment")

## Common controls in a risk-mitigation task

You can inherit the common controls to a risk-mitigating task when the entity is marked as a reliant entity in the common control. You can inherit the common controls to a risk-mitigating task when it is in the Draft or Work In Progress state. The following example shows the inherit common controls option on the risk-mitigation task form.

![Inherit common controls in risk mitigation.](../image/inherit-control-risk-mitigation.png "Inherit common controls in risk-mitigation task")

## Common controls in a risk event

A common control is automatically linked to a risk event when the underlying risk has materialized for the risk event. It enables the control owner to identify when the common control fails and to take immediate action if a common control does fail. The following example shows the inherit common controls option on the risk event form:

![Inherit common controls in risk mitigation.](../image/inherit-common-control-risk-event.png "Common controls in risk event")

**Parent Topic:**[Using the Risk Workspace](using-risk-workspace.md)

