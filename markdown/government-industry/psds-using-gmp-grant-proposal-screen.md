---
title: Screen a grant proposal in the Grants Proposal Playbook
description: You can use the Grants Proposal playbook to review information provided by the applicant, along with other relevant documents. From Grants management version 1.41 onward, during screening, you can also flag documents for verification and request updated documents from applicants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-using-gmp-grant-proposal-screen.html
release: australia
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 3
keywords: [grants management, document verification, document resubmission, screen proposal]
breadcrumb: [Grants Management Proposal Playbook, Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Screen a grant proposal in the Grants Proposal Playbook

You can use the Grants Proposal playbook to review information provided by the applicant, along with other relevant documents.From Grants management version 1.41 onward, during screening, you can also flag documents for verification and request updated documents from applicants.

\[Omitted image "psds-gmp-rev-prop-details.png"\] Alt text: gpm screening view

The Screening stage of the Grants proposal playbook consists of the following tasks:

-   Reviewing the proposal
-   Checking and confirming eligibility
-   Approving new contacts
-   Verifying documents submitted by the applicants

As the grants program manager or the grants program director, you can review the proposal details and the required documents from the proposal. After verifying the documents, you can assign the proposal to yourself, and either reject the proposal or move it to the Evaluation stage. The case details entered by the applicant in the intake stage are displayed to the grant program manager or the grant program director in an accordion view for a comprehensive review experience.

## Document verification

During the Verify documents activity, you can flag documents and request resubmission without losing the audit trail. From Grants management version 1.41, the document verification capability provides enhancements to the **Verify documents** screen:

-   Flag documents: When you flag a document, the document remains in the system and is visible in the Flagged section. Flagged documents retain all metadata including file name, size, applicant name, and document type. Prior to Grants management version 1.41, flagged documents were simply deleted and there wasn’t any options to undo it.
-   Reset status: You can reverse a flagged document by selecting the reset status icon on the flagged document row. The document moves back to the Requires verification section. No confirmation is required, and no file content or metadata is lost.
-   Request documents from applicant: You can request updated documents from the applicant by selecting **Request Documents** at the bottom of the Verify documents screen. This action permanently deletes the flagged document, creates a case task for the applicant to re-upload a new document, and sends a notification to the applicant in the applicant portal.

## How document verification works

From Grants management version 1.41, the document verification capability provides grant program managers the option to flag a document for a re-upload. The document verification flow involves the following process:

1.  The Grant program manager flags a document during the Verify documents activity and provides a reason in the **Message for Applicant** field. The document moves to the Flagged section and the Flagged count increments.
2.  The flagged document is deleted and its status changes to **Pending resubmission**. A case task is created and assigned to the applicant who owns the flagged document.
3.  The case state changes to **Awaiting Documentation**, and an **Upload Additional Documents** activity is added to the playbook.
4.  The applicant receives a notification and can re-upload the corrected document through the applicant portal in the **Upload additional documents** activity.
5.  After the applicant uploads the corrected document and marks the activity complete, the Upload Additional Documents activity closes automatically and the grant program manager can continue the verification.

## Document verification states

From Grants management version 1.141, documents in the Verify documents activity can have the following states:

|State|Description|
|-----|-----------|
|Requires verification|The document has been uploaded by the applicant and is waiting for review by the grant program manager or grant program manager.|
|Verified|The grant program manager has confirmed that the document meets the application requirements.|
|Flagged|The document does not meet the requirements and requires resubmission. Flagged documents remain in the system and retain all metadata.|
|Pending resubmission|A document resubmission request has been sent to the applicant. The original flagged document has been deleted and the applicant has a case task to upload a replacement.|

**Related topics**  


[Check eligibility of an applicant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-check-eligibility.md)

[Verify documents uploaded to a grant proposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-verify-documents.md)

