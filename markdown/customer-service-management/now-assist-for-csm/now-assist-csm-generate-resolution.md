---
title: Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)
description: Generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Generate resolution notes in case form, Use, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)

Generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

In CSM Configurable Workspace and Core UI, you can generate the resolution information for a case by selecting **Propose Solution** on the case record. This UI action displays the Propose Solution modal. Using this modal, you can select a resolution code, add information about the cause of the issue, and review and edit the resolution notes text.

**Note:** The Propose Solution UI action is available to the customer service agents who have assigned cases in the Open state.

You can also generate resolution information on demand from the Now Assist panel. For more information, see .

**Note:** The resolution notes generation skill requires a minimum of 50 words in the case record to generate the resolution notes. If the resolution notes cannot be generated, the system displays a message below the **Resolution notes** field.

**Note:** You can skip this if you are using the Now Assist Content menu experience for Resolution Notes Generation skill.

## Procedure

1.  In CSM Configurable Workspace, open a customer service case.

2.  Select **Propose Solution**.

    The system generates a resolution summary and displays the information in the Propose Solution modal, which includes the following fields:

    -   **Resolution code**
    -   **Cause**
    -   **Resolution notes**
    If the **Resolution notes** field on the case record is empty, the resolution notes generation skill adds the information to this field in the modal.

    ![AI-generated resolution information for a case record.](../image/now-assist-csm-propose-solution-modal.png "Propose Solution modal")

3.  Select a **Resolution code** for the case.

    A resolution code describes how the case was resolved. For example, common resolution codes include:

    -   Solved: Fixed by Support/Guidance provided
    -   Solved: Fixed by closing related PRB
    -   Solved by customer
4.  If you know the cause of the customer's issue, add it to the **Cause** field.

    For example, a customer's issue may be the result of a software upgrade.

5.  In the **Resolution notes** field, review the resolution summary and make any necessary corrections.

    Because the information in this field is automatically generated, it's a good idea to review the text and make sure it's accurate. Any changes that you make are saved when you save the case record.

6.  If you want to add the resolution information to the case activity stream, select the **Add resolution notes to comments** check box.

    Selecting this check box makes the resolution notes available to anyone who can view the case activity stream.

7.  Select **Propose**.

    -   The system populates the fields in the Closure Information section of the case record with the information from the Propose Solution modal.
    -   The case moves to the Resolved state.
    -   The resolution is proposed to the customer.

**Parent Topic:**[Generate resolution notes in case form](gen-resolution-notes-in-case-form.md)

