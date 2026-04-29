---
title: Configure Microsoft Outlook integration
description: Set up Microsoft Outlook to integrate meeting invites from Hiring Experiences with your Outlook account.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Configure Microsoft Outlook integration

Set up Microsoft Outlook to integrate meeting invites from Hiring Experiences with your Outlook account.

## Before you begin

Role required: admin

## Procedure

1.  Set up the Microsoft Exchange Online spoke.

    For more information, see [Microsoft Exchange Online Spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

2.  In the navigation filter, enter `sys_properties.list`.

    The System Properties \[sys\_properties\] table is displayed.

3.  Locate the **sn\_ta\_recruiter.enable\_outlook\_integration** property and set the value to **true**.

4.  Locate the **sn\_ta\_recruiter.exchange\_meeting\_user** property and set the value to the user principal name.

    -   Any email invites originating from Hiring Experiences is sent from the user principal name account, if defined. If not defined, it defaults to the user account used when setting up the Microsoft Exchange Online spoke.
    -   To send emails on behalf of the user principal name account, the user created while setting up the Microsoft Exchange Online spoke should have delegated access.
5.  Enable placeholder outlook invites to be sent by locating the **sn\_ta\_recruiter.block\_interviewer\_calendar** property and setting the value to **true**.

6.  Navigate to **All** &gt; **Microsoft Exchange Online Spoke** &gt; **Webhook Registry**.

7.  Locate and open the Job interview scheduling record.

8.  Select **Callback URL**.

9.  Select **Update**.


**Parent Topic:**[Integrations for Hiring Experiences](../concept/integrate-with-talent-acquisition.md)

