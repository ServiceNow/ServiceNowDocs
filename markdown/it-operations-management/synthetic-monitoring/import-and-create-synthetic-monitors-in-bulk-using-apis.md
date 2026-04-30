---
title: Import and create synthetic monitors in bulk using API
description: Create multiple synthetic monitors simultaneously by importing raw JSON or CSV files through the Bulk Monitor Creation API.
locale: en-US
release: zurich
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Import and create synthetic monitors in bulk using API

Create multiple synthetic monitors simultaneously by importing raw JSON or CSV files through the Bulk Monitor Creation API.

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

One of the following tools: Terminal \(with curl command\), Postman, or scripting environment.

## About this task

The Bulk Monitor Creation API uses a two-step process:

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


## Procedure

1.  Prepare your monitor data file in raw JSON or CSV format.

2.  Choose your preferred method \(Terminal, Postman, or Script\).

3.  Call the bulk import API endpoint to upload the file and generate a job ID.

4.  Use the status check URL to verify monitor creation status.

5.  Review the response for successful monitor creation or error details.

6.  Update the source file with correct data \(if there are errors\), and resubmit.


## Result

Monitors are created in the ServiceNow instance. The API response indicates:

-   Processing status \(processing/complete\)
-   Successfully created monitors
-   Failed monitors with error details \(required fields missing, invalid sys\_ids, and so forth\)

-   **[Create monitors in bulk using Postman](bulk_monitor_creation_postman.md)**  
Use Postman to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.
-   **[Create monitors in bulk using Terminal](bulk_monitor_creation_terminal.md)**  
Use curl commands in Terminal to create multiple synthetic monitors simultaneously by importing JSON or CSV files through the Bulk Monitor Creation API.

**Parent Topic:**[Configuring synthetic monitoring](../concept/configuring-synthetic-monitoring.md)

