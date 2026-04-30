---
title: Receive notifications
description: Individuals who are designated approvers automatically receive approval notifications, including approval status updates.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Receive notifications

Individuals who are designated approvers automatically receive approval notifications, including approval status updates.

Approval notifications will be sent at the following times:

-   When an individual is assigned as an approver either automatically or manually. If a group is chosen, then all members of the group will be sent an email. By default, the email an approver receives will contain a "mailto" link that will allow the approver to either approve or reject the request directly from their email system.
-   When the request reaches approved status, the person assigned to the request will receive an email indicating it has been approved.

The details contained in the emails and the points at which they are sent can be tailored using **System Definition** &gt; **Business Rules** and **System Policy**.

Note for Blackberry users: In order to see the "mailto" links mentioned above to approve or reject a request \(i.e. 'Click here to approve CHG55555' or 'Click here to reject CHG55555'\), your Blackberry device must be using version 4.5 of their software which supports HTML emails. If your Blackberry device is using an earlier version, you will not be able to view or use the "mailto" links. However, as a workaround, users can reply to the email and add the statements `state:approved` or `state:rejected` within the body of the email before sending it to force the automatic approval/rejection functionality.

If you create an appropriate Inbound Email Action, you can let approvers respond to approval email notifications with a simple "yes" or "no" answer.

-   **[Embed an approval request within the Outlook email client](../task/embed-approval-in-outlook.md)**  
Embed an interactive approval request for service catalog requests in the email notification sent to a user. The user can accept or reject the approval request from the email client.

**Parent Topic:**[Classic approvals](../reference/r_Approvals.md)

