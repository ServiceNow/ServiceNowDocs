---
title: System log
description: View warnings and errors for instance processes, records, and non-critical events, such as memory usage on the server machine.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# System log

View warnings and errors for instance processes, records, and non-critical events, such as memory usage on the server machine.

The following information is tracked in the system log:

-   Workflows
-   Configuration
-   Chats sessions
-   Transactions for each view of each page in the system, including load times for network, server, and browser
-   Inbound and outbound email
-   Events triggered in the system
-   Imports and integrations
-   System warnings, errors, and script logs
-   Upgrade information for any plugin activations, update sets, or system upgrades

Log entries appear for the current day only. To view other log files, use the log file browser. This log provides the following information for all occurrences:

<table id="table_mdc_nsk_sq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time of the logging activity for the locale of the machine running the instance.

</td></tr><tr><td>

Level

</td><td>

Type of message. The levels are Debug, Error, Warning, and Information. -   A warning is an error that has been handled and recovered.
-   An error is something that must be fixed.

</td></tr><tr><td>

Message

</td><td>

System-generated message regarding the nature of the occurrence.

</td></tr><tr><td>

Source

</td><td>

Name of the process or area affected by the occurrence. For example, the source of the occurrence might be EMAIL or Memory.

</td></tr><tr><td>

Source Package

</td><td>

Name of the application package associated with the occurrence. Click on the name to view the Store Application \[sys\_store\_app\] record for this package.

</td></tr></tbody>
</table>## Workflow logging

-   Each activity executed, including:
    -   Date and time started
    -   Date and time ended
    -   State, for example, Finished, Cancelled, Timed Out, Error
    -   Result
    -   Fault description, if there was an error
-   Transition history, including:
    -   Time of transition
    -   Activity transitioned from
    -   Activity transitioned to
    -   Which transition was triggered
-   Workflow log, including any log statements added to the workflow

## Configuration information

-   Action taken, including insert, update, and delete
-   Category of change
-   Comments recorded with the change
-   Name of the change
-   XML difference of the change
-   Update set the change is associated to
-   Date and time of the change
-   User who made the change
-   Table where the change was made
-   Name of the object being changed
-   Type of object being changed
-   View the change was made in, for changes to forms or lists

