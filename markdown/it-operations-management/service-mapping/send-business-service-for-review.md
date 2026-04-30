---
title: Send application service maps for review
description: After you map an application service, send it to the application service owner for review to make sure that the map is accurate.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Review and approval of application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Send application service maps for review

After you map an application service, send it to the application service owner for review to make sure that the map is accurate.

## Before you begin

Perform initial error fixing as described in [Fix application service errors in bulk](fix-bus-serv-errors-by-category.md) and [Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md).

Role required: service\_mapping\_admin

## About this task

While you can fix errors in bulk, you always send application services for review individually, one by one.

Sending application service maps for review is part of the [review and approval process](business-service-approval.md). Typically, you send each application service map for review twice: The first time for the initial owner review and the second time after you implemented owner feedback.

After the initial mapping of application services, you fix errors and send individual application services for review. The system creates a service process task assigned to the service instance owner and sends an email notification about it.

To see documentation for another review phase, click the relevant box in the diagram.

![Approval flow for individual application services.](../image/ApproveBSFlow.png)

## Procedure

1.  To send an service instance for review from the service instance form:

    1.  Open the service instance map.

    2.  Sort the list of planned application services by status and scroll to see services in **In progress** status, or use the filter to narrow the list.

    3.  Click the required service instance.

    4.  Click **Actions** &gt; **Send For Review**.

2.  Alternatively, send an service instance for review from its map:

    1.  Navigate to **Service Mapping** &gt; **Home**.

        The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

    2.  Click the **Approve** tile.

    3.  Click **Send For Review**.

    4.  Click the required service instance.

        The map for this service instance opens.

    5.  Click **Send For Review** in the upper corner of the window.


## What to do next

When you receive an email notification that the owner sent comments for this service instance, [review and implement the owner's requests](review-implement-business-service-maps.md).

**Parent Topic:**[Review and approval of application service maps](business-service-approval.md)

