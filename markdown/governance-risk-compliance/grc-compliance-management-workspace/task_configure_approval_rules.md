---
title: Configure approval rules for control objective review
description: Configure dynamic approval rules to define who must approve a control objective before it can be published.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Control objective workflow, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configure approval rules for control objective review

Configure dynamic approval rules to define who must approve a control objective before it can be published.

## Before you begin

Role required: sn\_compliance.admin

The control objective workflow property must be enabled.

## About this task

The control objective workflow uses the dynamic approval rules framework to determine who must approve a control objective before it can be published. No approval rules are shipped out of the box.

When a control objective owner selects **Request Review**, the workflow evaluates all active approval rules that apply to the record. If matching rules exist, approvals are generated and the record moves to Review state. If no matching rules exist, the record moves directly to Approved without generating any approvals.

Any user or group can be configured as an approver through approval rules. When an approver rejects a record, the state returns to Draft. The owner must resolve the issue before re-submitting.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

2.  Select **New**.

3.  Configure the approvals for Control objective \(sn\_compliance\_policy\_statement\) table.

    For more information, see [GRC Approval Configurator.](../../grc-policy-and-compliance/concept/grc-approval-configurator-for-policy-extension-and-exception.md)


## Result

When a control objective owner selects **Request Review** on a record that matches the rule conditions, an approval is generated for each configured approver and the record moves to Review state. The record moves to Approved only after all approvers have approved.

