---
title: Verify documents uploaded to a grant proposal
description: Verify all documents the applicant has uploaded with the submitted proposal. Flag documents that don't meet requirements and undo accidental flags. From Grants management version 1.41 onward grant program managers can request corrected documents from applicants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-using-gmp-verify-documents.html
release: australia
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [verify documents, document correction, flag documents, grants management]
breadcrumb: [Screen a grant application, Grants Management Proposal Playbook, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Verify documents uploaded to a grant proposal

Verify all documents the applicant has uploaded with the submitted proposal. Flag documents that don't meet requirements and undo accidental flags.From Grants management version 1.41 onward grant program managers can request corrected documents from applicants.

## Before you begin

Role required: sn\_gsm\_grnt\_mgmt.program\_manager, sn\_gsm\_grnt\_mgmt.grant\_director

## About this task

\[Omitted image "psds-gmp-verify-doc-correction.png"\] Alt text: Verify and request correction for applicant documentation for a proposal

Review and verify the files and supporting documentation attached to the application. You can flag documents for further verification, undo accidental flags, or close the case by moving it to Decision.From Grants management version 1.41 onward grant program managers can request corrected documents from applicants.

Documents are organized into three sections: Requires verification, Verified, and Flagged. Each section displays a count of documents in that state.

## Procedure

1.  Select each document in the **Requires verification** list to review that the document has all the required details.

    For each document, you can perform one of the following actions:

    -   Select the checkmark icon to verify the document. The document moves to the **Verified** section.
    -   Select the flag icon to flag the document. The document moves to the **Flagged** section and retains all metadata including file name, size, applicant name, and document type.
2.  To reverse an accidental flag, select the reset status icon on the flagged document row in the **Flagged** section to undo the flagging.

    The document moves back to the **Requires verification** section. No file content or metadata is lost. The Flagged count decrements and the Requires verification count increments.

3.  To request corrected documents from the applicant, select **Request Documents** at the bottom of the Verify documents screen.

    The **Request Documents** button is active only when at least one document is in Flagged status.

    **Warning:**

    Selecting **Request Documents** permanently deletes all flagged documents. This action can't be undone. Before proceeding, verify that you have flagged only the documents that require correction.

    The following actions occur:

    -   The flagged documents are permanently deleted and their status changes to Pending resubmission.
    -   A case task is created and assigned to each applicant who owns a flagged document.
    -   The applicant receives a notification in the applicant portal about the task to re-upload the document.
    -   The case state changes to Awaiting Documentation.
    -   An **Upload Additional Documents** activity is added to the playbook for each applicant with flagged documents.
    The Upload Additional Documents activity closes automatically after the applicant uploads the corrected document and marks the activity complete.

4.  After all documents have been verified and any flagged documents have been resolved, select **Move to Evaluation** to advance the proposal.

    **Note:**

    If documents remain unverified, the playbook does not proceed to the next step and an error appears at the top of the Verify documents activity. Verify that all documents have been reviewed and marked as verified before proceeding.


## Result

The playbook moves to the **Evaluation** stage, where the grant program manager can select the merit reviewer group and release the merit review tasks.

