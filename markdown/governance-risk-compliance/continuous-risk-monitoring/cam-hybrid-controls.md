---
title: Set up baseline controls
description: Use the baseline controls to inherit a control, mark a control as common, or create a hybrid control. Create a hybrid control to inherit requirements partially from common controls and the remaining requirements are created for the control that was generated from the baseline control.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [RMF step 2 - Select controls for an authorization package, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Set up baseline controls

Use the baseline controls to inherit a control, mark a control as common, or create a hybrid control. Create a hybrid control to inherit requirements partially from common controls and the remaining requirements are created for the control that was generated from the baseline control.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.info\_system\_sec\_manager

## About this task

Hybrid controls not only give you the ability to inherit partial requirements from common controls but also gives you the flexibility to make the best use of the common control requirements while self-implementing the remaining requirements for that control.

In CAM there are two ways to inherit controls from the control objectives sourced from NIST 800-53-r5:

-   **Inherit from provider**

    The control is inherited directly and completely. For example, if the common provider, Building A, provides a control objective that is fire prevention, and this control objective has about three different requirements, namely fire alarm, smoke detection, and sprinkling, then the control is directly inherited by identifying it as common control.

    **Note:** A control associated with one authorization package can be a common provider to another authorization package if the control is marked as a Common control provider in its Authorization package, and that particular package must be in Monitor state. Only then it’s called as a common control.

-   **Hybrid inheritance**

    The control is partially inherited. Only one or a few of the control's requirements are inherited in this case. Considering the preceding example, hybrid inheritance is enabled in the following combinations:

    -   One of the requirement such as fire alarm can be inherited from Building A, and the other two requirements can be self-implemented.
    -   One of the requirements such as fire alarm can be inherited from Building A, and another requirement such as smoke detection can be inherited from Building B. The rest of which can be self-implemented.
    -   All requirements are inherited. This inheritance is not a partial inheritance because at least one of the requirements must be inherited and one must be self-implemented. Therefore this inheritance can’t be termed as hybrid inheritance.

**Note:** The role and responsibility of the authorization package must be assigned to an Authorization official \(AO\) who must review and approve the authorization package when it moves from one state to another. The Information System Security Officer \(ISSO\) is required to mark a common control, create a hybrid control, or to identify a control as not applicable as these control objectives are sourced by NIST. After the Authorization official \(AO\) provides the approval, the authorization package moves to the Implement state.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Packages**.

2.  Select an authorization package record that is in a **Select** state and has the Baseline controls added.

    In the **Select** state, all the baseline controls are added and you can identify the role of each baseline control. You can inherit a control, mark a control as common, or create a hybrid control.

3.  To assign baseline controls from a common control provider as common controls, select the control objectives in the Baseline Controls tab that you want to assign as common controls.

    1.  Select **Mark as Common** and then select **OK** in the Confirmation popup.![Common baseline controls.](../image/Baseline-control-mark-common.png)

    2.  Select **Request approval** to request approval.

        After approval, the authorization package moves to Implement state. Before moving to the Implement state, the **Creates controls automatically** option in the control objective form must be true for all the baseline controls and hybrid controls. Otherwise, an error message pops up with the list of control objectives prompting you to make the **Creates controls automatically** option as true.

    3.  Select the control objectives link in the message and enable the **Creates controls automatically** option for all the control objectives in the respective control objective form.

    After the authorization package is approved, the controls are created in the Controls tab. You can then move the authorization package to the Assess state. In this state, the Security Control Assessor \(SCA\) is required as an engagement lead, where the engagement is created to test the controls. After this state, the authorization package is moved to the Authorize state.

    For an authorization package to be available as a common control provider for other authorization packages, it must be in the Monitor state. After the authorization package is moved to the Monitor state and the Common control provider flag is set as true for a few of the baseline controls, the controls that were generated for those baseline controls become common control providers for other authorization packages.

4.  To inherit the requirements from a common control of a particular common control provider or create a hybrid control, select only one control objective in the Baseline Controls tab.

    1.  Select **Create Hybrid**.

        The Create hybrid control popup lists the entities in groups. Grouping by entity helps when there are more requirement numbers added to the reference number of a control objective. You can inherit requirements partially from some of the common control providers, and self implement the rest of the requirements. If you select all control requirements from all the categories of providers for inheritance without a single self implemented requirement, then the requirements are not partially inherited but becomes full inheritance of all requirements, which is not allowed. At least one self-implemented requirement is required to create a hybrid control.

    2.  Select the requirements from the entity groupings, leaving one or more requirements for self implementation for that control.

    3.  Select **Add**.

        The Hybrid Controls related list appears with the selected baseline controls. A baseline control is an m2m of a control objective and an authorization package.

        ![Set up baseline controls to inherit controls and requirements.](../image/cam-sort-baseline-controls.png "UI actions on baseline controls")

    4.  Select the Display/hide hierarchical lists \(![Display or hide hierarchical lists icon.](../image/cam-display-hide-hierarch-icon.png)\) icon to see the inherited requirements.

        All the other requirements that are not listed here are self implemented.

        **Note:** Only common control providers with control requirements can be used to create hybrid controls.

5.  To inherit controls from a single provider, select a control objective from the Baseline Controls related list.

    1.  Select **Inherit from Single Provider** and then select the Common control list in the Inherit from Common Control popup.

    2.  Select the controls that you want to inherit from and then select **Confirm**.

        The entities of the controls that you select become the common provider. For each of these authorization packages, there is an Inherited Controls related list. The **Inherited from** field in this related list gives you the information as to which control is the common control provider.

        **Note:** To inherit from a provider, which is a direct inheritance, there might not be any requirement for the control.

6.  To inherit controls from multiple providers, select a control objective from the Baseline Controls related list.

    1.  Select **Inherit from Multiple Providers**.

    2.  Select the requirements from the different providers and select **Add**.

    Unlike inherited controls from a single provider, fully inherited controls generate a control instance and test templates, so Security Control Assessors \(SCAs\) can test the controls within their engagements. All requirements are inherited from provider packages.

    Fully inherited controls differ from hybrid controls in one key way: in a hybrid control, at least one requirement is self-implemented by the current package. In a fully inherited control, all requirements must be inherited.

7.  To mark a particular baseline control as not applicable so that it is out of the work flow and not allow controls to be generated, select a baseline control

    1.  Select **Not Applicable**.

    2.  Enter a note to justify your action in the **Justification** field and then select **Confirm**.

        This action changes the status of the selected baseline control to **Not implemented**.

    In the **Select** state, you did the setup for the type of controls to be generated. After the setup is complete, you can approve the authorization package.

8.  Select **Request approval**.

    The authorization package then moves to the **Implement** state. In this state, based on the setup, controls are created.


