---
title: Components installed with Advanced Approval Management AI
description: MCP tools are installed with activation of the Advanced Approval Management AI plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/components-installed-with-advanced-approval-mgmt-AI.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [MCP tools, Advanced Approval Management AI, ServiceNow Otto for Advanced Approval Management, approval roles]
breadcrumb: [Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Components installed with Advanced Approval Management AI

MCP tools are installed with activation of the Advanced Approval Management AI plugin.

## Tools installed

<table id="table_apc_g2v_1kc"><thead><tr><th>

Tool name \[ID\]

</th><th>

Description

</th><th>

Role required

</th></tr></thead><tbody><tr><td>

Approver Actions \(sn\_adv\_apr\_mgt\_ai.approver\_actions\)

</td><td>

For approvers:-   Approve or reject one or more pending approval steps.
-   Add an ad-hoc approver \(user or group\) to an in-progress approval request.

</td><td>

sn\_adv\_appr\_mgmt.approval\_request\_approver

</td></tr><tr><td>

Get Approval Details \(sn\_adv\_apr\_mgt\_ai.get\_approval\_details\)

</td><td>

Provides:-   Preview of approval rules and routing for a quote that hasn't been submitted for approval.
-   Full history of approval cycles for a quote version, including steps that are pending, haven't started, or are finished.
-   List of eligible ad-hoc approver candidates.
-   Current approval status and history for several quotes at once.

</td><td>

sn\_adv\_appr\_mgmt.approval\_request\_viewer

</td></tr><tr><td>

Get Pending Approvals List \(sn\_adv\_apr\_mgt\_ai.get\_pending\_approvals\_list\)

</td><td>

For approvers, retrieves all approval requests currently waiting for approval action, grouped by approval chain.

</td><td>

sn\_adv\_appr\_mgmt.approval\_request\_viewer

</td></tr><tr><td>

Get Quote Details \(sn\_qut\_sum\_skill.get\_quote\_details\)

</td><td>

Retrieves quote header and line item details for active quotes.

</td><td>

sn\_quote\_mgmt\_core.quote\_viewer

</td></tr><tr><td>

Requestor Actions \(sn\_adv\_apr\_mgt\_ai.requestor\_actions\)

</td><td>

For requesters:-   Recall an approval request for a quote
-   Submit a quote for approval, which creates a new approval request.
-   Add an ad-hoc approver \(user or group\) to an in-progress approval request.

</td><td>

sn\_adv\_appr\_mgmt.approval\_request\_writer

</td></tr></tbody>
</table>**Parent Topic:**[Configure, price, quote reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/reference-cpq.md)

