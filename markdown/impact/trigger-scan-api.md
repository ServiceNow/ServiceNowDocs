---
title: Trigger a scan via API
description: You can start a Scan Engine scan by sending a POST request to the scan endpoint. The API returns a unique scan result ID that you use to check progress and retrieve findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/trigger-scan-api.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [scan, API, POST, trigger]
breadcrumb: [Scan Engine Headless REST API, Scan your instance, Impact Guided Setup, Configuring Impact, Impact]
---

# Trigger a scan via API

You can start a Scan Engine scan by sending a POST request to the scan endpoint. The API returns a unique scan result ID that you use to check progress and retrieve findings.

## Before you begin

Role required: sn\_se.scan\_engine\_user

## About this task

## Procedure

1.  Set up your authentication credentials.

    Prepare your session token or OAuth bearer token. You will include this in the `Authorization` header of your request. See [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-oauth-auth-method.md) for details.

2.  Determine the scan mode for your use case.

    Choose the type of scan to run. The Scan Engine API supports four scan modes:

    |Scan Mode|Description|
    |---------|-----------|
    |`instance_scan`|Full or delta instance scan against all applicable definitions.|
    |`update_set`|Scans one or more update sets before promotion to production.|
    |`application_scan`|Scans one or more applications with per-application concurrency.|
    |`content`|Scans raw ServiceNow XML records in-memory, without persisting them.|

3.  Compose your POST request to the scan endpoint.

    Send your request to:

    ```
    POST https://<instance>.service-now.com/api/sn_se/v1/scan_operations/scan
    ```

    Replace `<instance>` with your ServiceNow instance name. Always include `/v1/` in the URL—there is no default version.

4.  Add required headers and the request body.

    Include these headers:

    -   `Authorization: Bearer <your_token>`
    -   `Content-Type: application/json`
    Send a JSON body matching your chosen scan mode.

    **Instance Scan \(delta or full\)**

    ```
    {
      "scan_mode": "instance_scan",
      "source": "api",
      "instance_scan_type": "delta"
    }
    ```

    `instance_scan_type` is optional \(default: `"delta"`\). Allowed values: `"full"` or `"delta"`.

    **Update Set Scan**

    ```
    {
      "scan_mode": "update_set",
      "source": "api",
      "update_set_sys_ids": ["<32-char sys_id>", "..."]
    }
    ```

    `update_set_sys_ids` is a required array of sys\_ids \(not update set numbers\).

    **Application Scan**

    ```
    {
      "scan_mode": "application_scan",
      "source": "api",
      "application_sys_ids": ["<32-char sys_id>", "..."]
    }
    ```

    `application_sys_ids` is a required array of sys\_ids. The API natively supports multiple applications in one request.

    **Content Scan \(XML payload\)**

    ```
    {
      "scan_mode": "content",
      "source": "api",
      "xml_content": "<record_update table=\"sys_script_include\">...</record_update>"
    }
    ```

    `xml_content` is a required single well-formed `<record_update>` XML document.

    **Important:** The maximum payload size is 64KB per request. Use ISO 8601 date format \(`YYYY-MM-DDTHH:mm:ssZ`\) for any date fields.

5.  Send the request and capture the scan result ID.

    On success, the API returns a response with a `scan_result_sys_id`:

    ```
    {
      "result": {
        "scan_result_sys_id": "45ec57e5ffc743109124ffffffffffda",
        "status": "Getting Ready",
        "scan_mode": "instance_scan"
      }
    }
    ```

    Save the `scan_result_sys_id`—you need it to check scan status and retrieve findings later.

6.  Handle any errors.

    If the request fails, the API returns an error code and details. See [Scan Engine API error codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/api-error-codes-grouped.md) for common errors and suggested troubleshooting steps.

7.  Cancel a scan if it is no longer needed.

    If a scan is running but no longer needed, you can cancel it. Send a POST request to the cancel endpoint:

    ```
    POST https://<instance>.service-now.com/api/sn_se/v1/scan_operations/cancel
    ```

    **Request body:**

    ```
    {
      "scan_sys_id": "45ec57e5ffc743109124ffffffffffda"
    }
    ```

    Provide either `scan_sys_id` \(the sys\_id of the scan result\) or `scan_number` \(the scan result number\). Both are optional; if neither is supplied, the API targets the most recently created scan in an active state.

    |Outcome|HTTP Status and Meaning|
    |-------|-----------------------|
    |immediate|HTTP 200 — The scan was in getting\_ready or no batch was running. Cancelled synchronously. Status is now Cancelled.|
    |graceful|HTTP 202 — A batch was actively running. Cancel requested. The scan will finalize to Cancelled once the batch completes.|
    |no\_action|HTTP 200 — The scan completed naturally between the request and applying it. No cancellation needed.|
    |event\_queue|HTTP 200 — No active scan, but a pending queued scan event was found and voided.|

    **Tip:** Graceful cancellation waits for the current batch to complete before stopping. If you need to cancel immediately, issue the request while the scan is still in getting\_ready state.


## Result

A scan is now running on your target. The API returned a scan result ID that you can use to track progress. Proceed to check scan status and retrieve findings once the scan completes. You can cancel the scan at any time if it is no longer needed.

## What to do next

After triggering a scan, monitor its progress by polling the status endpoint. See [Check scan status and retrieve findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/check-scan-status-retrieve-findings.md) for details.

**Parent Topic:**[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)

