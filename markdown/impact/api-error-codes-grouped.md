---
title: Scan Engine API error codes
description: Error codes returned by the Scan Engine API, organized by HTTP status code. Each section includes proposed solutions and handling strategies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/api-error-codes-grouped.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [API, error codes, HTTP status, troubleshooting]
breadcrumb: [Scan Engine reference, Impact reference, Impact]
---

# Scan Engine API error codes

Error codes returned by the Scan Engine API, organized by HTTP status code. Each section includes proposed solutions and handling strategies.

## 400 Bad Request errors

Validation errors indicate a problem with your request. Review the error message and correct the field or value before retrying.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|DEFINITION\_NOT\_FOUND|GET /findings|The scan definition specified in your query does not exist. Verify the definition sys\_id or number.|
|INVALID\_APPLICATION|POST /scan \(application\_scan mode\)|The supplied application sys\_id does not exist or is invalid. Verify the sys\_id matches a valid application record.|
|INVALID\_FIELD\_VALUE|POST /scan, POST /cancel, GET /findings, GET /resolved\_findings|A field value does not match the expected format or type. Check the error detail for which field needs correction.|
|INVALID\_SCAN\_MODE|POST /scan|The `scan_mode` value is not recognized. Verify it matches one of the supported modes: `instance_scan`, `update_set`, `application_scan`, or `content`.|
|INVALID\_UPDATE\_SET|POST /scan \(update\_set mode\)|The supplied update set sys\_id does not exist or is invalid. Verify the sys\_id matches a valid application record.|
|INVALID\_XML\_CONTENT|POST /scan \(content mode\)|The XML content is not well-formed or is missing the `<record_update>` root element. Validate the XML structure.|
|MISSING\_REQUIRED\_FIELD|All endpoints|A required field is missing from your request. Check the error message to identify which field is required.|

## 401 Unauthorized errors

Authentication errors occur when credentials are invalid. Refresh your credentials and retry immediately. Log the error for audit purposes.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|NOT\_AUTHENTICATED|All endpoints|Your session token or OAuth credentials are invalid, expired, or missing. Re-authenticate and retry with valid credentials.|

## 403 Forbidden errors

Authorization errors are configuration issues. Contact your administrator to grant the required role. don't retry automatically.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|NOT\_AUTHORIZED|All endpoints|Your user account does not have the `sn_se.scan_engine_user` role. Contact your administrator to request access.|

## 404 Not Found errors

Resource not found errors occur when the requested scan or resource does not exist. Verify identifiers are correct and the resource has not been purged.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|APPLICATION\_SCAN\_NOT\_FOUND|GET /findings|No findings exist for the specified application scan. The scan may not have completed or the application ID may be incorrect.|
|INSTANCE\_SCAN\_NOT\_FOUND|GET /findings|No findings exist for the specified instance scan. The scan may not have completed or the scan result may have been purged.|
|NO\_ACTIVE\_SCAN|POST /cancel|No active scan is running and no identifier was provided. Supply either `scan_sys_id` or `scan_number`, or verify a scan is currently active.|
|SCAN\_NOT\_FOUND|GET /scan\_status, GET /findings, GET /resolved\_findings, POST /cancel|The scan result ID provided does not exist or has been purged. Verify the scan\_result\_sys\_id or scan\_number is correct.|
|UPDATE\_SET\_SCAN\_NOT\_FOUND|GET /findings|No findings exist for the specified update set scan. The scan may not have completed or the update set ID may be incorrect.|

## 409 Conflict errors

Conflict errors occur when a request can't be completed due to the current state. For rate limiting \(CONCURRENT\_SCAN\_RUNNING\), implement exponential backoff starting with a 30-second wait, then increase on subsequent retries.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|ALREADY\_CANCELLED|POST /cancel|The scan is already in a Cancelled state. No further cancellation is needed or possible.|
|CONCURRENT\_SCAN\_RUNNING|POST /scan|Another scan is already running for this target. Wait at least 30 seconds and retry, or cancel the existing scan first.|
|SCAN\_COMPLETE|POST /cancel|The scan has already completed and cannot be cancelled. Cancellation is only available for in-progress or queued scans.|

## 413 Payload Too Large errors

Payload size errors occur when the request body exceeds limits. Reduce the request size by using smaller batches or fewer records.

|Error Code|Applies to endpoints|Description|
|----------|--------------------|-----------|
|PAYLOAD\_TOO\_LARGE|POST /scan, POST /cancel|Request body exceeds 64KB. Reduce the request size by using smaller batches or fewer records.|

**Parent Topic:**[Scan Engine reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-reference.md)

