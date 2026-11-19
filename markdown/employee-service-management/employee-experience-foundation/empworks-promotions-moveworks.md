---
title: Deliver announcements to employees through Moveworks
description: Author and publish announcements and deliver them to employees through Moveworks with a Moveworks promotion. When processed, delivery goes to the Moveworks in-box or Slack for registered users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/employee-experience-foundation/empworks-promotions-moveworks.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-11-16"
reading_time_minutes: 2
breadcrumb: [Working with Moveworks capabilities, Moveworks overview, EmployeeWorks, Employee Service Management]
---

# Deliver announcements to employees through Moveworks

Author and publish announcements and deliver them to employees through Moveworks with a Moveworks promotion. When processed, delivery goes to the Moveworks in-box or Slack for registered users.

## Before you begin

Before you start, verify the following:

-   ServiceNow EmloyeeWroks with Announcements on these versions or later:
    -   ServiceNow EmployeeWorks Web App: 16.4
    -   ServiceNow EmployeeWorks Web App Extended: 2.5.3
    -   Content Publishing: 37.6.3
-   Moveworks Super admin access to Moveworks setup, to create a credential.
-   ServiceNow admin access to the configuration console, to connect to Moveworks.

Role required: sn\_cd.content\_manager, sn\_cd.content\_admin

## About this task

Content managers author, publish, and deliver announcements from one place, with Moveworks as the delivery channel. You get a single authoring experience, and employees get timely notifications where they already work.

**Note:** For additional overview, configurations and troubleshooting, refer to the following Moveworks document: [Deliver EmployeeWorks Announcements Through Moveworks](https://docs.moveworks.com/ai-assistant/capabilities/employee-communications/employeeworks-announcements#overview)

## Procedure

1.  On the **Content Library** page, select **Create** announcement.

2.  In the **Promote** section of the **Editor** page, select **Add a Moveworks promotion**.

    **Note:** Turning promotions off keeps the connection details. However, promotions already sent to Moveworks aren’t cancelled and removing the connection doesn’t cancel them.

3.  Enter the announcement details, the publishing start and end dates, and the intended audience.

    **Note:** If the promotion schedule is more than 24 hours away, Moveworks is notified 24 hours before go-live \(a processing message will appear\). If the promotion is between 1 and 24 hours away, the promotion is picked up by an hourly job, so it can go out later. If the promotion is within an hour \(or already past\), Moveworks might not deliver on time \(a warning appears on the UI\).

4.  When you finish the Moveworks promotion details, select **Done**.

5.  Select **Publish**.

    **Note:** When the announcement is published it is handed off to Moveworks for delivery. Links will appear in the notification as a button option, if the author of the announcement includes a link. Publishing makes the announcement live in the portal. The Moveworks notification is handled separately and is scheduled based on the start date, which might cause it to be sent later than the initial publishing time. Recipients must be registered Moveworks users to receive it. If a notification can't be delivered, the announcement will still be published.


## Result

The announcement publishes, and a notification is sent. The notification appears in the Moveworks in-box, Microsoft teams, or Slack channel, if configured.

**Note:** For additional overview, configurations and troubleshooting, refer to the following Moveworks document: [Deliver EmployeeWorks Announcements Through Moveworks](https://docs.moveworks.com/ai-assistant/capabilities/employee-communications/employeeworks-announcements#overview)

