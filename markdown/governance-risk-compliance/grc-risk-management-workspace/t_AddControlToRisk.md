---
title: Add a control to a risk
description: Controls are added to the risks for the on-going review of processes.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Add a control to a risk

Controls are added to the risks for the on-going review of processes.

## Before you begin

Role required: sn\_risk.manager and sn\_compliance.manager

## About this task

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Register** &gt; **All Risks**

2.  Open the risk record from the list.

3.  Continue with one of the following options.

<table id="choicetable_y2l_kdz_pv"><thead><tr><th align="left" id="d313154e91">

Option

</th><th align="left" id="d313154e94">

Description

</th></tr></thead><tbody><tr><td id="d313154e100">

**Add an existing control**

</td><td>

1.  In the **Controls** related list, select **Add**.
2.  Select the controls that are associated with the risk profile.
3.  Select **Add relationship**.
 **Note:** The controls displayed after selecting the **Add** button are limited to controls where the entity of control matches the risk entity. If there are no eligible controls that can be related to the risk, the **Add** button isn’t displayed on the Controls related list.

</td></tr><tr><td id="d313154e139">

**Add a new control**

</td><td>

1.  In the **Controls** related list, select **New**.
2.  On the form, fill in the fields. For a description of the field values on the Control form, see [Create a control](../../grc-policy-and-compliance/task/t_CreateAControl.md).
3.  Select **Submit**.


</td></tr><tr><td id="d313154e176">

**Inherit common controls**

</td><td>

1.  In the **Controls** related list, select **Inherit common controls**.
2.  Select the controls.
3.  Select **Add**.
 **Note:** The common controls displayed after selecting the **Inherit common controls** button are limited to controls where the reliant entity of control matches the risk entity. If there are no eligible controls that can be related to the risk, the **Inherit common controls** button isn’t displayed on the **Controls** related list.

</td></tr></tbody>
</table>    -   When a control objective and risk statement are associated and the control entity matches the risk entity, the risk-control association is created.
    -   The risks and controls that are created after associating a control objective to the risk statement aren’t associated with the risk statement immediately. They get associated when the **GRC Profile Generation** scheduled job runs.
    -   If you manually delete a control from a risk, the control won’t be re-created by the scheduled job. You must manually create it again if necessary.

**Parent Topic:**[Using Risk Management](../concept/using-risk-mgmt.md)

**Related topics**  


[Associate a risk statement with a control objective in the Risk Workspace](../../grc-workspace-risk/task/create-control-objective-ws.md)

