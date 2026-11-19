---
title: Approve block list entries for the Check Point NGTP integration
description: An approval process for Block List entries is part of the preconfigured workflow. You approve Block List entries before the entries are activated on Block Lists. After you approve the Block List entry, the Gateway retrieves the entry, and your observable is blocked from that point forward.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/approve-blk-list-entries.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Approve block list entries for the Check Point NGTP integration

An approval process for Block List entries is part of the preconfigured workflow. You approve Block List entries before the entries are activated on Block Lists. After you approve the Block List entry, the Gateway retrieves the entry, and your observable is blocked from that point forward.

## Before you begin

-   Approval for Block List entries is assigned to Security Incident Administrator \(sn\_si.admin\) by default, but this authority can be assigned as required by your organization. In the following example, the ServiceNow AI Platform admin has approval authority.

Role required: sn.si.admin

## About this task

When the approval process is enabled, a Block List entry is not activated or deactivated on the Block List until it is approved.

## Procedure

1.  Navigate to **All** &gt; **Check Point NGTP Integration** &gt; **Block Request List Entries**, and open the Block List Entry record.

2.  On the Block List Entry record, scroll to the **Approval Requests** section.

    \[Omitted image "approval-requests.png"\] Alt text: Approval requests

3.  In Approval requests, click an item in the **State** column to open it.

    The approval record is displayed.

    \[Omitted image "request-being-approved.png"\] Alt text: Request approval

4.  Choose one option for approving the Block List entry.

<table id="table_kpf_lrk_ls"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approve

</td><td>

On the entry record, the Status field changes to Added, and the Active check box is selected.The Deactivate button is displayed and active.

 Work notes show that the request for the Block List entry has been approved.

</td></tr><tr><td>

Reject

</td><td>

On the entry record, the Status field changes to Rejected, and the Active check box is cleared indicating the entry is not blocked on the Gateway.Work notes show that the request for the Block List entry has been rejected.

</td></tr></tbody>
</table>    After you have approved the Block List entry and it is activated, the Check Point next-generation firewall retrieves the Block List entry after the next retrieval interval. After the entry is retrieved, the observable is blocked from that point forward. In the following figure, note that the Active check box is selected, the status is Added, and the work notes indicate that the request has been approved.

    \[Omitted image "deactivate-entry-redbox.png"\] Alt text: Deactivate entry

    After the Block List entry is approved and activated, the security incident record is marked with a security tag. The tag is displayed at the top of the record.

    \[Omitted image "security-tag.png"\] Alt text: URL tag displayed

    The security tag is also displayed on the observable record.

    \[Omitted image "security-tag-in-observ.png"\] Alt text: URL tag displayed in an observable


