---
title: Approval email notification templates
description: Email notifications are triggered for new, due soon, and overdue approval to-dos in configurable templates. As an approver, you can review the details and approve the purchase requests directly from the email notifications.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Approve a request from Employee Center, Sourcing and Procurement Operations integration with Employee Center, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Approval email notification templates

Email notifications are triggered for new, due soon, and overdue approval to-dos in configurable templates. As an approver, you can review the details and approve the purchase requests directly from the email notifications.

When a purchase request that triggers an approval rule, is submitted, and you’re assigned as an approver for that purchase, a record is created in the sysapproval\_approver table, and an email notification is sent to you. You can review the details of the purchase request therein, view the attachments if needed, and provide your approval directly from the email notification. This makes the approval task experience seamless for you, and at the same time expedites the purchase experience of the requester or shopper who immediately receives the approval notification.

**Note:** When providing your approval from the email notification, ensure that the subject line of the response email has "approve" in it. Also ensure that there’s no mismatch in the approver's email address.

You may also reject the request, which redirects you to Employee Center to complete the action. Here, you can also request clarification on the purchase request from the requester, if need be. For more information on this, see [Approve a request from Employee Center](../task/approve-request-from-employee-center.md).

These email notifications are triggered for new, due soon, and overdue approval to-dos in templates that customers can easily configure to meet their specific business requirements.

-   Customers can modify the email content in flow designer or email scripts, according to their requirements.
-   They can also choose to fetch and use other details that aren’t displayed in the email by default, such as order type for purchase requisitions, product type or request type for sourcing requests, and so on. For detailed information on email templates and how to work with them, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   Customers can also configure the email layout, and change the background color or font color, for example. The html field in the email layout record must be modified to achieve this. For detailed information on email layouts and how to work with them, see [Email layouts](https://www.servicenow.com/docs/access?context=email-layouts&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Approve a request from Employee Center](../task/approve-request-from-employee-center.md)

