---
title: Run a scheduled job to generate TPM lifecycle data
description: Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run a scheduled job to generate TPM lifecycle data

Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.

## Before you begin

Role required: admin

## About this task

The scheduled job **Populate TPM Discovered Technologies and Lifecycles** is created to fetch the technology lifecycle data for your technology portfolio. This job can be run on-demand to calculate the technology lifecycle risk. The scheduled job executes the script generating the lifecycle risk dates, including end of support date, end of extended support date, and end of life date for your software and hardware models.

**Note:** The data for software products is displayed only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate TPM Discovered Technologies and Lifecycles**.

3.  Select  ** Execute Now**.


## Result

After executing the scheduled job, the engine automatically stores the technologies and lifecycle values in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. It updates the values in the table each time after you run the job.

## What to do next

To know the status of the scheduled job, refer to the TPM Discovered Technology Run Logs \[sn\_apm\_tpm\_discovered\_technology\_run\_log\] table. To view the technology lifecycle information, refer to the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. You can view the results in the Portfolio &gt; Technology Portfolio Management &gt; Logs page.

**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](../../concept/eaw-concept/eaw-work-with-tpm.md)

