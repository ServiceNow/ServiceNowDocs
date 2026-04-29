---
title: Push a request to Field Service Marketplace
description: Create a marketplace request and push to contractors using Field Service Marketplace.Use the Add Contractor button to add an eligible contractor to the list of marketplace participants once a work order task has already been pushed to Marketplace.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Allowing contractors to bid on work orders and tasks, Scheduling and dispatching, Use, Field Service Management]
---

# Push a request to Field Service Marketplace

Create a marketplace request and push to contractors using Field Service Marketplace.

## Before you begin

Role required: sn\_mktplace\_core.mktplace\_requestor

Ensure that the Field Service Marketplace plugin is active. For more information, see [Activate Field Service Marketplace](activate-contractor-marketplace.md).

The work order task must have the Marketplace task flag set to true.

## About this task

You can push tasks to contractors on Field Service Marketplace. The following procedure is completed using Playbooks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher** &gt; **Dispatcher Workspace**.

2.  Select a work order task.

3.  Select the **More Actions** icon \(![More actions icon.](../image/more_actions1.png)\).

4.  Select **Push to Marketplace**.

5.  Select an **Engagement method**.

6.  Enter a **Start** and **End** time for the request.

    The start and end fields set the duration the task is available on the marketplace. The default values are based on the lead time and duration fields of the selected engagement method.

7.  Select the contractors who can respond to the request.

8.  Select **Push request**.


## Result

The request is sent to the contractors. Contractors can respond with time or cost estimates depending on the configuration. For more information, see [Create a marketplace engagement method](create-marketplace-eng-mthd.md).

## What to do next

After receiving a response, review the responses to assign the task to a contractor or respond with other inquiries. For more information, see [Assign a task to a contractor on Field Service Marketplace](review-rspons-fsm-mrktplc.md).

## Add a contractor to Marketplace participants post-push

Use the Add Contractor button to add an eligible contractor to the list of marketplace participants once a work order task has already been pushed to Marketplace.

### Before you begin

Role required: sn\_mktplace\_core.mktplace\_requestor

Ensure that the Field Service Marketplace plugin is active. For more information, see [Activate Field Service Marketplace](activate-contractor-marketplace.md).

The work order task must have already been pushed to Marketplace.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher** &gt; **Dispatcher Workspace**.

2.  Select a work order task that has already been pushed.

3.  In **Marketplace Participants**, select the Add Contractor button and choose the contractor you want added to the list of eligible marketplace participants.


### Result

The contractor you selected has been added to the eligible list of marketplace participants.

