---
title: Use case for False positive or Request Exception Questionnaire
description: Scenario when the questionnaire for False Positive or Request Exception is raised but not filled completely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-ques-for-false-positive-or-request-exp.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Questionnaire support in Exception Management via Smart Assessment, Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Use case for False positive or Request Exception Questionnaire

Scenario when the questionnaire for False Positive or Request Exception is raised but not filled completely.

When the questionnaire for False positive or Request exception is raised but not filled completely, the Change Approval \(CA\) record goes into “Draft” state. If you want to raise an exception from the same category, you are navigated to the previous questionnaire following a pop-up note regarding the same. In case you want to raise a False Positive record instead of an existing request exception, the system overrides the False positive Change Approval record. It then creates a new False Positive Change Approval record.

In case the questionnaire is half filled and the same Vulnerability Item \(VIT\)/ or any ITEM is opened in classic view, you’re navigated to the workspace questionnaire to fill the remaining data if the same type of request is raised again. If the questionnaire in classic view is selectively filled and the same item is opened in the workspace, then the classic view questionnaire is opened in the workspace.

When a previously approved or rejected request is resubmitted, the change approval record tracks the **Resubmission context** \(After Approval or After Rejection\) to provide approvers with visibility into the history of the request.

## Flow differences between False Positive and Request Exception

The two questionnaire flows share a draft-state model but differ in how the resulting record transitions on approval and how a rejection can be recovered from:

|Aspect|False Positive flow|Request Exception flow|
|------|-------------------|----------------------|
|On approval, the finding transitions to|**Closed** with reason **False positive**.|**Deferred** until the configured **Until** date, then reverts to **Open**.|
|Required questionnaire evidence|Scanner output, screenshots, or reproduction notes showing the finding is incorrect.|Business justification, compensating-control description, and timeline to remediation.|
|Resubmission after rejection|Allowed only if new evidence is attached. The new record's **Resubmission context** is set to After Rejection.|Allowed; the requester may adjust the **Until** date and justification. The new record's **Resubmission context** is set to After Rejection.|
|Resubmission after approval \(extension\)|Not applicable — a closed false positive does not need extension.|Available via **Request Extension**. The new record's **Resubmission context** is set to After Approval.|

**Note:** If a questionnaire is half-filled in classic view and the same item is then opened in the workspace, the workspace inherits the in-progress responses. The reverse navigation works the same way.

