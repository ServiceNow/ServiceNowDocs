---
title: Queue registration form for recommendation process
description: The Recommended Actions use the queue registration form to create queues for recommendation process.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-05-15"
reading_time_minutes: 1
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Queue registration form for recommendation process

The Recommended Actions use the queue registration form to create queues for recommendation process.

<table id="table_cqx_1sf_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suffix

</td><td>

Suffix of the queue. For example, ra\_processor\_queue\_1.**Note:**

When creating additional custom queues beyond the default ra\_processor\_queue\_1, it's important to follow the established naming convention to ensure proper system recognition and functionality.

You should increment the trailing number in the queue name accordingly. For the second queue, name it as ra\_processor\_queue\_2 and so on. Continue this pattern for subsequent queues. Maintain the exact naming pattern to avoid configuration issues.

</td></tr><tr><td>

Application

</td><td>

Associated application name or identifier.

</td></tr><tr><td>

Queue

</td><td>

Title of the selected queue. For example, sn\_nb\_action.ra\_processor\_queue\_1.

</td></tr><tr><td>

Automatic Job Scheduling

</td><td>

Option to enable the automated job schedule for the queue.

</td></tr><tr><td>

Event Processing Order

</td><td>

Sequence in which events are processed.

</td></tr><tr><td>

Job Configuration type

</td><td>

Definition of how jobs are configured or processed.

</td></tr><tr><td>

Scale Factor

</td><td>

Number of polling jobs created for a particular queue. **Note:**

Each application node gets a job and an order according to queue. The customer can increase the value up to a maximum of 3. Increasing the scale factor creates more polling jobs according to application node for that queue.

For configuring queues:

-   You can create a maximum up to 8 custom queues for a recommended action use case.
-   Only one queue with one scale factor and a 10-second poll interval is shipped out of the base system.

For a higher load:

-   Increase number of queues.
-   Adjust scale factors accordingly.
-   Consider adding nodes, if needed.
-   Decrease polling interval.

</td></tr><tr><td>

Poll Interval

</td><td>

The poll interval is the waiting time before the queue is processed. It determines how often the queue is polled, that is, how frequently new events are fetched. **Note:** You can customize to a lower value \(for example, 1 second\) for reduced latency. The default poll interval is every 10 seconds.

You can reduce the interval to 1 second to decrease waiting time.

Decreasing the value to a lower number might cause acquiring most of the worker threads. Those threads are picked for RA use-case and can cause delays to other tasks on the instance.

The poll interval displays the duration in:

-   **Days**: Shows the number of days the queue has been added.
-   **Hours:** Indicates the duration \(in seconds, minutes, or hours\) that an event has been in the queue once added.

</td></tr><tr><td>

Description

</td><td>

Additional details about the queue.

</td></tr></tbody>
</table>