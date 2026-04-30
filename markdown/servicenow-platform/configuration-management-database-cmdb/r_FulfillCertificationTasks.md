---
title: View and resolve certification tasks
description: After you execute a certification schedule manually or at a scheduled time, the ServiceNow system performs certain actions.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data certification performance, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View and resolve certification tasks

After you execute a certification schedule manually or at a scheduled time, the ServiceNow system performs certain actions.

-   Creates certification tasks for any records that meet the filter requirements in the specified table, like tasks from the Configuration Item `[cmdb_ci]` table.
-   Assigns the new tasks to the user or group identified in one of these [certification schedule](../task/t_DefiningACertificationSchedule.md) fields:
    -   Assign to
    -   User
    -   Assign to group
    -   Group
-   Places the new tasks in the Work in Progress state.
-   Adds the certification schedule Short description and Assigned to values to the corresponding fields on the certification task record.
-   Adds the certification schedule Days to complete and Complete by date fields to the certification task record, based on when the task is created.

**Note:** If the certification filter does not match any CIs, the system sets the State to Closed Complete and the Percent complete to 100.

To view tasks assigned to you, navigate to **Data Certification** &gt; **Tasks** &gt; **My Tasks**. To resolve tasks assigned to you, see [Certify an element](../task/t_CertifyAnElement.md). For more information about purpose and usage of certification tasks, see [certification tasks](../concept/c_CertificationTasks.md).

The following information is tracked on the certification task record:

|Field|Description|
|-----|-----------|
|Number|An identification number for the certification task.|
|Assigned to|The user responsible for certifying the data.|
|Assignment group|The group responsible for certifying the data.|
|Complete by|\[Read-only\] A date field containing a deadline for the task. This field is automatically filled in based on the Days to Complete field on the certification schedule.|
|State|\[Read-only\] The current state of the certification task. The selections are: Work in Progress, Closed Incomplete, Closed Complete, and Cancelled.|
|Percent complete|The task progress as a percentage. This field is read-only when a task is in a Closed Incomplete, Closed Complete, or Cancelled state.|
|Escalation|\[Read-only\] The escalation level of the task. When 0–49% of the time to Complete By has elapsed, this field is set to Normal. At 50%, this field changes to Moderate and an email [reminder](r_SendCertificationTaskReminders.md) is sent to the task owner. At 75%, this field changes to High and an email reminder are sent to the task owner and the manager of the task owner. At 95%, this field remains set to High, but a second email reminder is sent to the task owner and manager.|
|Short Description|A short description of the task. This field is automatically filled in with the text from the certification schedule of the Task description field.|
|Work notes|Information about work performed on the certification.|

