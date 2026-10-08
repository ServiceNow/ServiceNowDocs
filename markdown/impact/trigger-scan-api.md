---
title: Trigger a scan via API
description: You can start a Scan Engine scan by sending a POST request to the scan endpoint. The API returns a unique scan result ID that you use to check progress and retrieve findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/trigger-scan-api.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 5
keywords: [scan, API, POST, trigger]
breadcrumb: [Scan Engine Headless REST API, Scan your instance, Configuring Impact, Impact]
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

    |Scan mode|Description|
    |---------|-----------|
    |`instance`|Full or delta instance scan against all applicable definitions.|
    |`update_set`|Scans one or more update sets before promotion to production.|
    |`application`|Scans one or more applications with per-application concurrency.|
    |`content`|Scans raw ServiceNow XML records in-memory, without persisting them.|

    **Note:** Each mode also accepts a suffixed spelling, such as `instance_scan`, `update_set_scan`, `application_scan`, and `content_scan`. These remain permanently supported for backward compatibility. The response always echoes the canonical unsuffixed mode name.

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

    **Instance scan \(delta or full\)**

    ```
    {
      "scan_mode": "instance",
      "trigger_channel": "api",
      "instance_scan_type": "delta"
    }
    ```

    |Field|Default|Description|
    |-----|-------|-----------|
    |`instance_scan_type`|`delta`|Type of instance scan to run. Allowed values: `full` or `delta`.|

    **Update set scan**

    ```
    {
      "scan_mode": "update_set",
      "trigger_channel": "api",
      "update_set_sys_ids": ["<32-char sys_id>", "..."]
    }
    ```

    |Field|Default|Description|
    |-----|-------|-----------|
    |`update_set_sys_ids`|Required|Array of sys\_ids to scan \(not update set numbers\). Must be a JSON array — sending a single sys\_id as a bare string is rejected with 400 INVALID\_FIELD\_VALUE.|

    Optional fields for update set scans:

    |Field|Default|Description|
    |-----|-------|-----------|
    |`remote`|`false`|Scans a `sys_remote_update_set` instead of a local update set.|
    |`is_batch`|`false`|By default, child and nested update sets are scanned along with the ones you specify. Set to `true` to scan only the exact update sets listed.|

    **Application scan**

    ```
    {
      "scan_mode": "application",
      "trigger_channel": "api",
      "application_sys_ids": ["<32-char sys_id>", "..."]
    }
    ```

    |Field|Default|Description|
    |-----|-------|-----------|
    |`application_sys_ids`|Required|Array of application sys\_ids to scan. The API natively supports multiple applications in one request. Must be a JSON array — sending a single sys\_id as a bare string is rejected with 400 INVALID\_FIELD\_VALUE.|

    **Content scan \(XML payload\)**

    ```
    {
      "scan_mode": "content",
      "trigger_channel": "api",
      "xml_content": "<record_update table=\"sys_script_include\">...</record_update>"
    }
    ```

    |Field|Default|Description|
    |-----|-------|-----------|
    |`xml_content`|Required|A single well-formed `<record_update>` XML document.|
    |`trigger_channel`|`api`|Recommended field for new integrations. The `source` field continues to work, but `trigger_channel` is the name to standardize on. If you send both fields with conflicting values, the API returns 400 INVALID\_FIELD\_VALUE.|

    **Warning:** The maximum payload size is 64KB per request.

5.  Send the request and capture the scan result ID.

    On success, the API returns a response with a `scan_result_sys_id`:

    ```
    {
      "result": {
        "scan_result_sys_id": "45ec57e5ffc743109124ffffffffffda",
        "status": "Getting Ready",
        "scan_mode": "instance"
      }
    }
    ```

    |Scan mode|HTTP status|Description|
    |---------|-----------|-----------|
    |`instance`, `update_set`, `application`|202 Accepted|The scan is queued and not run synchronously. Poll `scan_status` for the result.|
    |`content`|200 OK|The scan runs in-memory and returns the result directly.|

    Save the `scan_result_sys_id` to check scan status and retrieve findings later.

6.  Handle any errors.

    If the request fails, the API returns an error code and details. Common errors:

    |Error code|What it means|
    |----------|-------------|
    |MISSING\_REQUIRED\_FIELD \(400\)|A required field is missing from your request.|
    |INVALID\_SCAN\_MODE \(400\)|The `scan_mode` value is not recognized.|
    |NOT\_AUTHORIZED \(403\)|Your user account is missing the `sn_se.scan_engine_user` role.|
    |CONCURRENT\_SCAN\_RUNNING \(409\)|Another scan is already running for this target.|
    |NO\_ELIGIBLE\_DEFINITIONS \(409\)|A content scan found no scan definitions on the instance applicable to the submitted XML. Distinguishes **nothing could run** from a clean scan that found nothing.|
    |PAYLOAD\_TOO\_LARGE \(413\)|Request body exceeds 64KB. Reduce the request size.|

    See [Scan Engine API error codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/api-error-codes-grouped.md) for the full error code reference.

7.  Cancel a scan if it is no longer needed.

    If a scan is running, but no longer needed, you can cancel it. Send a POST request to the cancel endpoint:

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

    |Outcome|HTTP status and meaning|
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

