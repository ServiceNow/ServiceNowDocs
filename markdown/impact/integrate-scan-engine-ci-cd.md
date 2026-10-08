---
title: Automate scans in CI/CD pipelines and scheduled workflows
description: Use the Scan Engine API to automate scans in Continuous Integration/Continuous Deployment \(CI/CD\) pipelines and scheduled jobs, enabling you to block risky changes or monitor instance health programmatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/integrate-scan-engine-ci-cd.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 4
keywords: [CI/CD, integration, pipeline, scheduled, automation]
breadcrumb: [Scan Engine Headless REST API, Scan your instance, Configuring Impact, Impact]
---

# Automate scans in CI/CD pipelines and scheduled workflows

Use the Scan Engine API to automate scans in Continuous Integration/Continuous Deployment \(CI/CD\) pipelines and scheduled jobs, enabling you to block risky changes or monitor instance health programmatically.

## Before you begin

Role required: sn\_se.scan\_engine\_user

## About this task

You can embed Scan Engine into your deployment pipeline to block risky changes or run nightly health checks on your instance. Both patterns use the same API calls but differ in timing and scope.

## Procedure

1.  Choose your integration pattern.

    Select the approach that matches your goal:

    -   CI/CD gate: Scan each update set before it moves to production. Fail the build if critical violations are found.
    -   Scheduled health check: Run a nightly instance scan to track system health over time and alert if health drops below your threshold.
2.  Set up CI/CD gating.

    To block deployments based on scan findings:

    1.  In your CI/CD pipeline, after your code is packaged but before promotion, trigger an `update_set` scan via the API, passing the update set sys\_id.
    2.  Poll the status endpoint until the scan completes.
    3.  Read `.result.summary.total_errors` from the status response once the status is `Complete`.
    4.  If `total_errors` is greater than zero, fail the build step and notify your team. Otherwise, proceed with promotion.
    **Note:** Read `total_errors` from `/scan_status` once the scan is complete, not from the `/findings` endpoint.

    **Example pipeline script:**

    ```
    #!/bin/bash
    # Trigger the scan
    RESPONSE=$(curl -X POST https://instance.service-now.com/api/sn_se/v1/scan_operations/scan \
      -H "Authorization: Bearer $TOKEN" \
      -H "Content-Type: application/json" \
      -d '{"scan_mode": "update_set", "trigger_channel": "api", "update_set_sys_ids": ["<32-char sys_id>"]}')
    
    SCAN_ID=$(echo $RESPONSE | jq -r '.result.scan_result_sys_id')
    
    # Poll until complete
    while true; do
      STATUS=$(curl -s https://instance.service-now.com/api/sn_se/v1/scan_operations/scan_status?scan_result_sys_id=$SCAN_ID \
        -H "Authorization: Bearer $TOKEN" | jq -r '.result.status')
      if [ "$STATUS" = "Complete" ]; then
        break
      fi
      sleep 5
    done
    
    # Get error count from status response
    FINDINGS=$(curl -s https://instance.service-now.com/api/sn_se/v1/scan_operations/scan_status?scan_result_sys_id=$SCAN_ID \
      -H "Authorization: Bearer $TOKEN" | jq -r '.result.summary.total_errors')
    
    if [ $FINDINGS -gt 0 ]; then
      echo "Scan found $FINDINGS errors. Failing deployment."
      exit 1
    fi
    echo "Scan passed. Proceeding with deployment."
    ```

3.  Set up scheduled health checks.

    To monitor your instance health overnight:

    1.  Schedule a cron job to trigger an `instance` scan each night at a low-traffic time.
    2.  Log the returned `scan_result_sys_id` for tracking and historical analysis.
    3.  Read `.result.summary.se_score` from the status response once the scan is complete.
    4.  Set up alerting rules — if `se_score` drops below your threshold, for example below 80, send a notification to your team.
    **Example cron job script:**

    ```
    #!/bin/bash
    # Run nightly at 2:00 AM
    # 0 2 * * * /usr/local/bin/nightly-scan.sh
    
    TIMESTAMP=$(date +%Y-%m-%d_%H-%M-%S)
    SCAN_LOG="/var/log/scan-engine/nightly-$TIMESTAMP.log"
    
    # Trigger the scan
    RESPONSE=$(curl -X POST https://instance.service-now.com/api/sn_se/v1/scan_operations/scan \
      -H "Authorization: Bearer $TOKEN" \
      -H "Content-Type: application/json" \
      -d '{"scan_mode": "instance", "trigger_channel": "api", "instance_scan_type": "delta"}')
    
    SCAN_ID=$(echo $RESPONSE | jq -r '.result.scan_result_sys_id')
    echo "Scan ID: $SCAN_ID" >> $SCAN_LOG
    
    # Poll until complete
    while true; do
      STATUS_RESPONSE=$(curl -s https://instance.service-now.com/api/sn_se/v1/scan_operations/scan_status?scan_result_sys_id=$SCAN_ID \
        -H "Authorization: Bearer $TOKEN")
      STATUS=$(echo $STATUS_RESPONSE | jq -r '.result.status')
      if [ "$STATUS" = "Complete" ]; then
        SE_SCORE=$(echo $STATUS_RESPONSE | jq -r '.result.summary.se_score')
        break
      fi
      sleep 10
    done
    
    echo "Scan complete. Health score: $SE_SCORE" >> $SCAN_LOG
    
    # Alert if score is below threshold
    if (( $(echo "$SE_SCORE < 80" | bc -l) )); then
      echo "Health score dropped below 80. Sending alert." >> $SCAN_LOG
    fi
    ```

4.  Run parallel application scans.

    The `application` mode natively accepts an array of application sys\_ids in a single request. The response returns an array of `scan_result_sys_ids`, one per queued application. Poll each scan result independently:

    ```
    {
      "scan_mode": "application",
      "trigger_channel": "api",
      "application_sys_ids": [
        "<app1_sys_id>",
        "<app2_sys_id>",
        "<app3_sys_id>"
      ]
    }
    ```

    **Response:**

    ```
    {
      "result": {
        "scan_result_sys_ids": ["<scan1_id>", "<scan2_id>", "<scan3_id>"],
        "applications_queued": 3,
        "errors": []
      }
    }
    ```

    Poll each scan result independently using `GET /scan_status` with each `scan_result_sys_id`. Per-application concurrency applies, so you can safely run multiple application scans in parallel.

    **Note:** The `update_set` mode supports the same multi-target pattern using an array of `update_set_sys_ids`. When one item in a multi-target request fails, its entry in the `errors` array may include a `reason` field explaining why that target failed, without blocking the others.

5.  Handle errors in automated workflows.

    Your automation should account for common API errors:

    |Error|What to do|
    |-----|----------|
    |409 CONCURRENT\_SCAN\_RUNNING|A scan is already active. Wait 30 seconds and retry.|
    |401 NOT\_AUTHENTICATED|Your token expired or is invalid. Re-authenticate and retry.|
    |403 NOT\_AUTHORIZED|Your service account is missing the `sn_se.scan_engine_user` role. Contact your administrator.|
    |500 INTERNAL\_ERROR|A server-side issue occurred. Log the error and retry with exponential backoff.|
    |413 PAYLOAD\_TOO\_LARGE|Your request body exceeds 64KB. Reduce the request size and retry.|

    See [Scan Engine API error codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/api-error-codes-grouped.md) for the full error code reference.

6.  Monitor API usage.

    Track all API calls by checking the `sn_se_api_audit` table in your instance to identify patterns and troubleshoot issues.


## Result

The Scan Engine scans run automatically as part of your deployment or health-check workflows, allowing you to identify issues early and maintain system health without manual intervention.

**Parent Topic:**[Scan Engine Headless REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-headless-api-overview.md)

