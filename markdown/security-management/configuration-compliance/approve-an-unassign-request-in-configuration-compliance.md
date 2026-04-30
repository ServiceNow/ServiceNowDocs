---
title: Approve an unassign request in Configuration Compliance
description: Approve requests for the removal of remediation tasks from an assignment group or an individual user in the Configuration Compliance application.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Approve an unassign request in Configuration Compliance

Approve requests for the removal of remediation tasks from an assignment group or an individual user in the Configuration Compliance application.

## Before you begin

Role required: sn\_vulc.unassign\_approver

## About this task

By default, an approval configuration is provided. For unassign approvals, one approver is required in the Approver – Level 1 approval group. By default, the unassign approval group \(`Unassign Approver CC - Level 1`\) is created and users that are part of this group can approve the request. By default, this group contains the unassign approver role, sn\_vulc.unassign\_approver. You can modify or create a group and update the approval configuration by navigating to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Approval Rules** &gt; **Remediation Task Field Change Request** &gt; **Unassign Remediation Task**.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **My Approvals**.

2.  Select a request from your queue.

3.  Approve or reject the request by adding the appropriate comments.


