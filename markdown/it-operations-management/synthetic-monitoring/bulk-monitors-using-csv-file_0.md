---
title: Example of bulk monitors using CSV file
description: This is an example of using a CSV file wrapped in a JSON object to create bulk monitors using terminal.
locale: en-US
release: yokohama
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Example of bulk monitors using CSV file

This is an example of using a CSV file wrapped in a JSON object to create bulk monitors using terminal.

## Step 1: Submit bulk job in CSV format

`curl -X POST "https://<instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create" \ -u "admin:password" \ -H "Content-Type: application/json" \ -H "Accept: application/json" \ -d @monitors.json`

## Response

`{ "result": { "job_id": "a1b2c3d4e5f6...", "status": "pending", "total_count": 2, "message": "Bulk job accepted for processing" } }`

## Step 2: Check the job status

`curl -X GET "https://<instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/{job_id}" \ -u "admin:password" \ -H "Accept: application/json"`

## Response

`{ "result": { "job_id": "a1b2c3d4e5f6...", "status": "completed", "total_count": 2, "success_count": 2, "error_count": 0, "processed_count": 2 } }`

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

