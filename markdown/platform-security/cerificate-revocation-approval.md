---
title: Approve certificate revocation
description: Review and approve certificate revocation requests from the email approval notifications that are sent to your registered email address. Review the approval notification and select the Click here to approve or Click here to reject link to access the protected instance and act. You can also access the approval request and the code-signing quorum request directly from the email.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Quorum Controlled Certificate Revocation, Configure, Code Signing, Platform Security]
---

# Approve certificate revocation

Review and approve certificate revocation requests from the email approval notifications that are sent to your registered email address. Review the approval notification and select the **Click here to approve** or **Click here to reject** link to access the protected instance and act. You can also access the approval request and the code-signing quorum request directly from the email.

## Before you begin

Role required: sn\_cse.codesigning\_admin, approver\_user

## Procedure

1.  Access the protected instance by following the links provided in the notification email.

2.  Review the transaction requests under the Approvals menu.

3.  Approve the task by selecting **Approve**.

4.  In the approval confirmation page, select **Yes** to access the specific code signing quorum request.

5.  Review the Code Signing quorum request and add any additional notes in the **Comments** menu, if necessary.

6.  Select **Update**.


## Result

The Code Signing quorum request is approved. If you have enabled the MID Server restart while exporting the revocation request, the MID Server restarts for the request to be activated.

**Parent Topic:**[Quorum Controlled Certificate Revocation](../concept/certificate-revocation.md)

