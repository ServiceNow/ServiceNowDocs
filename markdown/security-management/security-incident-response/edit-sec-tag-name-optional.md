---
title: Edit the security tag name for the Check Point NGTP integration
description: If the Display tag check box is selected when you create the Block List record, you can edit the tag names and colors of the security tags. Security tags help you track observables that are already blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/edit-sec-tag-name-optional.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit the security tag name for the Check Point NGTP integration

If the Display tag check box is selected when you create the Block List record, you can edit the tag names and colors of the security tags. Security tags help you track observables that are already blocked.

## Before you begin

Role required: sn.si.admin

## About this task

Security tags help you quickly identify which security incidents have observables on a block list. Tags also help you identify whether an observable is already blocked, or, if it has been removed from a Block List. By default, the color of the security tag is black for block list entries and gray for allow list entries. You can change the names and colors of the tags to help you recognize certain tags more easily.

## Procedure

1.  Navigate to **All** &gt; **Check Point NGTP Integration** &gt; **Block Request List Configuration**.

    \[Omitted image "activate-block-list.png"\] Alt text: Activate block list

2.  Click an item in the **Name** column to open it.

    The Block List record is displayed. By default, the security tag name is the same value you entered in the Name field of the Block List when you created it. By default, the name also includes a Block List prefix, for example, Block List – Malware Malicious URLs.

    \[Omitted image "block-ip.png"\] Alt text: Tag for Observables field

3.  Click the information icon next to tag for observables then Open record.

    \[Omitted image "open-record.png"\] Alt text: Information for observables

    The Security Tag Form is displayed.

    \[Omitted image "security-tag-form.png"\] Alt text: Security Tag form

4.  In the **Name** field, modify the security tag name.

5.  Click **Update**.

    The updated Block List record is displayed with the modified tag name.

    **Note:** In the following example, Outbound has been added to the tag name. Keep the Check Point prefix in your new tag name to help you identify the tag is associated with the Check Point next-generation firewall integration.

    \[Omitted image "block-ip.png"\] Alt text: Block IP

    The security tags are displayed for each observable type \(IP, URL, Domain\) on the Security Incident record and the Observable record each time that observable is added to Block List.


## Result

\[Omitted image "sec-tag-displayed-in-observ.png"\] Alt text: Observable added to a block list

If an observable has already been added to a Block List, and a security tag is displayed on a security incident for this observable, the Block List security tag also is displayed automatically on any subsequent security incident records that are created. This duplication tells you that the observable is already on a block list. You do not need to add this observable and re-block it.

When an observable is no longer blocked, a security tag is not displayed on the security incident record or the observable record. In this instance, no security tag indicates that the expiration date of the observable may have passed, or the observable has been deactivated from a Block List.

