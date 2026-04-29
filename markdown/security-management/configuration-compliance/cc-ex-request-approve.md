---
title: Approve an exception request in Configuration Compliance
description: Approve exception requests for remediation tasks that can't be remediated immediately. You must assess these requests for risk and then approve them for deferral until they can be remediated.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Requesting and approving an exception for a remediation task, Use, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Approve an exception request in Configuration Compliance

Approve exception requests for remediation tasks that can't be remediated immediately. You must assess these requests for risk and then approve them for deferral until they can be remediated.

**Important:** As an admin or analyst, you can approve or reject an exception request from the Vulnerability Manager Worksapce.

## Before you begin

Role required: sn\_vulc.exception\_approver

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **My Approvals**.

2.  Select a request from your queue.

3.  Approve or reject the request with appropriate comments.

    **Note:** In case of a two-level approval workflow, after the first-level approval, the request is submitted to the second level for further approval. If there are no users in the second level, the request is automatically approved after the first-level approval.

    After the request is approved, the remediation task moves to a Deferred state. In case of rejection, the remediation task reverts to its earlier state.


