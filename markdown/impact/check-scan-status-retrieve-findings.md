---
title: Check scan status and retrieve findings
description: After triggering a scan, poll the status endpoint to monitor progress and retrieve findings when the scan completes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/check-scan-status-retrieve-findings.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 4
keywords: [scan status, findings, API, GET]
breadcrumb: [Scan Engine Headless REST API, Scan your instance, Configuring Impact, Impact]
---

# Check scan status and retrieve findings

After triggering a scan, poll the status endpoint to monitor progress and retrieve findings when the scan completes.

## Before you begin

Role required: sn\_se.scan\_engine\_user

## About this task

After you trigger a scan, poll the status endpoint to see whether it's complete, then retrieve the findings once the scan finishes. Findings show the specific violations discovered during your scan.

## Procedure

1.  Check the scan status.

    Send a GET request to the status endpoint, passing the scan result ID you received when you triggered the scan:

    ```
    GET https://<instance>.service-now.com/api/sn_se/v1/scan_operations/scan_status?scan_result_sys_id=a1b2c3d4e5f6g7h8
    ```

    Include the `Authorization` header with your session token or OAuth bearer token.

2.  Interpret the status response.

    The API returns scan progress information:

    ```
    {
      "result": {
        "scan_result_sys_id": "a1b2c3d4e5f6g7h8",
        "number": "SCAN0001234",
        "scan_type": "delta_instance_scan",
        "status": "Complete",
        "source": "myinstance.service-now.com",
        "trigger_channel": "API",
        "progress_percent": "100",
        "start_time": "2026-08-31 10:00:00",
        "end_time": "2026-08-31 10:05:00",
        "total_batches": "1",
        "batches_complete": "1",
        "summary": {
          "total_findings": "17",
          "total_errors": "5",
          "total_warnings": "12",
          "se_score": "72",
          "total_impact_to_instance": "50",
          "total_technical_debt": "2 Days 4 Hours",
          "definitions_scanned_for": "210"
        }
      }
    }
    ```

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`scan_result_sys_id`

</td><td>

Unique sys\_id of the scan result record.

</td></tr><tr><td>

`number`

</td><td>

Scan result number, for example, SCAN0001234.

</td></tr><tr><td>

`scan_type`

</td><td>

The classification recorded on the scan result record. Possible values: -   `full_instance_scan`
-   `delta_instance_scan`
-   `on_demand_instance_scan`
-   `application_scan`
-   `update_set_scan`
-   `push_commit_scan`
**Note:** This is a separate field from the `scan_mode` You send in the request and use its own value list. For example, a request with `scan_mode: application` is recorded as `application_scan`.

</td></tr><tr><td>

`status`

</td><td>

Current scan state. Keep polling while status is not a terminal state. -   `Waiting`
-   `Getting Ready`
-   `Scanning`
-   `Complete`
-   `complete_with_errors`
-   `Cancelled`
-   `Cancellation Requested`
-   `No Action Taken`
-   `Queued Scan Cancelled`


</td></tr><tr><td>

`source`

</td><td>

The originating ServiceNow instance name, or null if not applicable.

</td></tr><tr><td>

`trigger_channel`

</td><td>

The declared request channel, either API, UI, or Scheduled, captured from the request at trigger time. Use this to determine whether a scan was triggered via the API.

</td></tr><tr><td>

`progress_percent`

</td><td>

Scan progress percentage \(0–100\).

</td></tr><tr><td>

`start_time`

</td><td>

Scan start timestamp \(YYYY-MM-DD HH:MM:SS\).

</td></tr><tr><td>

`end_time`

</td><td>

Scan end timestamp \(YYYY-MM-DD HH:MM:SS\), or null if still running.

</td></tr><tr><td>

`total_batches`

</td><td>

Total number of batches the scan is divided into.

</td></tr><tr><td>

`batches_complete`

</td><td>

Number of batches that have finished processing.

</td></tr><tr><td>

`summary`

</td><td>

Available only when `status` is `Complete`. Contains the fields listed below.

</td></tr><tr><td>

`summary.total_findings`

</td><td>

Total count of findings from the scan.

</td></tr><tr><td>

`summary.total_errors`

</td><td>

Count of findings classified as errors.

</td></tr><tr><td>

`summary.total_warnings`

</td><td>

Count of findings classified as warnings.

</td></tr><tr><td>

`summary.se_score`

</td><td>

Overall health score on a 0–100 scale. Higher scores indicate healthier targets.

</td></tr><tr><td>

`summary.total_impact_to_instance`

</td><td>

Sum of the impact to instance score across all findings.

</td></tr><tr><td>

`summary.total_technical_debt`

</td><td>

Estimated total technical debt across all findings, expressed as days and hours.

</td></tr><tr><td>

`summary.definitions_scanned_for`

</td><td>

Count of scan definition inspections performed.

</td></tr></tbody>
</table>3.  Set up polling intervals.

    Most scans complete in seconds. Use a smart polling strategy to avoid unnecessary requests:

    -   Begin with 5-second intervals for scans expected to complete quickly.
    -   Increase the interval to 30 seconds if the scan continues beyond the initial polling attempts.
    -   Cease polling when the status reaches a terminal state, such as `Complete`, `Cancelled`, `No Action Taken`, or `Queued Scan Cancelled`.
4.  Retrieve findings once the scan is complete.

    When the status shows a terminal state, fetch the findings endpoint:

    ```
    GET https://<instance>.service-now.com/api/sn_se/v1/scan_operations/findings?scan_result_sys_id=a1b2c3d4e5f6g7h8
    ```

    Include your `Authorization` header with valid credentials.

5.  Process the findings response.

    The API returns findings, sideloaded definition metadata, and pagination information:

    ```
    {
      "result": {
        "findings": [ { ... } ],
        "definitions": { ... },
        "pagination": {
          "limit": 100,
          "offset": 0,
          "has_more": false,
          "total": 17
        }
      }
    }
    ```

    For complete field descriptions, see [Scan Engine API field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/finding-resolved-finding-fields.md).

6.  Handle pagination for large result sets.

    When a scan returns more than 100 findings, the API implements offset and limit based pagination. The default page size is 100 results, with a maximum of 1,000 results per page. Reference the pagination metadata to retrieve subsequent pages:

    ```
    GET https://<instance>.service-now.com/api/sn_se/v1/scan_operations/findings?scan_result_sys_id=<your_scan_result_sys_id>&offset=100&limit=100
    ```

    Use the offset parameter to skip findings already retrieved. The limit parameter controls how many results return per page.

7.  Act on the findings in your workflow.

    Use the findings to make decisions in your automation:

    -   If `total_errors` is greater than zero, fail your CI/CD build or alert your team.
    -   If `se_score` is below your threshold, trigger a remediation workflow.
    -   Store findings in your audit trail or reporting system for tracking over time.
8.  Retrieve resolved findings to track improvements over time.

    Query for findings that have been resolved or fixed over time. These are queried from a separate resolved findings history table, not tied to a specific scan result.

    **Send a GET request to retrieve resolved findings:**

    ```
    GET https://<instance>.service-now.com/api/sn_se/v1/scan_operations/resolved_findings?definition=sn_SE10189
    ```

    For complete query parameter and field descriptions, see [Scan Engine API field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/finding-resolved-finding-fields.md).

    **Tip:** Use resolved findings to measure improvements in your instance health over time and identify which scan definitions have the highest resolution rates.


## Result

You now have detailed findings from your scan and can track resolved findings over time. Use findings to guide your next actions, such as blocking a deployment, starting a fix workflow, logging results to your audit system, or measuring long-term improvements.

## What to do next

For common usage patterns, integrate the scan results into your CI/CD pipelines or scheduled workflows. See [Automate scans in CI/CD pipelines and scheduled workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/integrate-scan-engine-ci-cd.md) for examples.

**Parent Topic:**[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)

