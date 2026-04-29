---
title: Control requirement generation and upgrade steps
description: The Creates controls automatically and Create control requirements options in the control objective form and the state of the authorization package are important to create control requirements.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Control requirement generation and upgrade steps

The **Creates controls automatically** and **Create control requirements** options in the control objective form and the state of the authorization package are important to create control requirements.

## Control requirement generation logic

If you enable the **Creates controls automatically** and **Create control requirements** options in the control objective form, then the item generation flow is triggered automatically to create controls and control requirements, respectively. Depending on the state of the control, the generated control requirements' state changes.

If the **Create control requirements** option is selected when the authorization package moves from the **Select** to the **Implement** state, the controls are generated. At the same time, control requirements for the control objective requirements are also generated. Control requirements would be generated only if the control objective requirements are present and if the flag is true. If the control objective requirements are present but the flag is false, then the control requirements would not be generated.

If while creating the control objective, the flag was set as false and the requirements weren’t generated, you can still generate the control requirements by selecting the flag and saving the control objective record, provided the controls associated with this particular control objective have control objective requirements, and the controls are Active and in the Draft state. If the controls are in any state other than Draft, then control requirements would not be generated. However, if, for example, the control was in the Monitor state and is moved back to Draft state, then control requirements would be generated provided the **Create control requirements** option is selected.

-   **New control objective requirements added**

    The same is the case when you add control objective requirements to a control objective using **New** or **Edit** in the Control objective requirements related list.

-   **Update**

    If you update the description of a control objective requirement, then the description of the corresponding control requirement is updated provided the control is in the Draft state. If the control is in any other state, then the description is updated when the control moves back to Draft state.

-   **Delete**

    If a few of the control objective requirements of a control objective are removed, then correspondingly the control requirements of the control cannot be removed, instead they are marked as a Manual requirement. This condition is true for controls in any state. Later, if the control moves to Draft state, then you can remove the manual tag from these requirements. On the other hand, if a new control is created after some of the control objective requirements are removed, then the new control does not have the requirements that were removed but only the existing number.


If the authorization package moves from the Implement to Select state, then all the associated controls of CAM are retired, and correspondingly all the requirements associated with them are also retired. All these actions are handled by item generation.

## Required upgrade steps

The following actions happen when you upgrade to the Australia release:

1.  The **Authorization package** field and **Control allocation** field in the Control form are newly added. The values in these fields are populated for existing CAM controls.
2.  For all NIST 800-53-revision 5 control objectives, the **Create control requirements** option is set to **True** by default in the Control objective form.
3.  The control requirements are created for all the existing controls, from NIST 800-53-revision 5 control objectives, which are in the Draft state.

