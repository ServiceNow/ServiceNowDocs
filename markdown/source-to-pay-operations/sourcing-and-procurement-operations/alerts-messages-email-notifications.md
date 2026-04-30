---
title: Alerts and email notifications from ShoppingHub
description: Several alerts and email notifications are triggered from ShoppingHub. This may be a result of your action, an assignment for you, or to keep you updated on the status of your purchases, including blanket contracts.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Alerts and email notifications from ShoppingHub

Several alerts and email notifications are triggered from ShoppingHub. This may be a result of your action, an assignment for you, or to keep you updated on the status of your purchases, including blanket contracts.

## Alerts

You receive an alert triggered from ShoppingHub when:

-   You switch the user that you’re shopping as in ShoppingHub
-   You switch to shop as someone else's delegate
-   You submit a revision
-   You complete a to-do that isn't an approval
-   You approve a purchase
-   You reject an approval
-   ShoppingHub has a global fail or fails to complete an action, due to server issue

## Email notifications

ShoppingHub sends out emails in a predefined template and uses flow designer to trigger the different email conditions. You can use the deep links that are provided in the emails to view relevant details. You’re notified through email when:

-   You submit a purchase request, irrespective of approval requirement \(for one or multiple purchase lines\)
-   You submit a new purchase request from a third-party site​.
-   Your delegate submits a purchase request, irrespective of approval requirement \(for one or multiple purchase lines\)
-   You submit a purchase request, irrespective of approval requirement that is automatically merged with an existing purchase request \(for one or multiple purchase lines\)
-   A purchase request that triggers an approval rule, is submitted, and you’re assigned as an approver for that purchase.

    **Note:** As an approver, you can approve the purchase from the email itself. For details, see [Approval email notification templates](approval-email-notifications-template.md).

-   An approver requests clarifications on your purchase request
-   An approver requests clarifications on your sourcing request
-   You respond to clarification requests on your purchase request
-   You respond to clarification requests on your sourcing request
-   A purchase is manually merged with an existing purchase, irrespective of approval requirement
-   A merged purchase is approved, partially approved, or rejected
-   You submit a sourcing request
-   Your delegate submits a sourcing request
-   Your purchase is approved, partially approved, or rejected and canceled
-   Your sourcing request is approved, partially approved, or rejected
-   You initiate or submit a purchase revision, irrespective of approval requirement
-   Your purchase revision is confirmed, approved, rejected, or canceled
-   There are any price or quantity changes during purchase order confirmation
-   There are any rejections for any purchase order lines that could not be fulfilled during purchase order confirmation
-   Your purchase is ordered from a supplier
-   Purchasing permissions are added for you on a blanket purchase order \(for one or multiple purchase lines\)
-   A blanket purchase order, for which you have purchasing permissions, is created or open \(for one or multiple purchase lines\)
-   Seven days are left for a blanket purchase order contract to expire \(for one or multiple purchase lines\)
-   20% budget is left on a blanket purchase order \(for one or multiple purchase lines\)
-   No budget is left on a blanket purchase order \(for one or multiple purchase lines\)
-   A blanket purchase order is closed \(for one or multiple purchase lines\)
-   You’re assigned as a delegate
-   You’re no longer assigned as a delegate
-   An item is removed from your cart or Purchase later section
-   You receive a delivery
-   A purchasing task is assigned to you
-   A breached approval review task is assigned to you
-   You’re mentioned in an activity stream
-   A new to-do is created and assigned to you
-   A to-do assigned to you is due today or overdue
-   A confirm receipt to-do is assigned to you
-   A confirm milestone to-do is assigned to you
-   A to-do requesting you to provide more information is assigned to you
-   A select supplier to-do is assigned to you
-   An invoice approval to-do is assigned to you
-   A purchase approval to-do is assigned to you
-   A purchase approval to-do is updated or canceled
-   An approval to-do is assigned to you as a result of a revision or merge reassessment
-   A procurement case state automatically changes to **Awaiting Acceptance**

    **Note:** The requestor gets an email notification with options to accept or reject the case resolution within a set time. The admin can set this time limit by navigating to **All &gt; Finance Common &gt; S2P Custom Configuration &gt; Case resolution acceptance config** and updating the `auto_close_in_days` value to an integer greater than 1 in the **Script** column. To turn off the email notifications, the admin can set the `email_acceptance` value to **False**. The requestor can also respond directly in the Employee Center by clicking **View case details**. For more information on procurement case states and approve request from Employee Center, see [Procurement case states](purchasing-tasks.md#awaiting_acceptance_case_state) and [Approve a request from Employee Center](../task/approve-request-from-employee-center.md).


You can adjust the email trigger conditions and content in flow designer or email scripts, if necessary. You can also choose to fetch and use other details that aren’t displayed in the email by default, such as order type for purchase requisitions, product type or request type for sourcing requests, and so on. For detailed information on email templates and how to work with them, see [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=australia&pubname=australia-platform-administration&ft:locale=en-US). You can also configure the email layout, and change the background color or font color, for example. The html field in the email layout record must be modified to achieve this. For detailed information on email layouts and how to work with them, see [Email layouts](https://www.servicenow.com/docs/access?context=email-layouts&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[Using Shopping Hub](use-shoppinghub-portal.md)

