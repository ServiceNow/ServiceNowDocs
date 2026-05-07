---
title: Perform CRI tiering questionnaire to determine the tier value of entity
description: Perform CRI tiering questionnaire on an entity to determine its tier, evaluation controls associated with the tier will be created or updated. Based on the response to the CRI questionnaire from the assessor, the compliance status of each mapped control to a question is determined and the overall compliance score of the entity is calculated.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage control objectives and policies, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Perform CRI tiering questionnaire to determine the tier value of entity

Perform CRI tiering questionnaire on an entity to determine its tier, evaluation controls associated with the tier will be created or updated. Based on the response to the CRI questionnaire from the assessor, the compliance status of each mapped control to a question is determined and the overall compliance score of the entity is calculated.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.it\_compliance\_manager

## About this task

Cyber Risk Institute \(CRI\) focuses on collaborating with financial sector customers and regulators and streamlines the standards in managing compliance in financial organizations. To mitigate the risks, CRI has created a profile as CRI Profile that is based on NIST CSF v2.0 content.

The content is based on NIST CSF v2.0 functions such as identify, protect, detect, respond, recover, and govern that are called as diagnostic statements. These statements map to various citations coming from the industry standards and generalized into common control objectives. When financial institutions comply with these diagnostic statements, they automatically comply with all the regulations and standards enforced by the financial sector.

ServiceNow base system provides this CRI Profile content to customers and they are:

-   Authority documents for CRI Profile.
-   FFIEC CAT is part of CRI Accelerator. For more information, see [Cyber Risk Institute accelerator](../../grc-cri-accelerator/concept/cyber-risk-inst-accelerator.md).
-   NIST CSF content is part of CSF Accelerator. For more information, see [NIST CSF process overview](../../grc-nist-csf/concept/nist-csf-process.md).

The CRI assessment is done in two steps:

-   **CRI tiering questionnaire**

    With CRI, you can tier your organization with a prescriptive set of questions that you take to assess your company. Based on the responses to the assessment, your company is assigned a tier value.

-   **CRI profile assessment**

    After the CRI tiering questionnaire is complete and based on the tier state of your company, you are required to complete the second step that is CRI profile assessment, which determines the compliance status of the controls and the overall compliance score of your company.


## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the lists \(![List icon.](../../grc-cam-workspace/image/ws-list-icon.png)\) icon.

3.  From the Compliance library of Authority documents list on the left pane, select an authority document based on CRI Profile v2.0.

4.  Select the Citations related list to view the citations associated with the authority document, and select a citation.

    Each of these citations have a control objective associated to it.

5.  From the Citation record's overview page, select the Control objective related list.

6.  Select a control objective record and click the Citations related list to see the related citations that are from the CSF Profile v2.0 and FFIEC.

    You will know how the records are mapped to the CSF Profile v2.0 content. You also have the content for FFIEC CAT and NIST CSF v2.0 in the Compliance library – Authority documents. With these content available, you can perform the tiering questionnaire for your company or subsidiary.

7.  From the Lists page select **All entities** and click an entity record.

8.  Select the **Details** related list of the entity record and click the **Class** field.

    Select any entity class, where the **Is CRI** option is enabled for **Cybersecurity Risk Profile \(CRI\)**. This flag determines whether this class is applicable for CRI profile assessment. Any entity related to this class is entitled to be assessed for the CRI tiering questionnaire.

9.  Close the record, and select the Details related list of the entity.

10. Enter the tier details in the Cybersecurity Risk Profile \(CRI\) related list.

    For more information, see

    -   The Entity form in [Create an entity](../../grc-common-workspace/task/create-new-entity-ws.md).
    -   The Related lists in the [Entities section](../../grc-common-workspace/concept/entities-in-risk-ws.md).
11. Select the ![More actions icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) icon and click the **Initiate CRI tiering questionnaire** option.

12. Enter a message in the **Message** field and select the **Initiate tiering questionnaire** button in the CRI tiering questionnaire pop-up.

    After you initiate the tiering questionnaire the **CRI tiering questionnaire** related list appears in the Entity record.

13. Select the **CRI tiering questionnaire** related list and click the assessment instance link.

    You can also respond to the assessment from the **Tier assessments** list of the My pending tasks related list in the Tasks page and from the Employee Portal. Review the tiering assessment instructions and respond to the questions. Based on your response to each question, the tier level of the entity is determined.

    To respond to an attestation, see [Respond to attestations from Tasks page of Compliance Workspace](smart-assessment-task-page-ws.md) and [Responding to assessments](../../assessment-engine/concept/sae-respond-to-asmnt.md).

14. After you submit your assessment, open the entity record to view the tier value in the **Tier** field of the **Cybersecurity Risk Profile \(CRI\)** section.

    Additionally, based on the tier value you can also know the number of controls that are generated based on the control objectives coming from the tier profile.

15. To view the controls mapped to the tier value, select the **Downstream controls** related list.

    After the tier is determined based on the tiering questionnaire, you can now [perform the CRI profile assessment](perform-cri-assess-pc-ws.md).


