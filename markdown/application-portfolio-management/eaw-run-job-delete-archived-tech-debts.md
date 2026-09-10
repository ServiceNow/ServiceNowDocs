---
title: Run the Delete Archived Tech Debts job
description: Run the Delete Archived Tech Debts scheduled job manually or modify its default monthly schedule to match your maintenance window.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-run-job-delete-archived-tech-debts.html
release: zurich
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run the Delete Archived Tech Debts job

Run the **Delete Archived Tech Debts** scheduled job manually or modify its default monthly schedule to match your maintenance window.

## Before you begin

Role required: admin

## About this task

The job runs monthly by default on day 1 at 00:00:00 in the instance time zone. You can modify the schedule to align with your maintenance windows. You can also run the job on demand to immediately remove archived technical debt records that exceed the retention period.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the Name column, search for and open **Delete Archived Tech Debts**.

3.  To modify the schedule, update the **Run**, **Day**, **Time zone**, or **Time** fields.

4.  Select **Update** to save your changes

5.  To run the job immediately instead of waiting for its next scheduled run, select **Execute Now**.


## Result

The job deletes archived technical debt records whose **Updated** value is older than the retention period set in the system property **sn\_apm\_tpm.monthsToDeleteArchivedTechDebt**. For details on setting that retention period, see [Update the retention period for archived technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-update-system-property-archived-tech-debt-retention.md).

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[Update the retention period for archived technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-update-system-property-archived-tech-debt-retention.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Scheduled jobs for TLM in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-tpm-scheduled-jobs.md)

