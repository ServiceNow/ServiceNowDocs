---
title: Configure Microsoft Outlook integration
description: Set up Microsoft Outlook to integrate meeting invites from Hiring Experiences with your Outlook account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/configure-microsoft-outlook-integration-ta.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Configure Microsoft Outlook integration

Set up Microsoft Outlook to integrate meeting invites from Hiring Experiences with your Outlook account.

## Before you begin

Role required: admin

## Procedure

1.  Set up the Microsoft Exchange Online spoke.

    For more information, see .

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


**Parent Topic:**[Integrations for Hiring Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/integrate-with-talent-acquisition.md)

