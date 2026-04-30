---
title: Process job states in RPA Hub
description: A process job represents the execution of a bot process on a robot.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-10-02"
reading_time_minutes: 2
keywords: [Success, Failed, Canceled, Skipped, Abandoned, Running, RPA Hub]
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Process job states in RPA Hub

A process job represents the execution of a bot process on a robot.

<table id="table_olx_3hf_xcc"><thead><tr><th>

State

</th><th>

Scenario

</th></tr></thead><tbody><tr><td>

Running

</td><td>

When a bot process is being executed by a robot, the status of the process job is updated to **Running**.

</td></tr><tr><td>

Canceled

</td><td>

When a bot process execution is canceled manually, the process job status is updated to **Canceled**.If Bot process 1 is already executing, and Bot process 2 with force start enabled is triggered, then the process job status of Bot process 1 is updated to **Canceled**, and the process job status of Bot process 2 is updated to **Running**.

</td></tr><tr><td>

Success

</td><td>

After a bot process is executed successfully by a robot, the process job status is updated to **Success**.

</td></tr><tr><td>

Failed

</td><td>

When a bot process execution fails to complete, the process job status is updated to **Failed**.

</td></tr><tr><td>

Skipped

</td><td>

Consider the following scenarios when more than one bot processes are triggered for the same unattended robot:-   If Bot process 1 is already executing and Bot process 2 with force start disabled is triggered, then the process job status of Bot process 2 is updated to **Skipped**.
-   If two bot processes, BP1 and BP2, are scheduled to run on the same robot at the same time and BP2 has lower priority \(higher priority order number\), then the process job status of BP2 is updated to **Skipped**.
-   If two bot processes, BP1 and BP2, with the same priority order are scheduled to run on the same robot at the same time, then only one of the bot process would be selected randomly for running and the process job status of the other one is updated to **Skipped**.
-   If Bot process 1 is triggered and robot is waiting to login, and in the mean time Bot process 2 is triggered, then process job status of Bot process 2 is updated to **Skipped**.
-   The **Start process** action is invoked for Bot process 1. Until the execution starts, if other bot processes are triggered then the process jobs of all other start process requests are updated to **Skipped**.
-   When a robot comes back to responsive state, it will start to receive start process requests that were triggered when the robot was in the unresponsive state. The latest request which falls under the configured threshold is updated to **Running** and all the older requests are updated to **Skipped**.

</td></tr><tr><td>

Abandoned

</td><td>

-   For any robot type, if a bot process was previously executing and the process job status was not updated to **Completed**, and a new process job is created, then the status of the previously executing process job is updated to **Abandoned**.
-   When a process job is running, the robot state is moved from **Busy** state to any other state.

For example, when a process job is executing locally in the robot machine, a robot may fail to update RPA Hub with its heartbeat call due to network failure, certificate authentication failure, machine user profile corruption, and so on.

In all such scenarios, when the robot calls the RPA Hub after an interruption, and then updates its status from **Busy** or **Disconnected** to **Available**, then the status of the last known process job is changed to **Abandoned**.


</td></tr></tbody>
</table>