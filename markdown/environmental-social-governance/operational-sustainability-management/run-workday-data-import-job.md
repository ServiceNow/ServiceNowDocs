---
title: Run the Workday data import job
description: Run the scheduled integration job that runs that pulls data for the activated reports based on the frequency specified in the job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/run-workday-data-import-job.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with Workday, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Run the Workday data import job

Run the scheduled integration job that runs that pulls data for the activated reports based on the frequency specified in the job.

## Before you begin

At least one [Workday report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/activate-the-workday-reports.md) must be activated.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Search** field, enter `Workday`.

3.  From the filtered search results, select and open the **Workday data import** scheduled job.

4.  Select **Execute Now**.


