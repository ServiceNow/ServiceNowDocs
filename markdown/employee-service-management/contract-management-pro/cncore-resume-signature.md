---
title: Resume signature process
description: Resume the paused signature process with the modified signatories.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-06-16"
reading_time_minutes: 1
breadcrumb: [Modify signatories, Signature workflow for a contract request, Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Resume signature process

Resume the paused signature process with the modified signatories.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

Use the **Resume signature** option to resume the signature process. If the signature process is not resumed within the configured time duration \(as defined by the system property **maximum\_signature\_pause\_duration**\), any changes made to the signatories are automatically reverted, and the signature process resumes from its previous state.

**Resume signature** option is only available for wet signature workflow and electronic signature workflow with Docusign electronic signature provider integration.

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request that is in Signature paused status.

3.  Select **Resume signature**.

4.  Select **Resume** on the confirmation screen.


## Result

-   The Contract Status is updated to Awaiting signature.
-   If the current signatory is different from before the pause, a notification is sent for signature request.
-   The activity stream records the resume signature action.

**Parent Topic:**[Modify signatories](cncore-pause-signature.md)

