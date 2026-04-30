---
title: Create a VRM tiering assessment
description: The TPR assessor creates a tiering assessment from the vendor record, initiating the third-party risk tiering assessment life cycle. Also, third-party risk managers can select multiple third parties at a time and trigger multiple third-party risk tiering assessments.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [VRM third-party risk tiering assessments, Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a VRM tiering assessment

The TPR assessor creates a tiering assessment from the vendor record, initiating the third-party risk tiering assessment life cycle. Also, third-party risk managers can select multiple third parties at a time and trigger multiple third-party risk tiering assessments.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

The more complete IRQ process replaces tiering.

**Important:**

In the TPRM application, the IRQ is an internal questionnaire that improves the original tiering assessment process. IRQs enhance internal risk assessments with increased flexibility, control, and scalability. Unlike a tiering assessment where external questionnaires are determined solely by the risk tier, an IRQ can dynamically trigger external questionnaires based on both respondents' answers and risk tier.

To enable a seamless transition to TPRM, you have the option to duplicate existing tiering assessments and designate them as IRQ internal assessments. Risk tiering is supported as an unchanging legacy process.

## Procedure

1.  Use either of the following methods to start the process:

    -   On the **Risk** tab of the Vendor Management Workspace, select **Create tiering assessment** in the Quick actions box.
    -   Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Submission Rules** &gt; **Tier Based Submission**.
2.  Fill in the fields on the **Details** tab and then select **Save**.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the tiering assessment.

</td></tr><tr><td>

Short description

</td><td>

Description of the tiering assessment.

</td></tr><tr><td>

Number

</td><td>

For each risk tiering assessment, the system auto-assigns a unique ID number that starts with the text VTA.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Applies to

</td><td>

The entity to which the assessment applies:-   **Third party**: The parent organization.
-   **Engagement**: The organization within the third party that will supply the product or service.


</td></tr><tr><td>

Third party

</td><td>

Vendor being assessed.

</td></tr><tr><td>

State

</td><td>

-   Draft: Default value while the assessment is being defined.
-   Awaiting Response
-   Tiering Assignment
-   Closed


</td></tr><tr><td>

Assigned to

</td><td>

TPR manager assigned to manage the tiering assessment process.

</td></tr><tr><td>

Tier level

</td><td>

Risk tier for the third party. -   Critical
-   High
-   Moderate
-   Low
-   Minor
The results of the tiering assessment and risk assessment help to determine the value. The TPR manager can override the value.

</td></tr><tr><td>

Tiering assessors

</td><td>

Internal assessors responsible for completing the tier assessment.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Tiering Assessment Schedule|
    |Planned duration|Estimated duration of the assessment.|
    |Planned start date / Planned end date|Date and time that work on the tiering assessment is expected to begin and end.|
    |Actual duration|Amount of time it took to complete the tiering assessment. This value is calculated using the **Actual state date** and **Actual end date**.|
    |Actual start date / Actual end date|Date and time that work on the tiering assessment began and was completed|
    |Notes and Comments|
    |Work notes|Information about the assessment process. Work notes are visible to users who are assigned to the issue.|
    |Additional comments \(Customer visible\)|Public information about the third-party risk assessment.|

3.  Select **Save**.

    The **Compose section** on the **Details** tab enables you to permanently add text to the record. The Activity section is updated with any actions on issues and tasks, submissions to TP contacts, and also with work notes and comments that users add to the record. Add text in the following fields as needed:

    -   **Work notes \(Private\)**: Information about the third-party risk assessment. Work notes are visible only to internal users who are assigned to the process.
    -   **Comments**: Comments about the third-party risk assessment are visible both to internal users and to third-party contacts.
4.  Select the **Tiering Questionnaires** tab, select the questionnaires to use for the tiering assessment, and then select **Add** and select **Add**.

    **Note:** The base system includes a sample tiering questionnaire called **Basic**. Modify and save the questionnaire to meet your needs.

5.  Select **Save**.

6.  When all settings are correct, select **Submit Assessment**.


