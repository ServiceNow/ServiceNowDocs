---
title: Compliance impact on control requirements
description: Control objective requirements are created for a control objective. The control requirements are generated for all the controls that are associated with a control objective. However, a control or a control requirement can become non-compliant because of an attestation failure or issue creation at either of the two levels.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Compliance impact on control requirements

Control objective requirements are created for a control objective. The control requirements are generated for all the controls that are associated with a control objective. However, a control or a control requirement can become non-compliant because of an attestation failure or issue creation at either of the two levels.

## Associating an issue to a control requirement and its impact on control status

An issue can be created for a control requirement through an attestation. You can enable the **Take attestation at requirement level** option to send out the attestations for all the control requirements instead of sending an attestation for the control at the control level. The **Take attestation at requirement level** option is in the Attestation related list of the Control form.

If the attestation fails, then an issue is created. The issue created because of an attestation failure has the **Issue source** field tagged as **Requirement Attestation Failure**.

You can view the control requirement reference in the **Control/Risk** field of the Details related list in the Issue form.

You can close the issue by providing a response and saving it in the Issue form. Your response can be either **Remediate** or **Accept**.

-   If you select Remediate and set the state of the issue to Closed Complete, then the control requirement becomes compliant, provided there is no other open issue on the control requirement.
-   If you select Accept, then you imply that the issue still exists and that you accept it. In this case, even if you close the issue with no other open issues, the status of the control requirement is still non-compliant.

Therefore, to make the control requirement status compliant you must set your response to Remediate and not Accept.

Whenever the control requirement becomes non-compliant, the control also becomes non-compliant. When the status of the control requirement becomes compliant, there are two more criteria to be checked at the control level:

-   There should be no open issue on the control.
-   Not even one control requirement of the control must be non-compliant.

If these two conditions are satisfied, then the status of the control becomes compliant. Otherwise, the status of the control remains non-compliant despite the control requirements status being compliant.

-   If the control and control requirements are in Draft or Attest state, then you can pass the attestation to make the control and control requirement compliant.
-   If the control and control requirements are in the Review or Monitor state, you can move the state **Back to attest** and pass the attestation to make the control and control requirements compliant.
-   If the control requirement is in Monitor or Retired state, then you cannot create an issue for the control requirement.

## Impact of indicator test and control test on the control requirement status

A control requirement can become non-compliant because of an issue that is created as a result of an attestation failure on this control requirement. If there is no open issue on the control or even if you close the issue that existed, the control requirement remains non-compliant. Although the indicator task **Result** is **Passed**, the control remains non-compliant because one of the control requirements of the control is non-compliant. You must explicitly make the control requirement of the control as compliant, and then when the indicator test is passed, then the control becomes compliant.

The same is the case for a control test also.

## Changes in control state and its impact on control requirements

-   **Draft**

    All control requirements are generated when the control is in Draft state.

    When the control moves to Draft state, the associated control requirements also move to Draft state.

-   **Attest**

    When the control moves to Attest state from any other state, then all the control requirements of the control also move to Attest state irrespective of the **Take attestation at requirement level** option.

    **Note:** When you select **Attest**, you have the option to take a single attestation at the control level or take multiple attestations at the control requirements level, which is guided by the **Take attestation at requirement level** option.

-   **Review**

    For control-level attestation, when the **Take attestation at requirement level** option is not selected, after attestation is complete the control moves to Review state. Simultaneously all associated control requirements of the control move to Review state.

    For control requirement level attestation, when the **Take attestation at requirement level** option is selected, then the attestation is sent to all the Attestation respondents of all the control requirements individually. When the attestation is completed, irrespective of the attestation outcome as Pass or Fail at the control requirement level, the control requirement moves to Review state. If the attestation passes, the status of the control requirement becomes compliant, and if it fails, the control requirement becomes non-compliant. After the attestation is completed for all the control requirements and when they all are in Review state, then the control moves to the Review state.

-   **Monitor**

    When the control moves to Monitor state, the associated control requirements also move to Monitor state.

    Control requirements remain in the Monitor state as long as the control remains Active and hasn’t moved back to Draft or Attest state.

-   **Retired**

    When the control is Retired, the control requirements move to Retired state.

    Deleting a control removes or deletes all the control requirements associated with the control.


For more information on attestation flow scenarios, see the [Attestation workflow for Control and Control requirements \[KB0555561\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0555561) article in the Now Support Knowledge Base.

## Impact of inherited requirements on the life cycle of a control

1.  If one of the control requirements becomes non-compliant, then the corresponding control is also non-compliant.
2.  If one of the inherited control requirements becomes non-compliant, then the control is also non-compliant.
3.  If an attestation for a control fails, an issue is created, and the control becomes non-compliant.
4.  If an attestation for a control requirement fails, an issue is created, and the control requirement becomes non-compliant. So, the associated control also becomes non-compliant.
5.  If one of the inherited control requirements of a hybrid control retires in such a condition, an automated issue is created. The reason for issue creation is reflected in the **Issue source** field of the Issue form as **Provider Control Retired**. An appropriate message is also logged in the Activity related list of the Issue form. To resolve the issue, you can either change the common control provider or convert the control requirement to self implemented.
6.  If the control is in Draft state and one of its requirements is retired, then you cannot move the control from Draft to Attest state.

**Note:** For more information, see the [Operational changes and their impact on the process flow of control and its requirements \[KB1587264\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587264) article in the Now Support Knowledge Base.

**Parent Topic:**[CAM reference](reference-grc-cam.md)

