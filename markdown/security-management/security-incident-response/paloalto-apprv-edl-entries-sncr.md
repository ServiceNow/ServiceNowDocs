---
title: Approve EDL entries for Palo Alto Networks Next-Generation Firewall
description: An approval process for External Dynamic List \(EDL\) entries is part of the preconfigured workflow. You approve EDL entries before the entries are activated on EDLs. One you approve the EDL entry, the firewall retrieves the entry, and your observable is blocked from that point forward.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Approve EDL entries for Palo Alto Networks Next-Generation Firewall

An approval process for External Dynamic List \(EDL\) entries is part of the preconfigured workflow. You approve EDL entries before the entries are activated on EDLs. One you approve the EDL entry, the firewall retrieves the entry, and your observable is blocked from that point forward.

## Before you begin

Role required: Approval for EDL entries is assigned to sn\_si.admin by default, but this authority can be assigned as required by your organization. In the following example, the ServiceNow AI Platform admin has approval authority.

## About this task

When the approval process is enabled, an EDL entry is not activated or deactivated on the EDL until it is approved.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Entries** and open the EDL record.

2.  On the EDL record, scroll to the Approval Requests section.

    **Note:** If you have Tabbed forms selected in System Settings, the section appears as a tab on the record.

    ![Approval requests on the firewall EDL entry record.](../image/4-30-url-entry-apprv.png)

3.  In Approval requests, click an item in the **State** column to open it.

    The approval record is displayed.

    ![Approval record.](../image/4-30-entry-form-apprv.png)

4.  Choose one option for approving the EDL entry.

<table id="choicetable_xbq_cvh_vdb"><thead><tr><th align="left" id="d147836e122">

Option

</th><th align="left" id="d147836e125">

Description

</th></tr></thead><tbody><tr><td id="d147836e131">

**Approve**

</td><td>

On the entry record, the **Status** field changes to `Added`, and the **Active** check box is selected.The **Deactivate**button is displayed and active.

 Work notes show that the request for the EDL entry has been approved.

</td></tr><tr><td id="d147836e158">

**Reject**

</td><td>

On the entry record, the Status field changes to **Rejected**, and the **Active** check box is cleared indicating the entry is not blocked on the firewall.Work notes show that the request for the EDL entry has been rejected.

</td></tr></tbody>
</table>    After you have approved the EDL entry and it is activated, the Palo Alto Networks Next-Generation Firewall retrieves the EDL entry after the next retrieval interval. After the entry is retrieved, the observable is blocked from that point forward. In the following figure, note that the Active check box is selected, the status is Added, and the work notes indicate that the request has been approved.

    ![Status, Active check box, and work notes highlighted.](../image/4-30-entry-apprvd-callout.png)

    After the EDL entry is approved and activated, the security incident record is marked with a security tag. The tag is displayed at the top of the record.

    ![Security tag on a Security Incident record.](../image/4-30-si-tagged.png)

    The security tag is also displayed on the observable record.

    ![Security tag on an observable record.](../image/4-30-url-tag-obsv.png)


**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall](paloalto-submit-entry-fm-blklist.md)

**Next topic:**[EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](../reference/paloalto-edl-execptions.md)

