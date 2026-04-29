---
title: Create monitors in bulk using Terminal
description: Use curl commands in Terminal to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.
locale: en-US
release: australia
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Import synthetic monitors using API, Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Create monitors in bulk using Terminal

Use curl commands in Terminal to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.

## Before you begin

Role required: sn\_sow\_synthetics.synthetics\_admin or sn\_sow\_synthetics.synthetics\_editor

-   Valid ServiceNow instance credentials
-   Access to Http endpoint
-   Base URL: `https://<your-instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create`
-   Prepared raw JSON or CSV file with monitor data containing required fields:
    -   Monitor name
    -   HTTP endpoint sys\_id
    -   Parent service sys\_id
    -   Location sys\_id
    -   sys id of support group
    -   interval \(frequency\)
    -   Method \(\`GET\`, \`POST\`, \`PUT\`, \`DELETE\`, \`PATCH\`, \`HEAD\`\)
    -   Assertion field

## About this task

The Bulk Monitor Creation API uses a two-step process when accessed through Terminal. First, upload your monitor data file using a curl command to generate a job ID. Then, check the job status to verify monitor creation. The API processes records asynchronously and provides detailed feedback on successful creations and errors.

Different curl commands are required depending on whether you are uploading a JSON or CSV file.

## Procedure

1.  Open Terminal on your system.

2.  Navigate to the directory containing your monitor data file.

3.  Execute the appropriate curl command to upload your file and create a job ID.

    **For JSON files:**

    ```
    curl -X POST "https://{your-instance}.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create" \
      -H "Content-Type: application/json" \
      -H "Accept: application/json" \
      -u "admin:password" \
      -d @{filename}.json
    ```

    **For CSV files:**

    ```
    curl -X POST "https://{your-instance}.service-now.com/api/sn_now_synthetics/v1/synthetics_async_bulk_create?filename=filename.csv" \
      -H "Content-Type: text/csv" \
      -H "Accept: application/json" \
      -u "admin:password" \
      --d "$(jq -Rs '{csv_content: .}'filename.csv"
    ```

    Replace the following placeholders:

    -   `{your-instance}`: Your ServiceNow instance name
    -   `{filename}`: The name of your monitor data file
    The API returns a response containing a job ID and status check URL.

    ```
    {
      "result": {
        "job_id": "abc123def456",
        "status": "processing",
        "status_check_url": "https://{your-instance}.service-now.com/api/now/synthetic/monitor/bulk/status/abc123def456"
      }
    }
    ```

4.  Copy the status check URL from the response.

5.  Execute the status check curl command to verify job processing status.

    ```
    curl -X GET "https://{your-instance}.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/{job_id}" \
      -H "Accept: application/json" \
      -u "{username}:{password}"
    ```

    The API returns one of the following status responses:

    **Processing status:**

    ```
    {
      "result": {
        "job_id": "abc123def456",
        "status": "processing",
        "total_records": 10,
        "processed_records": 3
      }
    }
    ```

    **Complete status \(successful\):**

    ```
    {
      "result": {
        "job_id": "abc123def456",
        "status": "complete",
        "total_records": 10,
        "successful_records": 10,
        "failed_records": 0,
        "details": []
      }
    }
    ```

    **Complete status \(with errors\):**

    ```
    {
      "result": {
        "job_id": "abc123def456",
        "status": "complete",
        "total_records": 10,
        "successful_records": 8,
        "failed_records": 2,
        "details": [
          {
            "name": "Monitor_API_001",
            "status": "failed",
            "error_code": "MISSING_REQUIRED_FIELD",
            "reason": "CMDB CI is required"
          },
          {
            "name": "Monitor_API_002",
            "status": "failed",
            "error_code": "INVALID_REFERENCE",
            "reason": "Location not found for this sys_id"
          }
        ]
      }
    }
    ```

6.  If the status is "processing", wait for few moments and repeat the status check command.

    The system processes records asynchronously. Continue checking until the status changes to "complete".

7.  If any monitors failed to create, review the error details in the response.

    1.  Identify the failed monitor name from the compiled details.

    2.  Review the error code and reason provided.

    3.  Update your source JSON or CSV file to correct the data issues.

        Common errors include:

        -   Missing required fields \(CMDB CI, location, method\)
        -   Invalid sys\_id references that don't exist in the instance
        -   Incorrect data formats
    4.  Resubmit the corrected file by repeating the upload curl command.


## Result

Monitors are created in your ServiceNow instance. Successfully created monitors are immediately available for use. Failed monitors are reported with specific error details, allowing you to correct the data and resubmit.

## Complete workflow example

**Step 1: Upload JSON file**

```
curl -X POST "https://myinstance.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -u "admin:password123" \
  -d @monitor_data.json
```

**Response:**

```
{
  "result": {
    "job_id": "xyz789abc123",
    "status": "processing",
    "status_check_url": "https://myinstance.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/status/xyz789abc123"
  }
}
```

**Step 2: Check status**

```
curl -X GET "https://myinstance.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/status/xyz789abc123" \
  -H "Accept: application/json" \
  -u "admin:password123"
```

**Final response:**

```
{
  "result": {
    "job_id": "xyz789abc123",
    "status": "complete",
    "total_records": 5,
    "successful_records": 5,
    "failed_records": 0
  }
}
```

## What to do next

After successful creation, verify your monitors in the ServiceNow UI by navigating to **Synthetic Monitoring** &gt; **Monitors**. You can configure additional monitor settings and schedules, as needed.

**Parent Topic:**[Import and create synthetic monitors in bulk using API](import-and-create-synthetic-monitors-in-bulk-using-apis.md)

