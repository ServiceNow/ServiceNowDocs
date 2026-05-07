---
title: Review questionnaire to approve or reject requets
description: Approvers review the questionnaire and make approval/rejection decisions based on the provided information. Remediation owners must fill out the questionnaire before submitting for approval, if questionnaire configuration was selected during exception rule configuration..
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Unified Approvals View, Use, Unified Security Exposure Management, Security Operations]
---

# Review questionnaire to approve or reject requets

Approvers review the questionnaire and make approval/rejection decisions based on the provided information. Remediation owners must fill out the questionnaire before submitting for approval, if questionnaire configuration was selected during exception rule configuration..

## Before you begin

Role required: **sn\_vul\_cmn.smart\_assessment\_reader**

## About this task

The following is the workflow of the smart assessment adaption:

-   **Request for Exception/False Positive** when you request an exception or mark something as a false positive, the system checks if a questionnaire is required.
-   If the **questionnaire option is enabled**, a **mandatory message** will prompt the user to complete the questionnaire before proceeding with the approval process.
-   **Draft State**: The **Change Approval** \(CA\) record will remain in the draft state until the questionnaire is submitted, and the Vulnerability Item \(VIT\) will be in the open state.
-   **Approver View**: Once remediation owners fill out the questionnaire and submit it, the Change Approval \(CA\) and Vulnerability Item \(VIT\) records move to in review status. Approvers can review the smart assessment questionnaires from “All &gt; My Approvals” or view them in the review state. The VIT will be moved to deferred state upon approval of the records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Approvals**to view the questionnaire in the list view as well as inside the request form view.

2.  Once the record is **Approved**, VIT is moved to Deferred state.

3.  You can view the questionnaire via a link submitted by the Remediation Owners in the request information in Overview page.


**Parent Topic:**[Unified Approvals View](../concept/sem-approval-view.md)

