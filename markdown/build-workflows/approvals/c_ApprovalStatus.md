---
title: Approval status
description: The approval status of a change request is determined by looking at the current status of all the approvers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/approvals/c\_ApprovalStatus.html
release: australia
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Build workflows]
---

# Approval status

The approval status of a change request is determined by looking at the current status of all the approvers.

If any approver has rejected the change, the approval status will be Rejected. If all approvers have approved the change, the approval status will be Approved. If all approvers are in the Not Requested status or if there are no approvers, the change status will be Not Requested, otherwise the status will be Requested.

For added flexibility when creating approvals, including the ability to set up an "one of" approval where only one person of a group of approvers needs to approve, consider using [Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/wf-approvals-n-rollbacks.md) .

**Related topics**  


[Classic approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/r_Approvals.md)

