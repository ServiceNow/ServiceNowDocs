---
title: Run an ATF Health Check scan
description: Execute an ATF Health Check scan to detect configuration issues on your instance. You can run a full suite of all 14 checks, run only core checks, run checks for ATF Test Generator and Cloud Runner, or run a single check.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-health-check-run-scan.html
release: brazil
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 2
keywords: [ATF Health Check, instance scan, run scan, automated test framework]
breadcrumb: [ATF Health Check, Automated Test Framework \(ATF\) test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Run an ATF Health Check scan

Execute an ATF Health Check scan to detect configuration issues on your instance. You can run a full suite of all 14 checks, run only core checks, run checks for ATF Test Generator and Cloud Runner, or run a single check.

## Before you begin

Role required: admin

## About this task

Before running an ATF Health Check scan, verify the following:

-   The base Automated Test Framework plugin \(`com.glide.automated_testing_framework`\) is active
-   The Instance Scan plugin \(`com.glide.instance_scan`\) is active
-   The ATF Health Check plugin \(`com.glide.automated_testing_impl.atf_health_check`\) is installed

For checks in the ATF Test Generator and Cloud Runner suite to execute, the ATF Test Generator and Cloud Runner store app \(`sn_atf_tg`\) must be active. If the app is not active, those checks are skipped automatically.

## Procedure

1.  Navigate to **Instance Scans** &gt; **Suites**.

2.  Open one of the following suites:

    -   ATF Health Check Suites — Run all 14 checks \(both ATF Core and ATF Test Generator and Cloud Runner checks\)
    -   ATF Core — Run only the 10 core ATF checks
    -   ATF Test Generator and Cloud Runner — Run only the 4 checks for the Test Generator and Cloud Runner store app
3.  Select **Execute Suite Scan**.

4.  Wait for the scan to complete.

    **Note:** Scan time depends on the size of your instance and the number of checks being run.

5.  Open the scan results to view the status of each check.

    The results show whether each check passed and how many findings it produced.

6.  For each check with findings, open the check record to review its individual findings.

    Each finding links directly to the affected record, such as the specific ATF test, step, step config, or property. You can navigate to the record and resolve the issue.

    **Note:** To run a single check, open the check record and select **Test Check** or **Run Point Scan**. You can also schedule the suite using Instance Scan scheduling options.


## Result

The scan completes and displays findings for any issues detected on your instance. Each finding includes:

-   The check that detected the issue
-   The specific record affected \(test, step, property, etc.\)
-   Details about the issue

Navigate to each affected record using the links in the findings to review and resolve the configuration issue.

**Parent Topic:**[ATF Health Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-health-check-suites.md)

