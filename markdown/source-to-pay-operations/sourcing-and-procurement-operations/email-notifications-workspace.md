---
title: Email notifications from Playbook
description: Several email notifications are triggered from Playbook. This may be a result of your action, an assignment for you, or to keep you updated on the status of your purchases, including purchase revisions.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Email notifications from Playbook

Several email notifications are triggered from Playbook. This may be a result of your action, an assignment for you, or to keep you updated on the status of your purchases, including purchase revisions.

Playbook sends out emails in a predefined template and uses flow designer to trigger the different email conditions. You can use the deep links that are provided in the emails to view relevant details. You’re notified through email when:

-   Your request to edit a purchase order or purchase requisition has been confirmed.
-   Your request to edit a purchase order or purchase requisition has been rejected.
-   Your request to cancel a service request, purchase order, purchase requisition, purchase order line, or purchase requisition line has been confirmed.

    **Note:** You receive one email notification if you cancel from the header level. However, cancellation at line levels triggers respective email notifications.

-   Your request to cancel a service request, purchase order, purchase requisition, purchase order line, or purchase requisition line has been rejected.
-   Your request to return a product has been confirmed.
-   Your request to return a product has been rejected.

**Note:** You can adjust the email trigger conditions and content in flow designer or email scripts, if necessary. You can also choose to fetch and use other details that aren’t displayed in the email by default, such as order type for purchase requisitions, product type or request type for sourcing requests, and so on. For detailed information on email templates and how to work with them, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). You can also configure the email layout, and change the background color or font color, for example. The html field in the email layout record must be modified to achieve this. For detailed information on email layouts and how to work with them, see [Email layouts](https://www.servicenow.com/docs/access?context=email-layouts&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Procurement Case Management](../concept/psd-overview.md)

