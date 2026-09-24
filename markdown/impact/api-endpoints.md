---
title: Scan Engine API endpoints
description: Reference information for Scan Engine Headless API endpoints, authentication requirements, and response formats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/api-endpoints.html
release: brazil
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 6
keywords: [API, endpoints, error codes, HTTP status]
breadcrumb: [Scan Engine reference, Impact reference, Impact]
---

# Scan Engine API endpoints

Reference information for Scan Engine Headless API endpoints, authentication requirements, and response formats.

## Base URL and versioning

Scan Engine API requests use this base URL:

```
https://<instance>.service-now.com/api/sn_se/v1/scan_operations/
```

Always include `/v1/` in your requests—there is no default version.

**Important:** Replace `<instance>` with your ServiceNow instance name.

## Authentication and required headers

All API requests require these headers:

|Header|Value|Required|
|------|-----|--------|
|`Authorization`|`Bearer <session_token_or_oauth_token>`|Yes|
|`Content-Type`|`application/json`|Yes, for write endpoints \(POST\)|

All requests require the `sn_se.scan_engine_user` role. Requests without valid credentials return `401`.

## Request limits and format requirements

All API request size limits and format requirements.

|Limit|Value|
|-----|-----|
|Maximum payload size|64 KB per request|
|Date format|ISO 8601 \(YYYY-MM-DDTHH:mm:ssZ\)|
|Content-Type for write endpoints|`application/json`|

## API endpoints

The Scan Engine API provides five endpoints for triggering scans, checking status, retrieving findings, and canceling scans.

|Endpoint|Method|Purpose|
|--------|------|-------|
|`/scan`|POST|Trigger a new scan. Returns a `scan_result_sys_id` for tracking.|
|`/scan_status`|GET|Check the progress of a running scan. Pass `scan_result_sys_id` as a query parameter.|
|`/findings`|GET|Retrieve findings for a completed scan. Pass `scan_result_sys_id` as a query parameter.|
|`/resolved_findings`|GET|Retrieve findings that have been resolved or fixed over time. Supports filtering by date, definition, and scope.|
|`/cancel`|POST|Cancel a running scan. Pass `scan_number` or `scan_sys_id` in the request body.|

## Scan modes and parameters

When triggering a scan via the `/scan` endpoint, use one of these modes in your request body:

|Mode|Description|
|----|-----------|
|`instance_scan`|Full or delta instance scan against all applicable definitions. Include `instance_scan_type` to specify full or delta.|
|`update_set`|Scans one or more update sets before promotion to production. Include `update_set_sys_ids` array with sys\_ids \(not update set numbers\).|
|`application_scan`|Scans one or more applications with per-application concurrency. Include `application_sys_ids` array of sys\_ids.|
|`content`|Scans raw ServiceNow XML records in-memory, without persisting them. Include `xml_content` with well-formed record\_update XML.|

## Error codes

This table lists all error codes returned by the Scan Engine API, their HTTP status, applicable endpoints, and troubleshooting guidance.

|Error Code|HTTP Status|Applies to endpoints|Description|
|----------|-----------|--------------------|-----------|
|MISSING\_REQUIRED\_FIELD|400|All endpoints|A required field is missing from your request. Check the error message to identify which field is required.|
|INVALID\_SCAN\_MODE|400|POST /scan|The `scan_mode` value is not recognized. Verify it matches one of the supported modes: `instance_scan`, `update_set`, `application_scan`, or `content`.|
|INVALID\_FIELD\_VALUE|400|POST /scan, POST /cancel, GET /findings, GET /resolved\_findings|A field value does not match the expected format or type. Check the error detail for which field needs correction.|
|INVALID\_UPDATE\_SET|400|POST /scan \(update\_set mode\)|The supplied update set sys\_id does not exist or is invalid. Verify the sys\_id matches a valid update set record.|
|INVALID\_XML\_CONTENT|400|POST /scan \(content mode\)|The XML content is not well-formed or is missing the `<record_update>` root element. Validate the XML structure.|
|INVALID\_APPLICATION|400|POST /scan \(application\_scan mode\)|The supplied application sys\_id does not exist or is invalid. Verify the sys\_id matches a valid application record.|
|DEFINITION\_NOT\_FOUND|400|GET /findings|The scan definition specified in your query does not exist. Verify the definition sys\_id or number.|
|PAYLOAD\_TOO\_LARGE|413|POST /scan, POST /cancel|Request body exceeds 64KB. Reduce the request size by using smaller batches or fewer records.|
|NOT\_AUTHENTICATED|401|All endpoints|Your session token or OAuth credentials are invalid, expired, or missing. Re-authenticate and retry with valid credentials.|
|NOT\_AUTHORIZED|403|All endpoints|Your user account does not have the `sn_se.scan_engine_user` role. Contact your administrator to request access.|
|SCAN\_NOT\_FOUND|404|GET /scan\_status, GET /findings, GET /resolved\_findings, POST /cancel|The scan result ID provided does not exist or has been purged. Verify the scan\_result\_sys\_id or scan\_number is correct.|
|APPLICATION\_SCAN\_NOT\_FOUND|404|GET /findings|No findings exist for the specified application scan. The scan may not have completed or the application ID may be incorrect.|
|UPDATE\_SET\_SCAN\_NOT\_FOUND|404|GET /findings|No findings exist for the specified update set scan. The scan may not have completed or the update set ID may be incorrect.|
|INSTANCE\_SCAN\_NOT\_FOUND|404|GET /findings|No findings exist for the specified instance scan. The scan may not have completed or the scan result may have been purged.|
|NO\_ACTIVE\_SCAN|404|POST /cancel|No active scan is running and no identifier was provided. Supply either `scan_sys_id` or `scan_number`, or verify a scan is currently active.|
|CONCURRENT\_SCAN\_RUNNING|409|POST /scan|Another scan is already running for this target. Wait at least 30 seconds and retry, or cancel the existing scan first.|
|ALREADY\_CANCELLED|409|POST /cancel|The scan is already in a Cancelled state. No further cancellation is needed or possible.|
|SCAN\_COMPLETE|409|POST /cancel|The scan has already completed and cannot be cancelled. Cancellation is only available for in-progress or queued scans.|

## Error handling strategies

When integrating the Scan Engine API into your automation, implement these strategies for common errors:

|Error Type|Strategy|
|----------|--------|
|Rate limiting \(409 CONCURRENT\_SCAN\_RUNNING\)|Implement exponential back off. Start with a 30-second wait, then increase on subsequent retries.|
|Authentication \(401 NOT\_AUTHENTICATED\)|Refresh your credentials and retry immediately. Log the error for audit purposes.|
|Authorization \(403 NOT\_AUTHORIZED\)|This is a configuration issue. Contact your administrator to grant the required role. don't retry automatically.|
|Server errors \(500\)|Implement exponential backoff with a maximum retry count. Log the error and alert your operations team if retries are exhausted.|
|Validation errors \(400\)|These indicate a problem with your request. Review the error message and correct the field or value before retrying.|

## Response formats

The API uses consistent response structures. All successful responses include a `result` object. All error responses include an `error` object.

Success response

```
{
  "result": {
    "scan_result_sys_id": "a1b2c3d4e5f6g7h8",
    "status": "Complete",
    "total_errors": 5,
    "total_warnings": 12,
    "se_score": 72
  }
}
```

The `result` object contains:

-   `scan_result_sys_id`: Unique identifier for this scan. Use it to check status and retrieve findings.
-   `status`: Current scan state—`Waiting`, `Getting Ready`, `Complete`, or other terminal states.
-   `total_errors`: Count of violations classified as errors.
-   `total_warnings`: Count of violations classified as warnings.
-   `se_score`: Overall health score on a 0–100 scale.

Error response

```
{
  "error": {
    "code": "MISSING_REQUIRED_FIELD",
    "message": "A required field is missing",
    "detail": {
      "fields": ["scan_mode", "source"]
    }
  },
  "status": "failure"
}
```

The `error` object contains:

-   `code`: Machine-readable error code. Use this for programmatic error handling.
-   `message`: Human-readable description of the error.
-   `detail`: Additional context such as which fields are missing.

Findings response

```
{
  "result": {
    "findings": [
      {
        "severity": "error",
        "message": "Missing mandatory field",
        "affected_record": "cmdb_ci_00001"
      }
    ],
    "definitions": [ ... ],
    "pagination": {
      "limit": 100,
      "offset": 0,
      "has_more": false,
      "total": 17
    }
  }
}
```

The findings response includes:

-   `findings[]`: Array of violations found during the scan. Each finding includes severity, message, and affected\_record.
-   `definitions[]`: Deduplicated rule metadata for all findings in the response.
-   `pagination`: Offset-based pagination info. Default 100 results per page, max 1,000.

For a complete list of fields returned in finding and resolved finding responses, see [Scan Engine API field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/finding-resolved-finding-fields.md).

## Common query parameters

These query parameters are used across multiple Scan Engine API endpoints to identify scans, paginate results, and filter findings by definition or resolution date.

|Parameter|Used in|Description|
|---------|-------|-----------|
|`scan_result_sys_id`|`/scan_status`, `/findings`, `/resolved_findings`|The unique identifier returned when you triggered the scan. Required for status and current findings queries.|
|`offset`|`/findings`, `/resolved_findings`|Number of results to skip before returning results. Used for pagination. Defaults to 0.|
|`limit`|`/findings`, `/resolved_findings`|Number of results to return per page. Defaults to 100, maximum 1,000.|
|`definition`|`/resolved_findings`|Filter by definition sys\_id or number. Optional.|
|`resolved_on_from`|`/resolved_findings`|Filter findings resolved on or after this date. Use ISO 8601 format YYYY-MM-DD. Optional.|
|`resolved_on_to`|`/resolved_findings`|Filter findings resolved on or before this date. Use ISO 8601 format YYYY-MM-DD. Optional.|

**Parent Topic:**[Scan Engine reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-reference.md)

