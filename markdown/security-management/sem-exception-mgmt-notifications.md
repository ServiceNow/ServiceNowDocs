---
title: Exception management notifications
description: Email notifications fired by the exception management workflow. Each row lists the notification, the event that triggers it, who receives it, and the action expected from the recipient. Use this reference to anticipate what mail you will receive at each lifecycle stage and to verify that the correct people are on the routing list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-exception-mgmt-notifications.html
release: brazil
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 5
keywords: [notifications, email, exception management]
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Exception management notifications

Email notifications fired by the exception management workflow. Each row lists the notification, the event that triggers it, who receives it, and the action expected from the recipient. Use this reference to anticipate what mail you will receive at each lifecycle stage and to verify that the correct people are on the routing list.

## Notification catalog

The table lists the user-facing notifications fired by exception management. System-only notifications used for integration callbacks are not included.

|Notification|Trigger|Recipients|Action expected|
|------------|-------|----------|---------------|
|Exception request submitted|A requester submits a new exception \(deferral\) request.|Members of the matching approver group at Level 1.|Review the request in the Unified Approvals View and approve or reject.|
|Exception request approved|An approver approves an exception request, and all required levels have cleared.|Original requester.|Acknowledge; the finding is now in **Deferred** state until the configured expiry date.|
|Exception request rejected|An approver rejects an exception request.|Original requester.|Review the approver's justification. Either remediate the finding or submit a new request with adjusted justification.|
|Exception expiring soon|An approved exception is within one week of its expiry date.|Original requester and the assignment group.|Decide whether to extend \(use **Request Extension**\) or to complete remediation before the finding reopens.|
|Exception expired — finding reopened|An approved exception reaches its expiry date without an extension or remediation.|Original requester and the assignment group.|Resume remediation work; the finding is back in **Open** state.|
|Exception rule submitted|A requester submits a new exception rule for approval.|Members of the exception rule approver group \(`sn_sec_exception.approver`\).|Review the rule criteria and evidence; approve or reject. The email includes a count and link to the findings impacted by the rule.|
|Exception rule approved|An approver approves an exception rule request.|Original requester.|Acknowledge; the rule is now active and automatically applies exceptions to matching findings.|
|Exception rule rejected|An approver rejects an exception rule request.|Original requester.|Review the rejection reason. Adjust the rule criteria or evidence and resubmit if required.|
|Exception rule expiring soon|An active exception rule is approaching its validity end date.|Exception administrators \(`sn_sec_exception.admin`\).|Renew the rule before it expires, or allow it to lapse and let matching findings reopen.|
|Exception rule expired|An exception rule reaches its validity end date without renewal.|Exception administrators \(`sn_sec_exception.admin`\).|The rule no longer applies; previously matched findings return to their prior state.|
|Exception rule extension submitted|A requester submits a request to extend an existing exception rule's validity.|Members of the exception rule approver group \(`sn_sec_exception.approver`\).|Review the extension justification; approve or reject.|
|Exception rule extension approved or rejected|An approver acts on an exception rule extension request.|Original requester.|On approval, the rule's new validity end date applies. On rejection, the original end date stands.|
|Exception rule extension expiring|An exception rule's extension period is approaching its end.|Exception administrators \(`sn_sec_exception.admin`\).|Renew the exception rule with updated evidence, or let it expire and re-evaluate the matching findings.|
|Exception rule extension expired|An exception rule's extension period ends without a further extension or renewal.|Exception administrators \(`sn_sec_exception.admin`\).|The rule reverts to its prior validity end date, or expires if none remains.|
|Extension request submitted|A requester submits an extension on an existing deferred finding.|Members of the matching approver group.|Review the extension justification and approve or reject.|
|Extension request approved or rejected|An approver acts on an extension request.|Original requester.|On approval, the new **Until** date applies. On rejection, the original deferral date stands.|
|Extension expiring soon|An approved extension is within one week of its expiry date.|Original requester and the assignment group.|Decide whether to request a further extension or complete remediation before the finding reopens.|
|Extension expired — finding reopened|An approved extension reaches its expiry date without a further extension or remediation.|Original requester and the assignment group.|Resume remediation work; the finding is back in **Open** state.|
|False positive request submitted|A requester marks a finding as false positive.|Members of the False Positive Approver group.|Review the evidence and approve or reject.|
|False positive approved|A false positive request clears all approval levels.|Original requester.|Acknowledge; the finding is now **Closed** with reason **False positive**.|
|False positive rejected|An approver rejects a false positive request.|Original requester.|Review the rejection reason. Either remediate the finding, attach additional evidence, or escalate.|
|False positive expiring soon|An approved false positive determination is within one week of its expiry date.|Original requester and the assignment group.|Decide whether to request an extension or complete remediation before the finding reopens.|
|False positive expired — finding reopened|An approved false positive determination reaches its expiry date without an extension or remediation.|Original requester and the assignment group.|Resume remediation work; the finding is back in **Open** state.|
|Risk reduction request submitted|A requester submits a risk reduction request.|Members of the matching approver group at Level 1.|Review the request in the Unified Approvals View and approve or reject.|
|Risk reduction expiring soon|An approved risk reduction is within one week of its expiry date.|Original requester and the assignment group.|Decide whether to extend or complete remediation before the finding reopens.|
|Risk reduction expired — finding reopened|An approved risk reduction reaches its expiry date without an extension or remediation.|Original requester and the assignment group.|Resume remediation work; the finding is back in **Open** state.|
|Unassign request submitted|A requester submits an unassignment.|Members of the Unassign Approver group; current owner is copied.|Approver: review and approve or reject. Current owner: acknowledge that the assignment is under review.|
|Unassign approved|An unassign request is approved.|Original requester, original owner, new owner.|New owner: begin remediation. Original owner: confirm transfer of any in-progress notes.|
|Unassign rejected|An approver rejects an unassign request.|Original requester.|Review the approver's justification. The finding remains with the original owner.|
|Approval level escalation|A multi-level approval rule advances to the next level after the previous level approves.|Members of the next level's approver group.|Review the request and the prior level's decision; approve or reject.|
|Bulk action summary|An approver completes a bulk approve or bulk reject action in the Unified Approvals View.|The approver who initiated the bulk action.|Review the per-request outcome; act on any requests that the bulk action skipped.|

## Configuration notes

Notification routing is governed by the approval rule's approver groups and by the Notification Preferences of the recipient. Administrators can enable, disable, or adjust the recipients of each notification in **System Notification** &gt; **Email** &gt; **Notifications**, filtered by table `sn_sec_exception_change_approval`.

The table above lists user-facing notifications. The system also fires a small number of integration-only notifications for downstream automation; those are documented in the developer reference and are not visible to end users.

