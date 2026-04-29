---
title: Modify control requirement
description: Approve the authorization package when it is in the Select step to create controls. After approval, the authorization package moves to the Implement step and the controls are generated. You can still modify the control requirement implementation status at the control level.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Modify control requirement

Approve the authorization package when it is in the Select step to create controls. After approval, the authorization package moves to the Implement step and the controls are generated. You can still modify the control requirement implementation status at the control level.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner

## About this task

Controls are generated for all the baseline controls that have the value as **Applicable** or **Hybrid** in the **Control review** field of the Baseline control tab. Additionally, the type of control that is generated is determined by the **Control allocation** field in the Control form, which can be either **System specific** or **Hybrid**.

-   Controls are created for all controls coming directly from baseline controls that are system specific and marked as Applicable.
-   Controls are created for hybrid controls, which will have requirements based on the hybrid setup.
-   Controls are not created for inherited controls.

All the controls are generated in the **Implement** state, however you can still update the setup at the control level in this state.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Packages**.

2.  Select the authorization package that is in the Implement state, for which you want to modify the control setup.

3.  Select the Controls related list.

    The number of controls generated is displayed in the Controls related list.

    ```
    Number of Controls = Baseline Controls + Hybrid Controls
    ```

4.  Select the control to modify its setup.

    ![UI setup actions on a control when the authorization package is in Implement state.](../image/cam-implement-setup.png)

5.  To change the provider for a particular requirement, select the control requirement in the Control requirements related list.

    1.  Select **Change Provider**.

    2.  Select the **Common control** list field in the Inherit from Common Control popup.

        The filter query lists only those providers that you have not already selected for you to choose from.

    3.  Select **Confirm**.

    On selecting confirm, the query filter removes the current provider from the authorization package of the Control requirements list. You can also select the Activity Journal related list to see the message that the provider has been changed, logged in the **Activities** field.

    You can only change the provider for the requirement using **Change Provider**. However, this action does not make the requirement automatically compliant by changing the provider.

    **Important:** You must not make a selection that changes the value in the **Control allocation** field of the Control form when you do this setup change. If it is a hybrid control and if this requirement is the only one that has the **Implementation status** as **Self implemented**, and by changing the provider to another control that has the control allocation value as **System specific** where the **Implementation status** of all its requirements are **Inherited**, then the control allocation is no longer hybrid as all its requirements are inherited.

    For a hybrid control at least one requirement should be inherited and at least one should be Self implemented.

    -   All the requirements are Self implemented for a system specific control.
    -   At least one requirement must be Self implemented and the rest can be inherited for a hybrid control. If it is inherited, then the control requirements are inherited from a provider, which comes from the Baseline Controls related list.
6.  To change the implementation status of the control requirements to self implemented, select those control requirements in the Control requirements related list.

    1.  Select **Convert to Self implemented**.

    2.  Select **Yes** in the Confirmation popup.

    Your control requirement selections can also include those requirements that are already in self implemented status. However, after this operation, only those requirements that were in Inherited status are converted to Self implemented.

    By this UI action, the existing m2m relationship between the control provider and the control is deleted. Thereafter, a new m2m relationship is created with the new selection. A message describing the change is also logged in the **Activities** field of the Activity Journal tab of the Control form.

7.  To convert a control requirement from self implemented to inherited status, select the requirement in the Control requirements related list.

    1.  Select **Convert to Inherited**.

    2.  Select the **Common control** list field in the Inherit from Common Control popup.

        You can select from all the providers that are available to inherit that control requirement. After this UI action, the previous self implemented control requirement is deleted, and the new requirement that you selected is inherited from the provider. Simultaneously, the set up is also changed at the authorization package level in the Hybrid Controls related list, where the requirement selections of that baseline control reflect your change.

        If this is the only requirement that is in self implemented status for the hybrid control, then you cannot convert it to inherited.

8.  To see the list of control requirements for a hybrid control, select the Display/hide hierarchical lists \(![Display or hide hierarchical lists icon.](../image/cam-display-hide-hierarch-icon.png)\) icon that gives you a hierarchy view.

    You can use ![Display or hide hierarchical lists icon.](../image/cam-display-hide-hierarch-icon.png) in the Hybrid Controls related list as well. Additionally, you can also do the above three actions – Convert to Self implemented, Convert to Inherited, and Change Provider – from the Controls related list.

    From the Implement state you can move back to the Select state. When you do so, all the controls that were active and created in the Implement state will be deleted or retired. When you are in Select state, you can modify the setup for all the hybrid controls and generate controls once again.

9.  To revert a hybrid control as a baseline control, select the control in the Hybrid Controls related list.

    1.  Select **Return to Baseline Control** and then select **OK** in the Confirmation popup.

    This action deletes the previous Requirement selections for the hybrid control. It also updates the baseline control's **Control review** field from **Hybrid** to **Applicable**. You can set up the steps for this baseline control and select **Create Hybrid**. You can view the current control requirements available for this control. Four setup changes are possible for a hybrid control to return to being a baseline control:

    -   It must be a system specific control while moving back to Select state, and you can mark this as inherited.
    -   Convert from hybrid to inherited.
    -   Move the control back to baseline, mark it as common, and make it a common provider.
    -   Convert the control to not applicable so that it is out of the work flow and controls will not be generated for this.
    You can also revert an inherited control as a baseline control by selecting **Return to Baseline Control** in the Inherited Controls related list. In this case, the baseline control's **Control review** field is updated from **Inherited** to **Applicable**.


