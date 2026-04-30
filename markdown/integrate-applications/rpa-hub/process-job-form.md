---
title: Process job form in RPA Hub
description: Use the Process job form to view a list of the execution logs of a bot process.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Process job form in RPA Hub

Use the Process job form to view a list of the execution logs of a bot process.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the process job.

</td></tr><tr><td>

Process

</td><td>

Name of the associated bot process.

</td></tr><tr><td>

Robot

</td><td>

Assigned robot that is running on the bot process.

</td></tr><tr><td>

State

</td><td>

State of the process job:-   Success
-   Failed
-   Running
-   Skipped
-   Canceled
-   Abandoned

For more information about process job states and their scenarios, see [Process job states in RPA Hub](../concept/process-job-states-rpa.md).

</td></tr><tr><td>

Storage

</td><td>

Storage location of the logs:-   **Instance**
-   **Robot Machine**

</td></tr><tr><td>

Triggered By

</td><td>

Source of the trigger.-   **Schedule**- If the automation is triggered via a schedule.
-   **API**- If the automation is triggered by a flow
-   **Manual**- If the attended automation is triggered by a user or if the unattended automation is triggered by **Start Process**.
-   **Embedded Task Automation**- If the attended automation is triggered from the ServiceNow form.

For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).


</td></tr><tr><td>

Execution Log Status

</td><td>

Status on the availability of the execution logs:-   **No Logs**
-   **Sync in progress**
-   **Complete**

 The available logs are viewed on the RPA Desktop Design Studio.

</td></tr><tr><td>

Graceful Stop

</td><td>

Indicates whether the Graceful Stop is executed or not.If it is marked true, the associated bot process is stopped gracefully instead of stopping abruptly.

</td></tr><tr><td>

Started At

</td><td>

Start date and time of the process job.

</td></tr><tr><td>

Completed At

</td><td>

End date and time of the process job.

</td></tr><tr><td>

Duration

</td><td>

Time taken to complete the automation.

</td></tr><tr><td>

Message

</td><td>

Any information or error message returned by the robot.

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[View the process jobs of a bot process](../task/view-process-jobs-botprocess.md)

[View RPA Hub process jobs for all bot processes](../task/view-process-jobs.md)

