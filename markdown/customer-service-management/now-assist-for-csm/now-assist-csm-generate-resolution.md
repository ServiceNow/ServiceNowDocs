---
title: Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)
description: Generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.Use the Now Assist context menu in the resolution notes field of the case form in both Core UI \(UI16\) and Workspace to create resolution note.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI skills, Now Assist for CSM, Customer Service Management]
---

# Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)

Generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.

## About this task

Watch this video to learn how to generate the resolution notes for a case.

Generate resolution notes for a case 

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

In CSM Configurable Workspace and Core UI, you can generate the resolution information for a case by selecting **Propose Solution** on the case record. This UI Action displays the Propose Solution modal. Using this modal, you can select a resolution code, add information about the cause of the issue, and review and edit the resolution notes text.

**Note:** The Propose Solution UI action is available to the customer service agents who have assigned cases in the Open state.

You can also generate resolution information on demand from the Now Assist panel.

**Note:** The resolution notes generation skill requires a minimum of 50 words in the case record to generate the resolution notes. If the resolution notes cannot be generated, the system displays a message below the **Resolution notes** field.

**Note:** You can skip this if you're using the Now Assist Content menu experience for Resolution Notes Generation skill.

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

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

## Generate resolution notes in case form

Use the Now Assist context menu in the resolution notes field of the case form in both Core UI \(UI16\) and Workspace to create resolution note.

### Before you begin

Role required: admin

### About this task

In both the CSM Configurable Workspace and Core UI, you can generate resolution notes for a case by using the Now Assist context menu within the resolution notes field in the case form.

An agent can do these actions by using the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png):

-   Generate resolution notes based on the case context.
-   Refine the recommendation by elaborating or shortening the content.

**Note:** The case must be in the open state.

### Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a customer service case that is in an open state.

2.  Navigate to the Resolution notes field in the case form.

3.  Select the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png).

    Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) generates a recommended text that is based on the context of the case.

    ![Resolution notes is generated](../image/now-assist-csm-resolutionnotes-caseform-generate.png "Generate resolution notes using the Now Assist icon")

4.  Select **Insert** to add the generated content into the resolution notes field.

5.  Review the generated content and select **Refine** to modify the content.

    You get the option to either elaborate or shorten the content as needed.

    ![Shorten or elaborate the resolution note](../image/now-assist-csm-resolutionnotes-caseform-refine.png "Refine resolution notes using the Now Assist icon")


