---
title: Deliver announcements to employees through Moveworks
description: Author and publish announcements and deliver them to employees through Moveworks with a Moveworks promotion. When processed, delivery goes to the Moveworks in-box or Slack for registered users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/employee-experience-foundation/empworks-promotions-moveworks.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 1
breadcrumb: [Working with Moveworks capabilities, Moveworks, EmployeeWorks, Employee Service Management]
---

# Deliver announcements to employees through Moveworks

Author and publish announcements and deliver them to employees through Moveworks with a Moveworks promotion. When processed, delivery goes to the Moveworks in-box or Slack for registered users.

## Before you begin

Before you start, verify the following:

-   Your organization has super admins assigned in Moveworks who can update configurations, such as the client ID and client secret.
-   A super admin has generated the client ID and client secret for the Moveworks endpoint with ecomms scope.

Role required: Content Manager

## About this task

Content managers author, publish, and deliver announcements from one place, with Moveworks as the delivery channel. You get a single authoring experience, and employees get timely notifications where they already work.

## Procedure

1.  On the **Content Library** page, select **Create** announcement.

2.  In the **Promote** section of the **Editor** page, select **Add a Moveworks promotion**.

    **Note:** Turning promotions off keeps the connection details. However, promotions already sent to Moveworks aren’t cancelled and removing the connection doesn’t cancel them.

3.  Enter the announcement details, the publishing start and end dates, and the intended audience.

    **Note:** If the promotion schedule is more than 24 hours away, Moveworks is notified 24 hours before go-live \(a processing message will appear\). If the promotion is between 1 and 24 hours away, the promotion is picked up by an hourly job, so it can go out later. If the promotion is within an hour \(or already past\), Moveworks might not deliver on time \(a warning appears on the UI\).

4.  When you finish the Moveworks promotion details, select **Done**.

5.  Select **Publish**.

    **Note:** When the announcement is published it is handed off to Moveworks for delivery. Selected employees receive it in the Moveworks assistant with a link to the content. Delivery can take a short time, and publishing doesn’t wait for Moveworks to finish.


## Result

The announcement publishes, and a notification is sent. The notification appears in the Moveworks in-box, Microsoft teams, or Slack channel, if configured.

