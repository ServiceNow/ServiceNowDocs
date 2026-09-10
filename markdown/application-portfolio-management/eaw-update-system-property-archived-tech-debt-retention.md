---
title: Update the retention period for archived technical debts
description: Change how long an Archived technical debt record is retained before the Delete Archived Tech Debts scheduled job permanently deletes it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-update-system-property-archived-tech-debt-retention.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [archived technical debt, retention period]
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Update the retention period for archived technical debts

Change how long an Archived technical debt record is retained before the **Delete Archived Tech Debts** scheduled job permanently deletes it.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

The **sn\_apm\_tpm.monthsToDeleteArchivedTechDebt** property controls how many months an Archived technical debt record is kept before permanent deletion. The **Delete Archived Tech Debts** scheduled job runs automatically on the first day of every month and reads this property. It deletes Archived records whose **Updated** value is older than the configured number of months. The default retention period is 12 months.

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Open the **sn\_apm\_tpm.monthsToDeleteArchivedTechDebt** system property.

3.  In the **Value** field, enter the number of months to retain Archived technical debt records before permanent deletion.

4.  Select **Update**.

    The **Delete Archived Tech Debts** job applies the new retention period when it runs automatically on the first day of the next month. To apply the change immediately, run the job manually. For information, see [Run the Delete Archived Tech Debts job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-delete-archived-tech-debts.md).


**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Run the Delete Archived Tech Debts job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-delete-archived-tech-debts.md)

[Scheduled jobs for TLM in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm-scheduled-jobs.md)

