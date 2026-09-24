---
title: Check scan status and retrieve findings
description: After triggering a scan, poll the status endpoint to monitor progress and retrieve findings when the scan completes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/check-scan-status-retrieve-findings.html
release: brazil
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [scan status, findings, API, GET]
breadcrumb: [Scan Engine Headless REST API, Scan your instance, Impact Guided Setup, Configuring Impact, Impact]
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

    For complete field descriptions, see [Scan Engine API field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/finding-resolved-finding-fields.md).

3.  Set up polling intervals.

    Most scans complete in seconds. Use a smart polling strategy to avoid unnecessary requests:

    -   Begin with 5-second intervals for scans expected to complete quickly.
    -   Increase the interval to 30 seconds if the scan continues beyond the initial polling attempts.
    -   Cease polling when the status reaches `Complete`.
4.  Retrieve findings once the scan is complete.

    When the status shows `Complete`, fetch the findings endpoint:

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

For common usage patterns, integrate the scan results into your Continuous Integration/Continuous Deployment \(CI/CD\) pipelines or scheduled workflows. See [Automate scans in CI/CD pipelines and scheduled workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/integrate-scan-engine-ci-cd.md) for examples.

**Parent Topic:**[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)

