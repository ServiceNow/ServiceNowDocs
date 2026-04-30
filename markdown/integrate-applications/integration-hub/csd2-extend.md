---
title: Extend a software lease
description: Users of software deployed by CSD 2.0 can request the extension of a lease window, if the software is revocable by a software distribution system.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Extend a software lease

Users of software deployed by CSD 2.0 can request the extension of a lease window, if the software is revocable by a software distribution system.

## Before you begin

Role required:

**Note:** Ensure that the user has one of the two mentioned set of roles.

-   itil and sn\_csd.CSD Admin
-   itil and sn\_csd.CSD User

## About this task

If your software has a lease end date defined, and the software status is **Installed** or **Not Synced**, you can request an extension of the lease, pending any approvals your organization requires.

## Procedure

1.  Navigate to **Client Software Distribution 2.0** &gt; **Requested Software**.

    The list shows only the software you have requested from the service catalog.

2.  Select the record for the installed software whose lease you want to extend.

3.  Under **Related Links** click **Extend Lease**.

    ![Requested Software form](../../integrationhub/images/ExtendLease.png "Requested Software form")

4.  In the dialog box that appears, select a new lease end date in the calendar and click **OK**.

    You must select a date later than the current date.

    ![New Lease End Date Time dialog](../../integrationhub/images/NewLeaseEndDate.png)

    If the lease extension is subject to manager approval, you are notified of the decision. If the request is approved, a notification shows the new lease end date. If the new end date is within 5 days \(the default notification period\) of the date when you made the request, CSD 2.0 sends an immediate end-of-lease notification.

    **Important:** If lease extensions in your organization require approval, make sure the approver is available and has enough time to process your extension request. If the extension cannot be approved before the original end date expires, the software is revoked.


**Parent Topic:**[Client Software Distribution 2.0 application](../concept/csd-app-2.md)

