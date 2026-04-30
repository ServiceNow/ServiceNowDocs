---
title: Create monitors in bulk using Postman
description: Use Postman to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.
locale: en-US
release: yokohama
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Import synthetic monitors using API, Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Create monitors in bulk using Postman

Use Postman to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.

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

The Bulk Monitor Creation API uses a two-step process when accessed through Postman. First, create a POST request to upload your monitor data file and generate a job ID. Then, use the status check URL to verify monitor creation. Postman provides a user-friendly interface for testing the API and viewing formatted responses.

The same Postman configuration works for both JSON and CSV files, with only the file format selection differing.

## Procedure

1.  Open the Postman application.

2.  Create a new request by selecting the **+** button or **New** &gt; **HTTP Request**.

3.  Set the request method to **POST** from the drop-down menu, and enter the bulk import API endpoint base URL in the request URL field.

    Replace `{instance-name}` in the base URL with your ServiceNow instance name.

4.  Configure authentication credentials.

    1.  Select the **Authorization** tab below the **URL** field.

    2.  Select **Basic Auth** from the **Type** dropdown.

    3.  Enter your ServiceNow username in the **Username** field.

        Ensure this user has the synthetic admin role.

    4.  Enter your password in the **Password** field.

5.  Configure the request body to upload your monitor data file.

    1.  Select the **Body** tab.

    2.  Select **binary** as the body type.

    3.  Select the **Select File** button, and browse to your monitor data file location and select your JSON or CSV file.

        If you are uploading a CSV file, ensure it is properly formatted with all required columns. [Convert CSV file to JSON format](convert-csv-file-to-json-format.md)

6.  Add the filename as a query parameter in the URL, and select **Send** to submit the request.

    For example if your filename is monitors .json, then the filepath will be `https://<your-instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create?filename=monitors.json`

    The API returns a JSON response containing a job ID and status check URL.

    `{ "result": { "job_id": "abc123def456", "status": "processing", "status_check_url": "https://{instance-name}.service-now.com/api/now/synthetic/monitor/bulk/status/abc123def456" } }`

7.  Copy the status check URL from the response.

8.  Create a new GET request to check the job status.

    1.  Click the status check URL in the response, or manually create a new request.

        If the URL is click-able in Postman, it will automatically create a new GET request with the URL populated.

    2.  If creating manually, set the request method to **GET**.

    3.  Paste the status check URL \(`https://<your-instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/{job_id}` into the **ß** field.

        Replace \{job\_id\} with the job ID from the POST response.

9.  Configure authentication for the status check request.

    If you are in the same Postman workspace, the authorization may already be inherited. If not, repeat the Basic Auth configuration from step 4.

10. Select **Send** to check the job status.

    You can save the requests in a collection for reuse.

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

11. If the status is "processing", wait for few moments and select **Send** again to refresh the status.

    The system processes records asynchronously. Continue checking until the status changes to "complete".

12. If any monitors failed to create, review the error details in the response.

    1.  Expand the `details` array in the Postman response viewer to see individual error records.

    2.  Note the monitor name, error code, and reason for each failure.

    3.  Update your source JSON or CSV file to correct the identified issues.

        Common errors include:

        -   Missing required fields \(CMDB CI, location, method\)
        -   Invalid sys\_id references that don't exist in the instance
        -   Incorrect data formats or field names
    4.  Return to your original POST request and resubmit with the corrected file.


## Result

Monitors are created in your ServiceNow instance. Successfully created monitors are immediately available for use. Failed monitors are reported with specific error details in a structured JSON format that is easy to review in Postman's response viewer.

## Complete workflow example

**Step 1: Configure POST request**

-   Method: POST
-   URL: https://myinstance.service-now.com/api/now/synthetic/monitor/bulk/import
-   Authorization: Basic Auth \(username: admin, password: \*\*\*\*\*\*\*\*\)
-   Body: binary, file selected: monitor\_data.json
-   Headers: Content-Type: application/json, Accept: application/json

**Response received:**

```
{
  "result": {
    "job_id": "xyz789abc123",
    "status": "processing",
    "status_check_url": "https://myinstance.service-now.com/api/now/synthetic/monitor/bulk/status/xyz789abc123"
  }
}
```

**Step 2: Configure GET request for status check**

-   Method: GET
-   URL: https://myinstance.service-now.com/api/now/synthetic/monitor/bulk/status/xyz789abc123
-   Authorization: Basic Auth \(inherited from workspace\)

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

-   Save your Postman requests to a collection for future use and easy resubmission.
-   Verify your monitors in the ServiceNow UI by navigating to Synthetic Monitoring &gt; Monitors.
-   Configure additional monitor settings such as schedules, notifications, and thresholds as needed.

-   **[Convert CSV file to JSON format](convert-csv-file-to-json-format.md)**  
Convert your CSV file to JSON format to create synthetic monitors.

**Parent Topic:**[Import and create synthetic monitors in bulk using API](import-and-create-synthetic-monitors-in-bulk-using-apis.md)

