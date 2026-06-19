---
title: Synthetic Monitoring Developer Guide
description: Use Synthetic Monitoring APIs create multiple synthetic monitors in a single operation.Create multiple synthetic monitors simultaneously by importing raw JSON or CSV files through the SyntheticsAsyncBulkCreate API.Use curl commands in Terminal to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the SyntheticsAsyncBulkCreate API.Use Postman to create multiple synthetic monitors simultaneously by importing JSON files through the SyntheticsAsyncBulkCreate API.The JSON file should contain an array of monitor objects, either directly or wrapped in a checks or monitors property.CSV files must include a header row followed by data rows.This is an example of using a CSV file wrapped in a JSON object to create bulk monitors using terminal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/synth-monitor\_dev-guide.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 10
breadcrumb: [Developer guides, API implementation and reference]
---

# Synthetic Monitoring Developer Guide

Use Synthetic Monitoring APIs create multiple synthetic monitors in a single operation.

This developer guide provides information on how to use the [SyntheticsAsyncBulkCreate API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/synth-async-api.md) to bulk create monitors from Postman or Terminal.

For more information about monitors, see .

## Import and create synthetic monitors in bulk using API

Create multiple synthetic monitors simultaneously by importing raw JSON or CSV files through the SyntheticsAsyncBulkCreate API.

### Before you begin

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

One of the following tools: Terminal \(with curl command\), Postman, or scripting environment.

### About this task

The SyntheticsAsyncBulkCreate API uses a two-step process:

1.  Creates a job ID by uploading your monitor data file.
2.  Checks job status to verify monitor creation status.

You can access this API through one of the following methods:

-   Terminal using curl commands
-   Postman application
-   Custom scripts

The API requires either a basic authentication or oauth token authentication.

-   Basic auth:

    ```
    `curl -u "username:password"`
    ```

-   OAuth token:

    ```
    `curl -H "Authorization: Bearer <your-oauth-token>"`
    ```


### Procedure

1.  Prepare your monitor data file in raw JSON or CSV format.

2.  Choose your preferred method \(Terminal, Postman, or Script\).

3.  Call the bulk import API endpoint to upload the file and generate a job ID.

4.  Use the status check URL to verify monitor creation status.

5.  Review the response for successful monitor creation or error details.

6.  Update the source file with correct data \(if there are errors\), and resubmit.


### Result

Monitors are created in the ServiceNow instance. The API response indicates:

-   Processing status \(processing/complete\)
-   Successfully created monitors
-   Failed monitors with error details \(required fields missing, invalid sys\_ids, and so forth\)

### Create monitors in bulk using Terminal

Use curl commands in Terminal to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the SyntheticsAsyncBulkCreate API.

#### Before you begin

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

#### About this task

The SyntheticsAsyncBulkCreate API uses a two-step process when accessed through Terminal. First, upload your monitor data file using a curl command to generate a job ID. Then, check the job status to verify monitor creation. The API processes records asynchronously and provides detailed feedback on successful creations and errors.

Different curl commands are required depending on whether you are uploading a JSON or CSV file.

#### Procedure

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


#### Result

Monitors are created in your ServiceNow instance. Successfully created monitors are immediately available for use. Failed monitors are reported with specific error details, allowing you to correct the data and resubmit.

#### Complete workflow example

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

#### What to do next

After successful creation, verify your monitors in the ServiceNow UI by navigating to **Synthetic Monitoring** &gt; **Monitors**. You can configure additional monitor settings and schedules, as needed.

### Create monitors in bulk using Postman

Use Postman to create multiple synthetic monitors simultaneously by importing JSON files through the SyntheticsAsyncBulkCreate API.

#### Before you begin

Role required: sn\_sow\_synthetics.synthetics\_admin or sn\_sow\_synthetics.synthetics\_editor

-   Valid ServiceNow instance credentials
-   Access to Http endpoint
-   Base URL: `https://<your-instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create`
-   Prepared raw JSON file with monitor data containing required fields:
    -   Monitor name
    -   HTTP endpoint sys\_id
    -   Parent service sys\_id
    -   Location sys\_id
    -   sys id of support group
    -   interval \(frequency\)
    -   Method \(\`GET\`, \`POST\`, \`PUT\`, \`DELETE\`, \`PATCH\`, \`HEAD\`\)
    -   Assertion field

#### About this task

The SyntheticsAsyncBulkCreate API uses a two-step process when accessed through Postman. First, create a POST request to upload your monitor data file and generate a job ID. Then, use the status check URL to verify monitor creation. Postman provides a user-friendly interface for testing the API and viewing formatted responses.

Only use Postman to import JSON files for this API. To import CSV files, [use Terminal instead](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/synth-monitor_dev-guide.md).

#### Procedure

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

    3.  Select the **Select File** button, and browse to your monitor data file location and select your JSON file.

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

    3.  Update your source JSON file to correct the identified issues.

        Common errors include:

        -   Missing required fields \(CMDB CI, location, method\)
        -   Invalid sys\_id references that don't exist in the instance
        -   Incorrect data formats or field names
    4.  Return to your original POST request and resubmit with the corrected file.


#### Result

Monitors are created in your ServiceNow instance. Successfully created monitors are immediately available for use. Failed monitors are reported with specific error details in a structured JSON format that is easy to review in Postman's response viewer.

#### Complete workflow example

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

#### What to do next

-   Save your Postman requests to a collection for future use and easy resubmission.
-   Verify your monitors in the ServiceNow UI by navigating to Synthetic Monitoring &gt; Monitors.
-   Configure additional monitor settings such as schedules, notifications, and thresholds as needed.

### JSON file format

The JSON file should contain an array of monitor objects, either directly or wrapped in a `checks` or `monitors` property.

#### Direct array

```json
[
  {
    "name": "API Health Check",
    "method": "GET",
    "cmdb_ci": "sys_id_of_http_endpoint",
    "interval": 5,
    "locations": ["location_sys_id_1"],
    "enabled": true,
    "parent_service_sys_id": "service_sys_id",
    "support_group_sys_id": "group_sys_id"
  }
]
```

#### Wrapped in object

```json
{
  "checks": [
    {
      "name": "API Health Check",
      "method": "GET",
      "cmdb_ci": "sys_id_of_http_endpoint",
      ...
    }
  ]
}
```

### CSV file format

CSV files must include a header row followed by data rows.

#### CSV header

```csv
name,method,description,interval,cmdb_ci,enabled,should_create_alert,alert_severity,locations,headers,alert_tags,valid_http_code_type,valid_http_code,max_latency_ms,query_string,credential,body,body_condition,parent_service_sys_id,support_group_sys_id
```

#### CSV example

```csv
name,method,description,interval,cmdb_ci,enabled,should_create_alert,alert_severity,locations,headers,alert_tags,valid_http_code_type,valid_http_code,max_latency_ms,query_string,credential,body,body_condition,parent_service_sys_id,support_group_sys_id
"My Monitor","GET","Health check",1,"0bd58579ff1232109a07ffffffffff72",true,true,1,"10eb9e1cffa2f2109a07ffffffffff27","[]","{}","equals","200","5000","","","","","81d847959f030200fe2ab0aec32e7031","2156c3a80b982300cac6c08393673a7e"
```

#### CSV special formatting

-   **locations**: Pipe-separated sys\_ids \(example, `loc1_sys_id|loc2_sys_id`\)
-   **headers**: JSON array string \(example, `[{"name":"Authorization","value":"Bearer xxx"}]`\)
-   **alert\_tags**: JSON object string \(example, `{"env":"prod","team":"api"}`\)
-   **body\_condition**: Colon-separated type:expression \(example, `jsonpath:$.status`\)
-   **Boolean values**: `true`, `false`, `1`, `0`, `yes`, `no`

### Example of bulk monitors using CSV file

This is an example of using a CSV file wrapped in a JSON object to create bulk monitors using terminal.

#### Step 1: Submit bulk job in CSV format

`curl -X POST "https://<instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create" \ -u "admin:password" \ -H "Content-Type: application/json" \ -H "Accept: application/json" \ -d @monitors.json`

#### Response

`{ "result": { "job_id": "a1b2c3d4e5f6...", "status": "pending", "total_count": 2, "message": "Bulk job accepted for processing" } }`

#### Step 2: Check the job status

`curl -X GET "https://<instance>.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/{job_id}" \ -u "admin:password" \ -H "Accept: application/json"`

#### Response

`{ "result": { "job_id": "a1b2c3d4e5f6...", "status": "completed", "total_count": 2, "success_count": 2, "error_count": 0, "processed_count": 2 } }`

