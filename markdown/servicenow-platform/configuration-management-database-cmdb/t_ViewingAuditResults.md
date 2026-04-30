---
title: View an audit result
description: To generate certification results, you must first create and run an audit.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Certification audit results, Certification audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View an audit result

To generate certification results, you must first create and run an audit.

## Before you begin

Role required: none

## Procedure

1.  Navigate to one of the following locations:

    -   **Compliance** &gt; **Desired State** &gt; **Audit Results**
    -   **Compliance** &gt; **Architecture Compliance** &gt; **Audit Results**
    -   **Compliance** &gt; **Scripted Audits** &gt; **Audit Results**
    -   **Data Certification** &gt; **Schedules** &gt; **Audit results**
2.  From any audit results list, you can edit the filter to show the results for any audit type.

    The results filter by audit type and grouped by audit number. Within the groups, results list by date, from oldest to newest.

3.  You can open the audit record, the CI record, or the follow-on tasks from this list.

    **Note:** The **Audit type** field was set automatically when the audit result was created and cannot be changed. For scripted audits, the audit type is set when you create the audit record.

    Audit results show this information:

<table id="table_ftx_tjp_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time the audit ran.

</td></tr><tr><td>

Document

</td><td>

Record that was certified, such as a configuration item \(CI\).

</td></tr><tr><td>

State

</td><td>

Results of certification for each condition evaluated. The three possible states are:

-   Certified A certified record is one that passed all conditions. The instance generates only one audit result for a certified record.
-   Failed Records that are not certified have an audit result for each failed condition. The **Column name**, **Desired value**, **Discrepancy value**, and **Follow on task**are only populated for failed results.
-   Pending A pending state indicates that the audit is incomplete. Data certification audits use this state when a result is awaiting user input.


</td></tr><tr><td>

Column name

</td><td>

Audited field, relationship, or related list column that did not match the expected state.

</td></tr><tr><td>

Desired value

</td><td>

Attribute or relationship required for this record that was not found, from the condition in the expected state template. For data certification, this column is blank if the record has a state of Failed or Pending.

</td></tr><tr><td>

Discrepancy value

</td><td>

Actual value of the attribute that did not match the expected state. The follow-on task, if provided, tracks resolution of this discrepancy. In a list of results for the **Data Certification** audit type, this column is blank if the record has a state of Certified or Pending.

</td></tr><tr><td>

Follow on task

</td><td>

Link to the follow-on task generated for remediating a discrepancy.

</td></tr><tr><td>

Audit

</td><td>

Link to the audit record that produced the results.

</td></tr><tr><td>

Threshold

</td><td>

State of an audited, desired state field with a defined failure threshold. This threshold is the acceptable number of failures for a desired state field within a specified health window and is configured in the Audit form. Possible threshold states for the results are:

-   In Limit
-   Exceeded


</td></tr><tr><td>

Stability

</td><td>

Stability state of a CI. Stability state is based on the number of times the audit result for a desired state field changes from Certified to Failed within a specified health window. Possible stability states are:

-   Stable
-   Unstable


</td></tr></tbody>
</table>
