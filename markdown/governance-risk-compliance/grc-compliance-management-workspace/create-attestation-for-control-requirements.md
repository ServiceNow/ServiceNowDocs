---
title: Take attestation at control requirements level
description: The Take attestation at requirement level option enables administrators to perform compliance attestation at a granular level for individual control requirements within a control.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 1
breadcrumb: [Manage controls using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Take attestation at control requirements level

The Take attestation at requirement level option enables administrators to perform compliance attestation at a granular level for individual control requirements within a control.

## Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager, sn\_compliance.user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the List icon.

3.  Under Compliance library, select **Controls**.

4.  Select the control that contains the control requirements you want to attest.

5.  In the Details tab, select **Take Attestation at Requirement Level**.

6.  The Attestation field will default to **GRC CR Attestation**.

7.  In the Assign Respondent field, specify the user or role responsible for attestation \(for example, System Administrator\).

8.  Select **Attest**.

9.  Navigate to **Control requirements** tab, and select each control requirement.

    Attestation tasks are generated for each control requirement under Assessment Instances.

10. For each assessment instance, select **Take assessment**.

    1.  Select Yes \(implemented\) or No \(not implemented\).

    2.  If Yes, attach evidence and provide an explanation.

    3.  If No, provide a reason in the Explain field.

    4.  Select **Submit**.

        :

11. Review the following information for any failed assessment.

    -   Generates an issue for that control requirement.
    -   Marks the parent control as non-compliant.
    -   Rolls up the same status to the entity and control objective level.

