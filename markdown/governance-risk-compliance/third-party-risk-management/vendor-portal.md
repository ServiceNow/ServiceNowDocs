---
title: Managing the Third-party portal
description: Third-party contacts respond to questionnaires, requests for documentation, tasks, and issues on the Third-party portal. The portal is the point of interaction between third parties and risk assessors.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Managing the Third-party portal

Third-party contacts respond to questionnaires, requests for documentation, tasks, and issues on the Third-party portal. The portal is the point of interaction between third parties and risk assessors.

## Third-party contacts

Third-party contacts are the individuals that represent the third party. By using the third-party portal, they can respond to questionnaires, work on tasks, and address issues that your third-party risk assessment team raises. Third-party contacts are either primary or secondary contacts. The primary contact is the assigned individual who receives the assessment questionnaires. Each third party must have at least one primary contact. The Third-party editor \[vendor\_editor\], Third-party Risk \(TPR\) manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], or the primary contact can create third-party contacts.

You assign the **primary contact** responsibility to the third-party contact who can directly answer assessment questions or assign another contact at the third party to answer the questions. Primary contacts can manage other contacts for the third party.

Third-party contacts are automatically assigned two roles: vendor\_contact and snc\_external. The vendor\_contact role provides third-party contacts with access to the Third-party portal, while the snc\_external role is a safeguard that restricts access only to the portal. The snc\_external role helps prevent any unauthorized entry into your instance. For more information, see [Set up third-party contacts](../../grc-vendor-risk-implementation/task/tprm-tp-contact-config.md).

**Note:** Third-party contacts see your organization's name in all references on the Third-party portal. You specify the name in the `sn_vdr_risk_asmt.company.name` property setting. See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

## Tasks for third-party contacts

The primary third-party contact can perform the following tasks:

-   Delegate questionnaires, tasks, and issues to other third-party contacts.
-   View and update the third-party contact information.
-   Update the notification preferences.

Secondary third-party contacts can use the portal to perform the following tasks:

-   View and respond to "assigned to me" assessments.
-   Change a password or request a new password.

**Important:** The third-party contact role should be used only for external contacts. The role prohibits access to the ServiceNow AI Platform and grants access only to the Third-party portal.

Third-party contacts see the portal as shown in the following example.

![Third-party portal as seen by a third-party contact.](../../grc-vendor-risk-implementation/image/vrm-assessment-portal.png "Third-party portal example")

## Questionnaire and document request states

Progress is tracked in assessment requests and the progress is indicated by the state of the requests within the questionnaires and document requests. Here are the possible states for requests.

-   **New**

    After questionnaires and document requests are sent out, they are in the **New** state.

-   **In progress**

    After the third-party or engagement contact has started providing responses in a questionnaire or document request, the requests is in the **In progress** state.

-   **Completed**

    After the third-party or engagement contact has provided responses for all questions in a questionnaire or document request and saved, the request is in the **Completed** state.

    **Note:** After all requests have entered the Completed state, you must return to the assessment page and submit the assessment.


## Responding to questionnaires using a Microsoft Excel template

Third-party contacts can use a Microsoft Excel template to respond to questionnaires by downloading the template, completing it, and importing the final version into the Third-party portal. The Microsoft Excel questionnaire template contains instructions for filling out the template. This enables third-party contacts to provide information outside the third-party portal, streamlining the due diligence process. For more information, see [Using a Microsoft Excel spreadsheet template for external questionnaires](../../grc-workspace-vrm/concept/tprm-excel-template-support.md) and [Respond using a Microsoft Excel template](../../grc-workspace-vrm/task/tprm-tpcontact-use-excel.md).

## Responding to assessments using a SIG questionnaire

Third parties can use the Shared Assessments Standardized Information Gathering questionnaire \(SIG\) to provide assessment documentation in the Third-party Risk Management application. The third-party contact can upload the pre-filled SIG spreadsheet or respond to a form-based questionnaire that is imported to the instance. For more information, see [Using the SIG questionnaire for a risk assessment](tprm-sig-use-and-support.md) and [Respond using the SIG](../task/tprm-tpcontact-use-sig.md).

**Note:** Third-party contacts can reassign a questionnaire to another team member by selecting the more actions menu icon ![](../image/context-menu-db-element-ac.png) and selecting **Reassign**. After reassigning the questionnaire, they lose access to the questionnaire.

## Launching the portal

Third-party contacts launch the portal by using **\[your instance URL\]/svdp**\).

## Learning to use the portal—the FAQ page

Third-party contacts can select **FAQ** to view answers to common questions, such as how to invite additional users to the portal and how to assign primary contacts to third-party or engagement records.

## Managing third-party contacts

Users in your organization with the TPR assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\] use TPRM to manage the following third-party contact activities:

-   Create a login for a new third-party contact.
-   Enable or disable a third-party contact login.
-   Reset a password for a third-party contact.
-   Assign a user role to a third-party contact.
-   Assign a third-party contact to an assessment.
-   View and update the customer contact information.
-   Access the completed assessments.

For more information, see [Set up third-party contacts](../../grc-vendor-risk-implementation/task/tprm-tp-contact-config.md) and [Manage the access for your third-party contacts](../task/tprm-manage-tp-contact.md).

**Note:** If necessary, you can respond on behalf of third parties or engagements to questionnaires. See [Respond to a questionnaire for a third party or engagement](../task/tprm-respond-for-tp.md) for more information.

The **Allow assessors to answer/edit questionnaires for third-party contacts** property \(**sn\_svdp.allow\_assessor\_edit**\) must be active. For more information on configuring this property, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

## Assessment assignments

Third parties and engagements can each have more than one primary or secondary contact. A third party can have multiple contacts, but each contact belongs to only one third party. Engagements are more flexible; an engagement can include many contacts, and a single contact can participate in multiple engagements. These relationships determine how external assessments are assigned in the Classic assessment engine and the Smart Assessment Engine.

External assessments are always assigned to primary contacts. When multiple primary contacts exist, the system automatically selects the alphabetically first primary contact as the initial assignee. The rules for who else is assigned and who can submit depend on which assessment engine your organization uses.

-   **Classic assessment engine**

    When a Classic external assessment is generated for a third party or engagement, the system assigns the questionnaire to only one primary contact—the alphabetically first primary contact. Classic assessments don’t designate a questionnaire owner; the assigned primary contact can complete and submit the questionnaire.

-   **Smart Assessment Engine**

    Smart assessments assign the questionnaire to all primary contacts of the third party or engagement. However, the Smart Assessment Engine introduces a questionnaire owner. The questionnaire owner is the alphabetically first primary contact and is responsible for submitting the assessment once all responses are complete.

    -   The owner is selected automatically in alphabetical order by name.
    -   The owner is the only primary contact who can submit the questionnaire.
    -   Other primary contacts can respond to questions but can’t submit unless ownership is reassigned.
    **Note:** If needed, the owner can reassign the questionnaire using the **Reassign** option in the questionnaire’s more actions menu. After reassignment, the previous owner loses access.


**Related topics**  


[E-signatures on questionnaires or document requests](../../grc-workspace-vrm/task/tprm-ws-approve-with-e-sig.md)

[Using a Microsoft Excel spreadsheet template for external questionnaires](../../grc-workspace-vrm/concept/tprm-excel-template-support.md)

[Using the SIG questionnaire for a risk assessment](tprm-sig-use-and-support.md)

[TPRM and the Explicit Roles plugin](vrm-and-explicit-roles-plugin.md)

