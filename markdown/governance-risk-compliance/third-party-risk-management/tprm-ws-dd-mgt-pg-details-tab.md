---
title: Due diligence request process management
description: From the Details tab, you can view and adjust the due diligence request information for a third party. You can also log external-facing comments and private work notes, attach files, and track request updates in the activity stream.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Due diligence request process management

From the Details tab, you can view and adjust the due diligence request information for a third party. You can also log external-facing comments and private work notes, attach files, and track request updates in the activity stream.

The **Details** tab for a due diligence request displays information in the following sections:

## Third-party due diligence request

<table id="table_drw_dbj_fyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

For each due diligence request, the system auto-assigns a unique ID number that starts with the text DDR.

</td></tr><tr><td>

State

</td><td>

Current state in the due diligence process: IRQ, external due diligence, approval, contract risk, or closed.

</td></tr><tr><td>

Request Type

</td><td>

-   **Onboard a new engagement.** Start the onboarding process for a new engagement with an existing third party.
-   **Reassess an existing engagement.** Reassess an existing engagement when the conditions change. For example, let's say that you hear adverse news or have changes in your third-party's supply lines. You might want to reassess the risk by conducting additional due diligence.
-   **Reassess an existing engagement for contract renewal.** Reassess the risk before your organization renews the contract with a current third party or engagement by conducting due diligence.
-   **Offboard an engagement with due diligence.** Determine if offboarding \(terminating the relationship\) with an engagement is the optimal course of action by conducting due diligence. For example, it might be too risky to switch third parties or engagements even if their current performance doesn’t meet expectations.
-   **Offboard an engagement with NO due diligence.** Request that an engagement be permanently terminated when an engagement ends or you want to switch to a different third party for other reasons. In this case, you typically don't need to conduct additional due diligence. The process does, however, include the normal Inherent Risk Questionnaire \(IRQ\) process to confirm that the services provided by the engagement will no longer continue.

</td></tr><tr><td>

Priority

</td><td>

Priority of the request.-   **1 - Critical**
-   **2- High**
-   **3 - Moderate**
-   **4 - Low**
-   **5 - Planning**

</td></tr><tr><td>

Third party

</td><td>

Third party with which the request is associated.

</td></tr><tr><td>

Annual spend

</td><td>

Money that is spent with the third-party organization in one year.

</td></tr><tr><td>

Engagement

</td><td>

Engagement with which the request is associated.

 **Note:** After the due diligence request is submitted by the requester, the TPR manager or due diligence request owner can update this field to an existing engagement by selecting the magnifying glass icon ![](../../../reuse/icons/product-icons/magnifying-glass-outline-24.svg). This helps avoid onboarding existing engagements.

</td></tr><tr><td>

Skip contract risk process

</td><td>

Option to skip the contract risk process. When you select the check box, you bypass the `contract negotiation` state. The **Contract start date** and **Contract expiration date** fields are replaced with **Engagement start date** and **Engagement expiration date**. See [Contract Risk process](../concept/tprm-workflow-in-workspace.md#def_contract_risk_process).

**Note:** After the Third-party risk \(TPR\) manager approves the request, it won’t be sent to the contract negotiators, and the request is closed.

</td></tr><tr><td>

Requestor

</td><td>

Creator of the request.

</td></tr><tr><td>

Opened

</td><td>

Date the request was opened.

</td></tr><tr><td>

Contract start date, Expiration date

</td><td>

Preferred dates for the beginning and end of interactions with the engagement.

</td></tr><tr><td>

Engagement start date, Engagement expiration date

</td><td>

Preferred dates for the beginning and end of interactions with the engagement.

</td></tr><tr><td>

IRQ assessor

</td><td>

User at your organization that responds to the IRQ. See [IRQ process management](tprm-ws-dd-mgt-pg-irq-tab.md).

</td></tr><tr><td>

Contract negotiator

</td><td>

User at your organization that prepares, negotiates, and approves the contract.

</td></tr><tr><td>

Assignment group

</td><td>

Qualified group of individuals available to work on the request.

 For new requests, the **Assignment group** is set to **Due diligence request assigners**. The system sends an email notification to all users in the group that is specified in the **Assignment group**. The message states that the request was received and is in the **New** state. The message also includes a link to the details page for the request.

 On the due diligence request form:

 -   Any member of the group can select **Assign to me** or set the **Owner** field to any other member of the group.
-   A TPR manager or TPR assessor can clear the **Assignment group** field or change the value to select from different TPR assessors in the **Owner** selection list.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to the due diligence request.

 The owner is responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, owners are notified when an assessment reaches a particular milestone. The owner must have the TPR manager or TPR assessor role.

</td></tr><tr><td>

Short description, Description

</td><td>

Description of the request that helps others to understand the creator's intent and requirements.

</td></tr></tbody>
</table>## Third-party basic information

<table id="table_tpddr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Third-party name

</td><td>

Name of third party with which the request is associated.

</td></tr><tr><td>

DUNS number

</td><td>

Unique numeric identifier for the single business entity. A DUNS number isn’t legally required for a business.**Note:** In the Third-party due diligence request \[sn\_tprm\_dd\_request\] table, there are two DUNs number columns: vdr\_duns\_number indicates the third party DUNs number and eng\_duns\_number indicates the engagement DUNs number.

</td></tr><tr><td>

Street, City, State/Province, ZIP/Postal code, Country, Phone, Fax

</td><td>

Standard contact information for the third-party organization.

</td></tr><tr><td>

Website

</td><td>

URL for the third party.

</td></tr><tr><td>

Type

</td><td>

Type of third party.

</td></tr><tr><td>

Industry

</td><td>

The industry in which the third party is involved.

</td></tr><tr><td>

First name, Last name, Title, Email, Phone

</td><td>

Standard contact information for the third-party contact.

</td></tr></tbody>
</table>## Engagement basic information

<table id="table_ebi"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Engagement name

</td><td>

Name of engagement with which the request is associated.

</td></tr><tr><td>

Type

</td><td>

Type of product or service for this engagement.

</td></tr><tr><td>

Use the corporation address

</td><td>

Option to use the same corporation address as the third party. When you select the check box, auto-populate the related fields with the third-party organization contact information.

</td></tr><tr><td>

Street, City, State/Province, ZIP/Postal code, Country, Phone, Fax

</td><td>

Standard contact information for the engagement organization.

</td></tr><tr><td>

Use the same contact

</td><td>

Option to use the same contact information as the third party. When you select the check box, the related fields are auto-populated with the third-party contact information.

</td></tr><tr><td>

First name, Last name, Title, Email, Phone

</td><td>

Standard contact information for the engagement contact who will respond to the questionnaires.

</td></tr></tbody>
</table>## Risk ratings

Fields are auto-populated by the current stage of the IRQ process for the request.

|Field|Description|
|-----|-----------|
|Inherent assessment rating|Rating determined by the IRQ process.|
|Risk intelligence rating|Rating determined by data from a risk intelligence service provider.|
|Third-party assessment rating|Rating determined by responses during the external assessment process.|
|Engagement rating|Rating determined for the engagement.|

## Progress summary

Status of the due diligence processes. The fields are auto-populated by the current stage of each assessment for the due diligence request.

-   Inherent risk assessment
-   Third-party risk assessment
-   Engagement risk assessment

## Compose, Activity, Attachments

The **Compose section** on the **Details** tab enables you to permanently add text to the record. The Activity section is updated with any actions on issues and tasks, submissions to TP contacts, and also with work notes and comments that users add to the record. Add text in the following fields as needed:

-   **Work notes \(Private\)**: Information about the third-party risk assessment. Work notes are visible only to internal users who are assigned to the process.
-   **Comments**: Comments about the third-party risk assessment are visible both to internal users and to third-party contacts.

-   **[Request third-party risk due diligence request form](tprm-dd-form.md)**  
The due diligence request form captures all the initial information that you need to start the due diligence process. Any employee within your organization can request due diligence. If you’re selecting an existing third party, a significant portion of the information is automatically filled in.

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Requesting third-party risk due diligence](../../grc-vendor-risk/concept/tprm-requesting-tpr-due-diligence.md)

[Request due diligence for a third-party engagement](../task/tprm-ws-request-dd-for-engagement.md)

[Offboarding an engagement without conducting due diligence](../concept/tprm-dd-request-offboard-no-dd.md)

[Request third-party risk due diligence request form](tprm-dd-form.md)

[Create New Third-party engagement form](../../grc-vendor-risk/reference/tprm-create-engmt-form.md)

