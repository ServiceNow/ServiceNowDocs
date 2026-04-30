---
title: Approve a change request, or registration request
description: Users with the snc\_external role can view and approve registration requests and change requests from the Customer Service Portal.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the Customer Service Portal, Customer communication, Using Customer Service Management, Customer Service Management]
---

# Approve a change request, or registration request

Users with the snc\_external role can view and approve registration requests and change requests from the Customer Service Portal.

## Before you begin

Role required: snc\_external

## About this task

A registration request or a change request may require approval from another employee within the same organization. For details on registration request, see [Customer contact self-registration](../concept/c_PortalSelfRegistration.md).

## Procedure

1.  In the Customer Service Portal header, click **Notification** &gt; **View all notifications**.

2.  Click a record in the Approvals section of the Notifications page.

    The system displays a read-only view of the record approval form. For requests that include one or more items, these items appear in a collapsible list at the bottom of the Request form.

3.  Click a requested item at the bottom of the Request form to view the details in a pop-up window.

4.  Click **Approve**.

    The system makes the following updates:

    -   The record status is set to **Approved**.
    -   The record status is displayed after the record number in the Related Records widget on the Case form.
    -   The record status is added to the Case form.
        -   If the record is approved by the customer administrator or if the customer self-approves the request, the change in status is added to the **Additional comments** field.
        -   For other approvers, the change in status is added to the **Work notes** field.
    -   The approval record is updated in the Approval table.

