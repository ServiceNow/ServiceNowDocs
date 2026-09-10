---
title: Request an approval
description: Request approval for a state change or a due date extension on an issue or remediation task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/request-an-approval.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue approval flows, Common GRC features, Governance, Risk, and Compliance]
---

# Request an approval

Request approval for a state change or a due date extension on an issue or remediation task.

## Before you begin

An approval configuration record must exist for the approval type that you want to request. See [Set up an approval configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-up-approval-configurator.md).

Role required: sn\_grc\_appr.approver

## Procedure

1.  Open the issue or remediation task.

2.  Select the approval type that you want to request.

<table><thead><tr><th align="left" id="d81626e66">

Approval type

</th><th align="left" id="d81626e69">

Action

</th></tr></thead><tbody><tr><td id="d81626e75">

**__State Change__**

</td><td>

Attempt to move the record past the state that requires approval. The approval request is created automatically.

</td></tr><tr><td id="d81626e86">

**__Due Date Extension__**

</td><td>

Select **Request due date extension**, and fill in the extension request fields.

</td></tr></tbody>
</table>3.  If requesting a due date extension, fill in the request fields.

    |Field|Description|
    |-----|-----------|
    |**Requested due date**|The new due date being requested.|
    |**Reason**|The reason for the extension request.|
    |**Requested by**|The user submitting the request. Defaults to the current user.|
    |**Requested on**|When the request was submitted. Read-only.|
    |**Approver**|The user or group who will review the request.|

4.  Select **Submit**.


## Result

An approval request is created and sent to the approver. The record cannot move past the associated state, or have its due date extended, until the approval is granted.

## What to do next

See [Review and respond to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-respond-to-an-approval-request.md).

**Parent Topic:**[Issue approval flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-approval-flows.md)

