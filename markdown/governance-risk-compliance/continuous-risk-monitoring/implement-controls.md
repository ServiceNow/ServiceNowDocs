---
title: RMF step 3 - Implement controls
description: After you have selected controls for implementation and performed any of the possible actions on them, you can implement the controls.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# RMF step 3 - Implement controls

After you have selected controls for implementation and performed any of the possible actions on them, you can implement the controls.

## Before you begin

Role required: sn\_irm\_cont\_auth.information\_type, sn\_irm\_cont\_auth.information\_owner, or sn\_irm\_cont\_auth.admin

## About this task

When approval was received on the Authorization Package form, a **Percentage of controls implemented** field and a **Controls** related list appeared on the form.

The **Controls** related list contains all of the controls created from the control objectives within the selected authorization boundary.

## Procedure

1.  From the list of controls, select the control number \(with a CTRL prefix\) to open the control.

    ![Control](../image/control-implement.png)

2.  The implementation process performed by your system owner and other technical or security personnel employs the control management workflow inherent in the base GRC system.

    For details, see the following:

    -   [Manage controls](../../grc-policy-and-compliance/concept/c_GRCControls.md)
    -   [Manage control attestations](../../grc-policy-and-compliance/concept/c_Attestations.md#)
    -   [Manage control indicators](../../grc-policy-and-compliance/concept/manage-indicators-policy-comp.md#)
3.  The **Percentage of controls implemented** field keeps track of your progress while you implement the controls.

4.  After you have completed the implementation process for all controls, select **Assess** to transition the package to the **Assess** state.

    To send the package back to the **Select** state, select **Back to previous step**. All active controls will be retired and the package must get approval to advance again to the **Implement** state.


