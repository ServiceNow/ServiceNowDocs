---
title: IRQ process management
description: The first internal step after an engagement request is approved is to start the IRQ process to scope the risk by determining the third party's risk score.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# IRQ process management

The first internal step after an engagement request is approved is to start the IRQ process to scope the risk by determining the third party's risk score.

## Accessing the IRQ process

On the Due diligence management page, select the **DDR** number for any due diligence request and then select the **Internal assessments** tab.

The tab displays the list of all IRQ processes for the engagement request. For each IRQ process, the system auto-assigns a unique ID number that starts with the text INA.

![Accessing the Vendor Management Workspace.](../image/tprm-ws-inherent-risk-assess-tab.png)

## Viewing the list of internal risk assessments

-   **Internal assessments tab**

<table id="table_drw_dbj_fyb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

For each IRQ process, the system auto-assigns a unique ID number that starts with the text INA.

 Select an INA number to work on the Internal assessments page to the **Risk overview** tab.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Name, Assigned to, Risk rating

</td><td>

Data from the engagement request.

</td></tr><tr><td>

State

</td><td>

The current state of the internal assessment: Draft, Awaiting response, Response received, or Closed.

</td></tr><tr><td>

Respondents

</td><td>

Users who responded to the request.

</td></tr></tbody>
</table>-   **Risk overview tab on the Internal assessments page**

    For each IRQ process, the system auto-assigns a unique ID number that starts with the text INA. Select an INA number to work on the IRQ process on the Internal assessments page.

    ![Select the INA number to work on the Internal assessments page.](../image/tprm-ws-dd-mgt-tp-irq-ovw-tab.png)

    -   The symbols indicate the state of each stage in the IRQ process for the request.

        ![IRQ process stages.](../image/tprm-ws-irq-stage-indicators.png)

    -   **Questionnaire requests** section: List of questionnaires that are associated with the third party. You can view each questionnaire by selecting the **Name**.
    -   **Tracking** section: Count of assessments associated with the third party that are in the **Open**, **Overdue**, and **Closed** state.
-   **Details tab on the Internal assessments page**
    -   **Internal assessment section**: General information on the third party and schedules for the overall assessment and questionnaire due dates from the engagement due diligence request.
    -   The **Compose section** on the **Details** tab enables you to permanently add text to the record. The Activity section is updated with any actions on issues and tasks, submissions to TP contacts, and also with work notes and comments that users add to the record. Add text in the following fields as needed:

        -   **Work notes \(Private\)**: Information about the third-party risk assessment. Work notes are visible only to internal users who are assigned to the process.
        -   **Comments**: Comments about the third-party risk assessment are visible both to internal users and to third-party contacts.
    -   The **Third-party overview** section provides key information on the third party that is associated with the engagement request.
-   **Questionnaire templates tab on the Internal assessments page**

    The tab lists all open IRQs. Select a questionnaire name to view the details.

-   **Scales tab on the Internal assessments page**

    The tab lists the definitions of the calculated rating and tier values. See [Set up risk rating scales for scoring](../../grc-vendor-risk-implementation/task/tprm-risk-rating-scales-config.md) for instructions for defining the settings.

-   **Questionnaire requests tab on the Internal assessments page**

    All values on the tab come from the internal assessments that have been conducted on the third part in the engagement.

<table id="table_fyw_dwj_fyb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

When a questionnaire template is added to an assessment and sent out, the system generates assessment instances for each template. Each of these instances is automatically assigned a unique ID number that starts with the text AINST.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Assessment number

</td><td>

For each external risk assessment, the system auto-assigns a unique ID number that starts with the text VRA.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Metric type

</td><td>

Questionnaire that determined the questionnaires used in the assessment.

</td></tr><tr><td>

Assigned to

</td><td>

User that is responsible for managing and responding to the IRQ.

</td></tr><tr><td>

Due date

</td><td>

Deadline for third party to respond to and return all questionnaires.

</td></tr><tr><td>

State

</td><td>

Current stage of the IRQ process for the engagement request.

</td></tr><tr><td>

Internal risk score

</td><td>

An engagement risk-scoring rule specifies component criteria that determine which engagements are selected for assessment. For example, a rule could enable assessments for engagements that involve more than $40,000 annual business. Engagement scoring rules apply only to engagements.

 See [Define engagement risk scoring rules](../../grc-vendor-risk/task/tprm-engagement-scoring-rules-df.md).

</td></tr></tbody>
</table>
-   **[Create new internal assessment form](../../grc-vendor-risk/reference/create-int-assess-form.md)**  
Use the internal assessment form to capture all the information that you need to create an internal assessment. As a third-party risk assessor, you can create an assessment template.

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Assessing your third-party risk](../../grc-vendor-risk/concept/tprm-assessing-tpr.md)

[Respond to an internal assessment](../task/tprm-irq-respond-to.md)

