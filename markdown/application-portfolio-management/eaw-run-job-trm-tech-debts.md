---
title: Update TRM technical debt data using scheduled job
description: Run the scheduled job to update technical debt data based on Technology Reference Model \(TRM\) phases. This job identifies products not approved for use in your enterprise and can be scheduled to run periodically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-run-job-trm-tech-debts.html
release: zurich
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update TRM technical debt data using scheduled job

Run the scheduled job to update technical debt data based on Technology Reference Model \(TRM\) phases. This job identifies products not approved for use in your enterprise and can be scheduled to run periodically.

## Before you begin

Role required: admin

## About this task

Running this job populates technical debt records for business applications based on the TRM phases you define. The job compares installed products against approved TRM phases to identify technical debt.

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and open the **Populate TRM technical debts in the EA Workspace** scheduled job.

3.  Select **Execute Now**.


## Result

After executing the scheduled job, the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table gets updated with the latest technical debt data for your application portfolio. It updates the values in the table each time after you run the job.

Existing technical debt records aren't deleted and re-created on each run. Instead, each record's **State** moves between Active, Resolved, and Archived based on what the job finds. For details, see [TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-states.md).

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[View Technology Reference Model technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/view-trm-tech-debt.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-setup-tech-debt.md)

[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-trm-governing-fields.md)

