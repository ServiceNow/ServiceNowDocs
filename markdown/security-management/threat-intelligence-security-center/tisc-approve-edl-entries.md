---
title: Approve EDL entries for Palo Alto Networks
description: Approving External Dynamic List \(EDL\) entries is part of the pre configuration. You must approve the EDL entries before the entries are activated on EDLs for the firewall to retrieve the entry and apply the security policy.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks integration, Firewall integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Approve EDL entries for Palo Alto Networks

Approving External Dynamic List \(EDL\) entries is part of the pre configuration. You must approve the EDL entries before the entries are activated on EDLs for the firewall to retrieve the entry and apply the security policy.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

When the approval process is enabled, an EDL entry is not activated or deactivated on the EDL until it is approved.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Analyst Workbench**.

2.  Drill down to **PAN NGFW** section and select the EDL record for approval.

3.  Go to **My Approvals**.

4.  Select the EDL record\(s\) for approval.

5.  Click **Approve**.

6.  Under **My Approval** requests, click an item in the **State** column to open it.

7.  Choose the option for approving the EDL entry.

<table id="choicetable_xbq_cvh_vdb"><thead><tr><th align="left" id="d246330e125">

Option

</th><th align="left" id="d246330e128">

Description

</th></tr></thead><tbody><tr><td id="d246330e134">

**Approve**

</td><td>

On the entry record, the **Status** field changes to `Added`, and the **Active** check box is selected. The **Deactivate** button is displayed and active.Work notes show that the request for the EDL entry has been approved.

</td></tr><tr><td id="d246330e158">

**Reject**

</td><td>

On the entry record, the Status field changes to **Rejected**, and the **Active** check box is cleared indicating the entry is not blocked on the firewall.Work notes show that the request for the EDL entry has been rejected.

</td></tr></tbody>
</table>    After you have approved the EDL entry and it is activated, the Palo Alto Networks retrieves the EDL entry after the next retrieval interval. After the entry is retrieved, the observable is blocked from that point forward. In the following figure, note that the **Active** check box is selected, the status is Added, and the work notes indicate that the request has been approved.

    ![Approved EDL entry.](../image/tisc-edl-approved-entry.png)


**Parent Topic:**[Palo Alto Networks integration](../concept/palo-alto-networks-integration.md)

