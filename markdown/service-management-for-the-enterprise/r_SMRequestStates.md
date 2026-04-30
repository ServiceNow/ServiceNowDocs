---
title: Request states
description: Service Management requests follow a specific life cycle and move through a series of states, which are displayed in the State field on the request record.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request Management in a Service Management application, Service Management]
---

# Request states

Service Management requests follow a specific life cycle and move through a series of states, which are displayed in the **State** field on the request record.

The request states displayed depend on the SM application, as indicated in the table.

**Note:** The **State** field on the request record is always read-only.

<table id="table_ds4_hf5_1r"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Request initiator adds information about the work to be done.

</td></tr><tr><td>

Awaiting Qualification

</td><td>

Initiator fully describes the request, and qualifier can process the request. This state is valid only for the following SM applications:-   Field Service Management

</td></tr><tr><td>

Qualified

</td><td>

Request is fully qualified, meaning that all technical information to complete the request tasks has been added, but work has not started. This state is valid only for the following SM applications:-   Field Service Management

</td></tr><tr><td>

Awaiting Approval

</td><td>

When the information is complete enough for review by an approver, the request is marked ready for approval. This state is valid only for the Facilities Service Management application.

</td></tr><tr><td>

Approved

</td><td>

The appropriate approver approves the request. This state is valid only for the Facilities Service Management application.

</td></tr><tr><td>

Work In Progress

</td><td>

Work has started.

</td></tr><tr><td>

Closed Complete

</td><td>

Request was completed to specification.

</td></tr><tr><td>

Closed Incomplete

</td><td>

Request could not be completed as specified.

</td></tr><tr><td>

Canceled

</td><td>

Request was canceled.

</td></tr></tbody>
</table>In addition to the **State** field, the different request task states are also shown visually at the top of each task record with the process flow formatter.

**Note:** If the **State flows are enabled** option in the configuration screen is not selected, the process flow formatter is removed. If you added states to the request and task tables, those states are visible on the request form.

**Parent Topic:**[Request Management in a Service Management application](../concept/rm-sm-application.md)

