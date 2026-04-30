---
title: \(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall
description: If the Display tag check box is selected when you create the External Dynamic List \(EDL\) record, you can edit the tag names and colors of the security tags. Security tags help you track observables that are already blocked.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall

If the **Display tag** check box is selected when you create the External Dynamic List \(EDL\) record, you can edit the tag names and colors of the security tags. Security tags help you track observables that are already blocked.

## Before you begin

Role required: sn\_si.admin

## About this task

Security tags help you quickly identify which security incidents have observables on a block list. Tags also help you identify whether an observable is already blocked, or, if it has been removed from an EDL. By default, the color of the security tag is black for block list entries and gray for allow list entries. You can change the names and colors of the tags to help you recognize certain tags more easily.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

    ![Select Firewall EDL Configuration.](../image/4-30-fedl-nav.png)

2.  Click an item in the **Name** column to open it

    The EDL record is displayed. By default, the security tag name is the same value you entered in the **Name** field of the EDL when you created it. By default, the name also includes an EDL prefix, for example, EDL – Malware Malicious URLs.

    ![Security tag name in the EDL tag for observables field.](../image/4-30-edl-tag-edit-b4-box.png)

3.  Click the information icon \(![Information icon](../../vulnerability-response/image/i-icon.png)\) next to **EDL tag for observables** then **Open record**.

    ![Open the EDL tag for observables record.](../image/4-30-edl-tag-edit-icon.png)

    The Security Tag Form is displayed.

    ![Security tag form.](../image/4-30-edit-tag-rcd.png)

4.  In the **Name** field, modify the security tag name and click **Update**.

    The updated EDL record is displayed with the modified tag name. In the following example, `Outbound` has been added to the tag name. Keep the `EDL` prefix in your new tag name to help you identify the tag is associated with the Palo Alto Networks Next-Generation Firewall integration.

    ![New security tag name in EDL tag for observables field.](../image/4-30-edl-tag-edit-after.png)

    The security tags are displayed for each observable type \(IP, URL, Domain\) on the Security Incident record and the Observable record each time that observable is added to an EDL.

    ![Security Incident record with security tag.](../image/4-30-si-tagged.png)

    If an observable has already been added to an EDL, and a security tag is displayed on a security incident for this observable, the EDL security tag also is displayed automatically on any subsequent security incident records that are created. This duplication tells you that the observable is already on a block list. You do not need to add this observable and re-block it.

    When an observable is no longer blocked, a security tag is not displayed on the security incident record or the observable record. In this instance, no security tag indicates that the expiration date of the observable may have passed, or the observable has been deactivated from an EDL.


**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](../reference/paloalto-edl-execptions.md)

**Next topic:**[Uninstall](paloalto-unistall.md)

