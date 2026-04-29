---
title: Screen an uploaded document type using the Document Screening Al skill
description: Use Now Assist for PSDS gen-AI to screen documents in the Social Benefits Playbook, classifying document types, validating them against what's expected for the case, flagging issues and providing clear explanations, and giving agents Al-composed messages to send back to constituents with specific resubmission instructions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Screen an uploaded document type using the Document Screening Al skill

Use Now Assist for PSDS gen-AI to screen documents in the Social Benefits Playbook, classifying document types, validating them against what's expected for the case, flagging issues and providing clear explanations, and giving agents Al-composed messages to send back to constituents with specific resubmission instructions.

## Before you begin

Role required: sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.constituent\_agent, sn\_gsm.agency\_constituent\_agent

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The Document screening generative AI skill automatically analyzes documents uploaded by applicants, identifies the type or category of each document \(for example, driver's license, passport, budget, or narrative\), and validates whether the uploaded document matches what was requested in an application checklist. If there is a mismatch, the agent flags it and helps government employees generate Al-assisted messages requesting corrected documentation.

## Procedure

1.  Navigate to a social benefits, license and permit, or information request case in the CSM Configurable Workspace.

2.  Complete the activities in the Review stage once the constituent has uploaded their documents and other supporting information through the Government Service Portal and the case is moved from Intake to Review stage.

    ![Asset analysis summary with comprehensive asset information and list of action items](../image/verify-docs-review-stage.png "Verify documents activity with document screening skill")

3.  Select the document record that you want to analyze.

    Review any documents in the pre-flagged state. Select **View pre-screen summary** to view the reasons why the documents was flagged.

4.  Enter a message in the the ‘Message for applicant’ text area to provide reasoning to the applicant and request a re-upload the pre-flagged documents, then select **Request Documents**.

    Manually type the reasons, or select **Compose message for applicant** to compose the reason summary into an ai-generated message to the applicant. Refine the reasons in a pop-up modal by selecting on the sparkle icon inside the text area to either shorten or elaborate on what was generated. Select **Insert** to add this text to the message to the applicant.

    ![Asset analysis summary with comprehensive asset information and list of action items](../image/doc-screen-skill-compose-message.png "Now Assist-generated correspondence to applicant")

5.  Select **Request Documents** action to request the constituent to re-upload the ‘Pre-Flagged’ documents.

    The Upload additional documents activity will display in the sidebar of the playbook, allowing the agent to review all pre-flagged, re-uploaded documents that the constituent has sent via the Government Service Portal. The agent can also re-upload ‘Pre-Flagged’ documents on behalf of the constituent. The Document screening skill will then re-analyze and mark the documents ‘pre-screened’ or ‘pre-flagged’.

    As an agent, you can manually override the result of a document screening by selecting **Undo**, moving the Document to the **Unverified** stage, where you can:

    -   Manually verify the document by selecting the checkmark icon
    -   Manually flag the document by selecting the flag icon
    -   Re-run the Document screening process for all unverified documents by selecting **Retry pre-screen** in the Screening incomplete modal.
6.  Select **Confirm and complete** to mark the activity as complete once all of the documents have been uploaded, screened, and marked as **Pre-screened** or **Verified**.

7.  Select **Confirm** to proceed.

    Any documents in the **Pre-Screened** state are changed to **Verified**.


