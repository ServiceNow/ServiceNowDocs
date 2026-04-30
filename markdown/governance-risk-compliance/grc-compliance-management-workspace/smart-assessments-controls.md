---
title: Control assessment based on GRC attestation template
description: You can select the option to attest controls using an assessment method. This assessment is an alternative method to the classic assessment that is based on ServiceNow AI Platform method of assessment.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Create a control objective using the Compliance Workspace, Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Control assessment based on GRC attestation template

You can select the option to attest controls using an assessment method. This assessment is an alternative method to the classic assessment that is based on ServiceNow AI Platform method of assessment.

## Pre-requisites to enable smart assessment in Policy and Compliance Management

-   **Smart assessment scoped applications**

    The base system ships the GRC smart assessment template to the users when the GRC: Policy and Compliance Management \(sn\_compliance\) plugin is installed. However, the following scoped applications are required:

    1.  Smart Assessment core \(sn\_smart\_asmt\)
    2.  Smart assessment Migration tools \(sn\_smart\_asmt\_mig\). For more information, see [Migrate a legacy metric type to an assessment template](../../assessment-engine/task/sae-asmnt-tmplt-migrate-metrics-to.md)
    3.  Smart Assessment Connected \(sn\_smart\_asmt\_conn\)
    4.  Smart Assessment Designer \(sn\_smart\_asmt\_desg\). For more information, see [Using the template designer](../../assessment-engine/concept/sae-template-designer.md)
-   **Enable smart assessments system property**

    The **Enable smart assessments on control** system property must be set to true if you want to assess the controls using the assessment method based on GRC attestation template. For more information on the system property, see [Enable smart assessments on control](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#smart-assessment).

-   **Migrate the template**

    Create a new template in Smart Assessment Engine. For more information, see [Creating an assessment template from legacy assessment metric types](../../assessment-engine/concept/sae-asmnt-template-migrating.md).


## Access control limitations for smart assessment user roles

-   **sn\_grc.business\_user and sn\_grc.business\_user\_lite**

    As logged in users they can respond to attestations in **My Attestations** on the Task page of Compliance Workspace, Risk Portal, and Employee Center.

-   **sn\_compliance\_ws.corporate\_compliance\_manager and sn\_compliance\_ws.it\_compliance\_manager**

    Can view and edit the templates.

-   **sn\_compliance.attestation\_creator**

    Can create template category and template migration.

-   **sn\_compliance.user**

    Can read all the assessments related to control category.


## Assessment template category and migration tables

-   **Assessment template categories \[sn\_smart\_asmt\_template\_category\]**

    The **Category role** field has the configuration of the minimum reader role required to read the template of this category. The role must contain sn\_smart\_asmt.template\_reader role.

-   **Assessment template migrations \[sn\_smart\_asmt\_mig\_template\_migration\]**

    Used to migrate the existing source metric type and template category to the new assessment template format.


## Impact of attestation method on control objective and control generation

When the **Enable smart assessments on control** system property is set to true and the Control objective record has the value **Attestation** in the **Attestation method** field, then all the controls that are generated for this control objective record after attestation has values defaulted from the control objective. The **Attestation method** field value defaults to **Attestation**.

**Note:** The old control objectives will have default assessment method as classic assessment. If you would like to explore smart assessment method, then you should make necessary changes to either the control objective or the control. The control can be updated only if it does not have any control objective. After you create a new record, you can either opt the classic attestation or attestation as your attestation method.

-   If the control objective is associated with the control, then the generated control inherits the **Attestation method** and **Attestation** field values.
-   If a control is created from a control objective, the **Attestation method** and the **Attestation** fields are pre-populated, if the control objective has values in these fields.

    **Note:** The controls are automatically created if the **Create controls automatically** option is enabled for the control objective.

    The **Attestation method** field is read only. However, you can edit the **Attestation** field and select a different template for attestation. Any changes done to the control objective are automatically updated in the associated controls.

-   After the control is saved and attested, the **Attestations** related list appears in the Control record. This related list displays all Assessment instances that are in Open and Completed states.

    If the assessment method is changed from Classic attestation to Attestation in the control objective record, then the changes are reflected in all the control records generated for the control objective. Up until the control moves to the Attest state, the **Attestation method** and **Attestation** field values can be updated.

-   If the control was previously generated opting the classic attestation method, then the **Classic attestation** related list has the details of all completed attestations.
-   If the control is moved to the Draft state by selecting the **Return to Draft** button, all the assessments that were active are canceled. Similarly, if the control retires, all related assessments are canceled as well.
-   If the control is marked **Exempt** owing to a policy exception, all the associated assessments are canceled. However, if the **Exempt** option is cleared for the control and if the control is in the Attest state, then the assessments are re-triggered. And, all the fields in the Attestation section of the control becomes read only.
-   If a policy is associated to the control objective, and the policy is published, then all the fields of the control objective form become read only.
-   When the control moves to the Attest state, the assessments are triggered. An email notification is sent to the control owner and the attestation respondents of the control, with the subject line referencing the new attestation name of the control number and the due date by which the attestation must be completed.
-   If an attestation fails for one of the controls generated from a control objective, then the control becomes non-compliant and an issue is created. Or, if the control has an issue that already exists, then the **Issue source** field is updated. If the control moves to the Attest state and if the attestation passes, then the existing issues are closed, and the control becomes compliant.

-   You can respond to the attestations from any of these portals:
    -   [Respond to attestations from the Employee Center](../task/smart-assessment-employee-center.md).
    -   [Respond to attestations on the Risk Portal](../task/smart-assessment-risk-portal.md).
    -   [Respond to attestations from Tasks page of Compliance Workspace](../task/smart-assessment-task-page-ws.md).
-   To view the Control objective and Control form changes, see:
    -   [Create a control objective using the Compliance Workspace](../task/create-ctrl-objective-ws.md).
    -   [Create a control using the Compliance Workspace](../task/create-control-ws.md).
-   To view the attestation widgets in the control and control objective overview pages, see [User interface changes for assessments based on GRC attestation](smart-assessments-ui.md).
-   To view the control attestations in 360° view, see [360° Relationship Visualization for Policy and Compliance Management](../../grc-policy-and-compliance/concept/grc-policy-data-navigtor.md).

