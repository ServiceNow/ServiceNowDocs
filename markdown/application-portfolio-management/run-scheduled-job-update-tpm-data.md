---
title: Run a scheduled job to generate TPM lifecycle data
description: Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run a scheduled job to generate TPM lifecycle data

Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.

## Before you begin

Role required: admin

## About this task

The scheduled job **Populate TPM Discovered Technologies and Lifecycles** is created to fetch the technology lifecycle data for your technology portfolio. This job can be run on-demand to calculate the technology lifecycle risk. The scheduled job executes the script generating the lifecycle risk dates, including end of support date, end of extended support date, and end of life date for your software and hardware models.

**Note:** The data for software products is displayed only if the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate TPM Discovered Technologies and Lifecycles**.

3.  Select  ** Execute Now**.


## Result

After executing the scheduled job, the engine automatically stores the technologies and lifecycle values in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. It updates the values in the table each time after you run the job.

## What to do next

To know the status of the scheduled job, refer to the TPM Discovered Technology Run Logs \[sn\_apm\_tpm\_discovered\_technology\_run\_log\] table. To view the technology lifecycle information, refer to the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. You can view the results in the Enterprise Architecture Workspace &gt; Setup &gt; Logs &gt; TPM Logs page.

**Note:** In the TPM Logs page, if you don’t see any change in the complete percentage, use either of the following steps to confirm that the job is running:

-   Navigate to Enterprise Architecture Workspace &gt; Technology Portfolio &gt; TPM Lifecycles and use the **Refresh** icon to refresh the list of TPM lifecycles. If the count increases, then it means that the scheduled job is running.
-   As an Admin user, navigate to System Diagnostics &gt; Active Transactions \(All Nodes\) and verify that the job is in the Active Cluster Transactions list.

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

