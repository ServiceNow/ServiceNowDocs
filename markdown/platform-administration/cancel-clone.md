---
title: Cancel a clone
description: You can cancel requested, scheduled, and active clones without negatively impacting system stability or usability. Canceling a clone restores the target instance to the pre-clone state, retaining all original data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Cancel a clone

You can cancel requested, scheduled, and active clones without negatively impacting system stability or usability. Canceling a clone restores the target instance to the pre-clone state, retaining all original data.

## Before you begin

Role required: admin

## About this task

![Active clone log](../image/ActiveSystemClone.png "Active system clone")

After starting a clone, the **Clone Log** and **Database Table Clones** related lists appear on the form. These related lists show general log messages, and the details of individual tables respectively.

The duration a clone remains active varies upon the amount of data being cloned, and whether the source and target instance are in the same physical location. If a clone takes longer than anticipated, ServiceNow Technical Support can identify additional details about the clone progress.

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Live Clones** &gt; **Active Clones**.

    The system displays the list of currently active clones.

2.  Select the clone you want to cancel.

    The system displays the System Clone record.

3.  From **Related Links**, click **Cancel Clone**.

    The **Cancel Clone** modal displays.

    ![Cancel clone](../image/cancel-clone-telemetry.png)

4.  In **Specify Reason**, select a reason for the cancellation and click **OK**, or select **Others**, enter a reason in the text box and click **OK**.

    The system stops any current clone activities and sets the **State** to **Canceled**.


## What to do next

If you want to restart a canceled clone, you must create a [new clone request](t_StartAClone.md).

