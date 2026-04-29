---
title: Manage table cleaner resource usage
description: Control the system resources used table cleaner by updating the table cleaner job.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deleting older or unwanted records in Core UI, Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Manage table cleaner resource usage

Control the system resources used table cleaner by updating the table cleaner job.

## Before you begin

Role required: admin

## About this task

By default, the table cleaner job runs asynchronously with multiple producer threads creating chunks of records for deletion and multiple consumer threads processing the chunks and deleting records.

You can mitigate the impact to system performance by starting a table cleaner run using a smaller dataset, checking resource usage as it runs, and then adjusting the number of producer and consumer threads as necessary to complete the job with minimal impact to your users.

## Procedure

1.  Open the DMJobs \[sys\_dm\_job\] table by entering `sys_dm_job.list` in the filter navigator.

2.  Select the DMTableCleaner job record.

3.  Change the number of producer threads devoted to creating chunks of records by updating the value in the **Max producers** field.

4.  Change the number of consumer threads devoted to deleting chunks of records by updating the value in the **Max consumers** field.

5.  Select **Update**.


## Result

Table cleaner begins the next run using the updated DMTableCleaner job configuration.

## What to do next

Check the status of the next table cleaner run by checking the values in the Chunks Errored column in the DMJob Runs \[sys\_dm\_run\] table. If a problem occurs, determine whether the issue occurred in all chunks or a single chunk. View the status of the individual chunks in the DMJob Chunks \[sys\_dm\_chunk\] table by checking the values in the Message and State columns.

**Parent Topic:**[Deleting older or unwanted records in Core UI](../concept/deleting-older-records.md)

