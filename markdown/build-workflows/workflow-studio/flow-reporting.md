---
title: Flow execution details retention
description: Due to the large amount of data consumed by flow execution details, your instance uses data retention policies to delete this data after a set time period.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Flow administration, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow execution details retention

Due to the large amount of data consumed by flow execution details, your instance uses data retention policies to delete this data after a set time period.

## Generating flow execution details

By default, the system only generates execution details when you run a test. To generate flow execution details, see [Activate flow reporting](../task/enable-flow-reporting.md#)

## Scheduled table cleanup

The system uses a standard table cleaner records to determine when to remove execution details. Each type of flow execution content is stored in its own table and has its own retention period. Once a record is older than its default retention period, it is deleted if it is in a completed state. To learn more about how to find and configure table cleaner records, see [Table cleaner](https://www.servicenow.com/docs/access?context=table-cleaner&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_hmm_shn_z2b"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Default retention period

</th></tr></thead><tbody><tr><td>

sys\_flow\_context

</td><td>

Parent table that stores all Workflow Studio context records and their associated process plans. Context records store the state and references to the data used to run a flow or action. See the child tables for context records in specific states.

</td><td>

-   2 weeks for completed flows
-   6 weeks for flows in the error or cancelled state

 **Warning:** Deactivating or increasing the retention period of Flow Context records can negatively impact instance performance. Retaining more flow contexts can impact flow performance and the ability to use new flow features.

</td></tr><tr><td>

sys\_flow\_context\_chunk

</td><td>

Child table that stores context records and runtime data for currently running flows and actions. This table replaces the sys\_json\_chunk table as the location to store data for active context records. A running flow or action can be in one of these states.-   Continue Sync
-   In Progress
-   Queued
-   Waiting

 **Danger**

Do not change or delete data in this table. Workflow Studio uses this table for flows and actions that are in an active state.

</td><td>

The system removes these records when the flow stops running and creates an entry in the sys\_flow\_context\_chunk\_archive table.

</td></tr><tr><td>

sys\_flow\_context\_chunk\_archive

</td><td>

Child table that stores context records and runtime data for flows and actions that have stopped running. This table replaces the sys\_json\_chunk table as the location to store data for inactive context records. A stopped flow or action can be in one of these states.-   Cancelled
-   Complete
-   Error

 **Note:** Workflow Studio uses this table for flows and actions that are in an inactive state.

</td><td>

Removed when the associated sys\_flow\_context record is removed.-   2 weeks for completed flows
-   6 weeks for flows in the error or cancelled state

</td></tr><tr><td>

sys\_flow\_report\_doc

</td><td>

Parent table that stores references to Workflow Studio context records that have execution detail reporting data available. See the child tables for the execution details of flows and actions in specific states.

</td><td>

The system removes these records when it removes the parent context record from sys\_flow\_context.

</td></tr><tr><td>

sys\_flow\_report\_doc\_chunk

</td><td>

Child table that stores the reporting data and execution details for currently running flows and actions. A running flow or action can be in one of these states.-   Continue Sync
-   In Progress
-   Queued
-   Waiting

 **Danger**

Do not change or delete data in this table. Workflow Studio uses this table for flows and actions that are in an active state.

</td><td>

The system removes these records when the flow stops running and creates an entry in the sys\_flow\_report\_doc\_chunk\_archive table.

</td></tr><tr><td>

sys\_flow\_report\_doc\_chunk\_archive

</td><td>

Child table that stores the reporting data and execution details for flows and actions that have stopped running. A stopped flow or action can be in one of these states.-   Cancelled
-   Complete
-   Error

 **Note:** This table replaces the sys\_json\_chunk table as the location to store reporting data for inactive execution details.

</td><td>

The system removes these records when it removes the parent context record from sys\_flow\_context\_chunk\_archive.-   2 weeks for completed flows
-   6 weeks for flows in the error or cancelled state

</td></tr><tr><td>

sys\_json\_chunk

</td><td>

Table that stores compiled process plans for future, running, and completed flows and actions created prior to the San Diego release.**Danger**

Do not change or delete data in this table. Workflow Studio uses this table for flows and actions that are in an active state.

</td><td>

The system removed these records when it removed the parent record.

</td></tr><tr><td>

sys\_flow\_log

</td><td>

Table that stores replicated log entries from the Log \[syslog\] table. Enables users to correlate logs with flow contexts.

</td><td>

The system removes these records in 28 days when the table is rotated or when it removes the context record, whichever comes first.

 The table rotation on sys\_flow\_log is configurable. For more information, see [Table rotation](https://www.servicenow.com/docs/access?context=c_TableRotation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

sys\_flow\_plan\_context\_binding

</td><td>

Table that stores a unique identifier for each context record and the trigger that started it. Whenever a triggering event occurs, the system calculates the unique identifier and compares it to a sys\_flow\_plan\_context\_binding record. If the calculated unique identifier matches an existing sys\_flow\_plan\_context\_binding record, then the triggered flow is not started.**Note:** This unique identifier is used to determine when to run flows with either the "run once" or "for each unique change" conditions.

</td><td>

The system removes these records 12 months after creation.**Important:** The system may rerun flows whose unique identifier was removed by the retention policy. For example, if the trigger conditions of a "run once" flow are met, and the sys\_flow\_plan\_context\_binding record was removed, then a new unique identifier is created and the flow runs.

</td></tr></tbody>
</table>## Unavailable flow data

A message displays at the top of the flow report to indicate that action reports are not available for a flow because of table cleanup. The **Show Action Details** link and Action states are not available in this case. A similar message is shown to indicate when reporting for a flow has been deactivated. In this case, a link to the report settings also displays.

![Flow execution details page displaying the data retention notification, The action details for this flow have been removed according to the report retention policy.](../images/flow-execution-cleanup-notification.png "Sample flow execution details with data removed by the report retention policy")

## Recovery options

[Contact Customer Service and Support](http://www.servicenow.com/support/contact-support.html) to restore data from an instance backup.

To know the period until which a data recovery request is accepted, see the [Instance Backup and Recovery \[KB0547654\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547654) article in the Now Support Knowledge Base.

**Parent Topic:**[Flow administration](flow-administration.md)

