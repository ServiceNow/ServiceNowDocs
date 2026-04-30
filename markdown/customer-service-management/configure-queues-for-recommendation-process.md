---
title: Configure queues for recommendation process
description: Enable administrators to configure custom queues to handle Recommended Actions asynchronously.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-23"
reading_time_minutes: 1
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configure queues for recommendation process

Enable administrators to configure custom queues to handle Recommended Actions asynchronously.

## Before you begin

Role required: admin or sn\_nb\_action.next\_best\_action\_admin

## Procedure

1.  Navigate **All** &gt; **** &gt; **System Policy** &gt; **Queue Registry**.

2.  Select an existing queue from the queue registry list.

3.  On the queue registration form, fill in the fields.

    For a description of the field values, see:[Queue registration form for recommendation process](../reference/ra-queue-registration-form.md).

4.  Select **Submit**.

5.  Select the recently added queue.

    **Note:** When the new queue is submitted, the status entry is **Active**.

6.  Update the number of jobs for this queue according to your requirement.

7.  If you want to roll back a queue to its previous configurations without automated job scheduling, select the rollback related link on the queue registration form.

    The rollback related link shows up only if you are in an automated jobs scheduling configuration.

8.  After the last queue registration is complete, ensure that the RA Admin \[sn\_nb\_action.next\_best\_action\_admin\] must update the number of queues available in the value field of the **sn\_nb\_action.ra\_processor\_number\_of\_queues** system property.

    For example, if the number of queue is increased from 2 to 3, then the value must be updated to 3 \(ra\_processor\_queue\_3\). The minimum and maximum values are 1 and 8 respectively. If the given value isn’t withing this range, then 1 is considered as the default value.


