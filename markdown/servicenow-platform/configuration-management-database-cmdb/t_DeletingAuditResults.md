---
title: Delete an audit result
description: While audit results can be deleted, you cannot delete an audit result that has a follow-on task associated with it.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification audit results, Certification audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete an audit result

While audit results can be deleted, you cannot delete an audit result that has a follow-on task associated with it.

## Before you begin

Role required: none

## Procedure

1.  Navigate to one of these modules:

    -   **Compliance** &gt; **Desired State** &gt; **Audit Results**
    -   **Compliance** &gt; **Architecture Compliance** &gt; **Audit Results**
    -   **Compliance** &gt; **Scripted Audits** &gt; **Audit Results**
    The list groups by audit name.

2.  Select the check box for a result in the list, and then select **Delete** from the **Actions on selected rows** menu at the bottom of the list.

    **Note:** If the result record has a follow-on task, the **Delete** option is not available. If you select multiple records, some with and some without tasks, the system only deletes those records that do not have tasks.

3.  Click a date/time link to see the results for a specific CI.

    **Note:** The **Delete** button only appears on the form if the audit result does not have a follow-on task.

4.  Click **Delete**.


