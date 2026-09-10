---
title: Verify and screen documents uploaded to grant proposal application by an applicant
description: Verify all documents the applicant has uploaded with the submitted proposal. Flag documents that do not meet requirements, and reverse a flag that was applied by mistake. From Grants management version 1.41 onward, grant program managers can also request corrected documents from applicants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-using-gmp-verify-documents.html
release: zurich
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Screen a grant application, Grants Management Proposal Playbook, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Verify and screen documents uploaded to grant proposal application by an applicant

Verify all documents the applicant has uploaded with the submitted proposal. Flag documents that do not meet requirements, and reverse a flag that was applied by mistake.From Grants management version 1.41 onward, grant program managers can also request corrected documents from applicants.

## Before you begin

Role required: sn\_gsm\_grnt\_mgmt.program\_manager, sn\_gsm\_grnt\_mgmt.grant\_director

## About this task

\[Omitted image "psds-gmp-verify-doc-correction.png"\] Alt text: Verify and request correction for applicant documentation for a proposal

Review and verify the files and supporting documentation attached to the application. Here, you can flag documents for further verification, reverse an accidental flag, or close the case by moving it directly to Decision.From Grants management version 1.41 onward, grant program managers can also request corrected documents from applicants.

Documents are organized into three sections: Requires verification, Verified, and Flagged. Each section displays a count of the documents in that state.

## Procedure

1.  Select each document in the **Requires verification** list to verify that the document has all the required details, then select the checkmark.

    Selecting the checkmark moves the verified documents into the **Verified** section.

2.  If the document does not meet the requirements set forth by the application guidelines, select the flag icon to flags the document.

    Flagging the document enables the Grant Program Manager to request and notify the applicant that the documentation needs their attention. If the document is flagged, it moves to the **Flagged** section.

3.  To reverse a flag that was applied by mistake, select the reset status icon on the flagged document row in the **Flagged** section.

    The document moves back to the **Requires verification** section. No file content or metadata is lost.

4.  To request corrected documents from the applicant, select **Request Documents** at the bottom of the Verify documents screen.

    The **Request Documents** button is active only when at least one document has a Flagged status.

    **Warning:**

    Selecting **Request Documents** permanently deletes all flagged documents. This action cannot be undone. Before proceeding, verify that you have flagged only the documents that require correction.

    The following actions occur:

    -   The flagged documents are permanently deleted and their status changes to Pending resubmission.
    -   A case task is created and assigned to each applicant who owns a flagged document.
    -   The applicant receives a notification in the applicant portal about the task to re-upload the document.
    -   The case state changes to Awaiting Documentation.
    -   An **Upload Additional Documents** activity is added to the playbook for each applicant with flagged documents.
    The Upload Additional Documents activity closes automatically after the applicant uploads the corrected document and marks the activity complete.

5.  Select **Mark as Complete** once all documents have been verified and any flagged documents have been resolved.

6.  Once all documents have been verified, select **Move to Evaluation**.

    **Note:** If the Grant Program Manager does not select the check mark next to each document, the playbook will not proceed to the next step, and an error appears at the top of the Verify documents activity. Ensure all documents have been reviewed and marked as verified before proceeding to the next activity.


## Result

The playbook is now moved to the **Evaluation** stage, where Grant Program Manager can select the Merit Reviewer Group and release the merit review tasks.

