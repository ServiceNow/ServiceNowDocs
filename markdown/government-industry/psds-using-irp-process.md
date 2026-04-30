---
title: Process requested documents using the Information Request Playbook
description: Complete the Process stage as your third step in resolving a case using the Information Request Playbook.Upload the documents.Request approval.As a legal reviewer, you can redact sensitive data from PDF documents by either searching keywords or selecting text in Information Request Playbook.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Information Request Playbook, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Process requested documents using the Information Request Playbook

Complete the Process stage as your third step in resolving a case using the Information Request Playbook.

In this stage, you will uploaded and send for review the documents requested by the requester.

## Upload documents requested by an individual or business contact in Social Benefits Playbook

Upload the documents.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Upload the documents needed to fill this request by selecting **New Document** or **Link Document**.

2.  Move to the next activity by selecting **Prepare for Review**.


## Send requested documents for legal or final review in Social Benefits Playbook

Request approval.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Enter any additional work notes or details needed for legal review, and then select **Send for Legal Review**.

    A case task is now created and assigned to the Legal Review assignment group for approval. If the uploaded documents are rejected during the legal review, you may need to make changes and request a review again or move the case directly to the Decision stage.

    **Note:** A legal review group must already have been created. For more information on how to configure legal assignment groups for use with Information Request Playbook, see [../concept/create-or-edit-assignment-group-psds.md](../concept/create-or-edit-assignment-group-psds.md).

2.  After the documents have been approved by the legal review group, document the work done in the work notes, then select **Send for Final Review**.

    The case is moved to the Final Review activity, where the documents and details of the request are reviewed by the Final Review Team assignment group.

    **Note:** A final review group must already have been created. For more information on how to configure review assignment groups for use with Information Request Playbook, see [../concept/create-or-edit-assignment-group-psds.md](../concept/create-or-edit-assignment-group-psds.md).

3.  After the documents have been approved by the Final Review Team, document the work done in the work notes and select **Move to Decision**.

    The documents are now approved to be released to the requester, and the case is moved to the **Decision** stage.


### What to do next

Complete the Decision stage, where the documents will be released to the requester.

## Redact sensitive data from a requested document in Information Request Playbook

As a legal reviewer, you can redact sensitive data from PDF documents by either searching keywords or selecting text in Information Request Playbook.

### About this task

Agents can:

-   Redact manually by selecting text to be highlighted for redaction.
-   Redact via keyword using Search and Redact.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

### Procedure

1.  Open the Information Request Playbook by navigating to Lists in the CSM Configurable Workspace.

2.  Navigate to the **Information Requests** list and select **All**.

3.  Select the case that contains the PDF you wish to redact information from.

4.  Navigate to the **Legal Review** activity in the **Process** stage.

5.  Under the Related Documents card, select the PDF you wish to redact information from.

6.  Select the Redact PDF ![Redact Icon](../image/redactpdficon.png) icon.

7.  To redact using the highlight functionality: select Highlight.

8.  Drag the cursor to form a box over the text you wish to redact.

    A green box will display over the selected text.

9.  Select **Apply Redactions** to redact the highlighted text.

10. Confirm your selection when prompted.

11. To redact using the Search and Redact functionality: enter a keyword you wish to redact, and select Search to parse the document for this keyword.

12. Select **Apply Redactions** to redact every instance of this keyword.

13. Confirm your selection when prompted.

14. Repeat steps 13-14 to redact multiple keywords.

15. Select **Save Changes** to save the redacted version of the PDF.

    Previous versions of the document \(which may contain different redacted text\) are available and can be accessed by a government employee.


### Result

The information is now permanently redacted from the PDF.

