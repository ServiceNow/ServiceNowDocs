---
title: Tracking employee contacts using daily logs
description: After employees start returning to the workplace, use daily contact logs to help promote the health and safety of all your employees. Let employees submit a list of other people with whom they come in contact during the day. Send mobile and email push notifications to employees to submit their contact log for the day.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Tracking employee contacts using daily logs

After employees start returning to the workplace, use daily contact logs to help promote the health and safety of all your employees. Let employees submit a list of other people with whom they come in contact during the day. Send mobile and email push notifications to employees to submit their contact log for the day.

Keep a track of the employees who have responded from the daily contact log responses. You can resend notifications to employees who have not responded to alert them for submitting their daily contact log.

The employee daily contact log in the Contact Tracing application works with the Emergency Outreach application. For more information, see [Emergency Outreach](../../business-continuity/concept/emergency-outreach.md).

A user with the sn\_imt\_checkin.checkin\_admin role for Emergency Outreach can review and modify the outreach notification for the daily contact log. For more information, see [Configure an Emergency Outreach notification for the daily contact log](../task/configure-outreach-notif-daily-log.md).

An administrator can modify the schedule associated with the outreach notification to configure the timing to send notifications to employees. For more information, see [Configure a scheduled job](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** If you are using Service Portal using a URL suffix other than the default `/sp`, update the same in the Daily Log form for it to work properly. You must associate the form with the service catalog. For more information on Service Portal, see [Create a portal](https://www.servicenow.com/docs/access?context=create-a-portal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) and for Service Portal page navigation, see [Page navigation by URL](https://www.servicenow.com/docs/access?context=navigate-by-portal-url&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

-   **[Send an Outreach notification for the daily contact log](../task/send-outreach-notif-daily-log.md)**  
Send an Emergency Outreach notification, on demand, to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.
-   **[Submit a list of contacts that you interacted with at the workplace](../task/submit-contacts-log.md#)**  
Submit a list of people that you've come into contact with at the workplace to help your organization identify on-site employees who may have been in contact with a potentially exposed coworker.
-   **[Review daily log responses](../task/review-daily-contacts-log.md)**  
Review daily contact log responses from employees who received a push notification requesting a list of contacts that they interacted with at the workplace.

**Parent Topic:**[Contact Tracing](contact-tracing.md)

