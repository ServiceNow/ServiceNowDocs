---
title: Run a scheduled job to update TRM technical debt data in EA Workspace
description: Run a scheduled job to fetch the TRM technical debts data. You must run this job to see the products that are not approved for usage in your enterprise according to the TRM phases defined in Enterprise Architecture Workspace &gt; Setup&gt;TRM Phases&gt;All. You can schedule this job to periodically update the TRM technical debt for all business applications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage TRM technical debt, Managing the Technology Reference Model in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run a scheduled job to update TRM technical debt data in EA Workspace

Run a scheduled job to fetch the TRM technical debts data. You must run this job to see the products that are not approved for usage in your enterprise according to the TRM phases defined in Enterprise Architecture Workspace &gt; Setup&gt;TRM Phases&gt;All. You can schedule this job to periodically update the TRM technical debt for all business applications.

## Before you begin

Role required: admin

## About this task

You must run this job to see the products that are not approved for usage in your enterprise according to the TRM phases defined in Enterprise Architecture Workspace &gt; Setup&gt;TRM Phases&gt;All. You can schedule this job to periodically update the TRM technical debt for all business applications.

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job will be available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate TRM technical debts in the EA Workspace**.

3.  Select  ** Execute Now**.


## Result

After executing the scheduled job, the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table gets updated with the latest technical debt data for your application portfolio. It updates the values in the table each time after you run the job.

**Parent Topic:**[Manage TRM technical debt](../../concept/eaw-concept/eaw-manage-trm-technical-debt.md)

