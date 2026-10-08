---
title: ATF Health Check
description: ATF Health Check detects ATF misconfiguration that may lead to support cases by scanning your instance for 14 known issues and providing findings you can resolve proactively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-health-check-suites.html
release: brazil
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 4
keywords: [ATF Health Check, instance scan, automated test framework, diagnostic checks]
breadcrumb: [Automated Test Framework \(ATF\) test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# ATF Health Check

ATF Health Check detects ATF misconfiguration that may lead to support cases by scanning your instance for 14 known issues and providing findings you can resolve proactively.

ATF Health Check is a set of Instance Scan checks for the Automated Test Framework \(ATF\). It inspects your instance's ATF configuration, tests, and step definitions for a known list of configurations and deviations from general guidelines. Each issue is reported as a finding you can act on.

The checks were built directly from the issues seen most often in ATF-related support cases. Examples include `gs.sleep()` calls left in test scripts, tests that modify large numbers of existing records, ATF Debug mode left enabled, and an invalid ATF Cloud User. Running the scan lets you confirm whether any of those issues are present on your instance, so you can resolve them proactively.

## Prerequisites

The following prerequisites must be met to use ATF Health Check:

-   The base Automated Test Framework plugin \(`com.glide.automated_testing_framework`\) and the Instance Scan plugin \(`com.glide.instance_scan`\) must be active
-   You need the `admin` role to execute the scan suites
-   The `admin` role is also required to change the configurable modified-records threshold
-   The four checks in the ATF Test Generator and Cloud Runner suite run only if the ATF Test Generator and Cloud Runner Store app \(`sn_atf_tg`\) is active. Otherwise, they are skipped automatically

## Terminology

-   **Instance Scan**

    The ServiceNow platform capability that runs configurable checks against an instance and reports the results as findings

-   **Suite**

    A named, organized group of related checks that can be run together

-   **Check**

    A single, specific test performed during a scan—for example, "is ATF Debug mode enabled?"

-   **Finding**

    A flagged result produced when a check's condition is met—that is, an issue was detected


## What's Included

ATF Health Check adds one parent suite with two child suites underneath it:

ATF Health Check Suites \(parent\): Root container for the following child suites. Run this suite to execute every ATF Health Check scan in one pass

-   ATF Core \(10 checks\): Covers core ATF configuration, test design, and performance. Available on any instance with the base ATF plugin active. Organized into Performance checks \(7\) and Upgradability checks \(3\)
-   ATF Test Generator and Cloud Runner \(4 checks\): Covers the ATF Test Generator and Cloud Runner \(TG/CR\) store app. These checks only execute if `sn_atf_tg` is active. Organized into Manageability checks \(3\) and Upgradability checks \(1\)

Each finding links directly to the affected record, so you can navigate and resolve issues immediately.

## Check categories

Checks are organized by category to help you prioritize and understand the scope of each issue:

-   Performance: Identifies configurations that slow down test execution, such as debug mode, fixed waits, excessive screenshots, or tests that modify too many records
-   Upgradability: Verifies that ATF data, configurations, and tests follow best practices that support clean instance cloning and upgrades
-   Manageability: Validates that infrastructure and integrations \(mutual authentication, Cloud Runner app, ADCV2 configuration\) are correctly configured for Test Generator and Cloud Runner

-   **[Run an ATF Health Check scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-health-check-run-scan.md)**  
Execute an ATF Health Check scan to detect configuration issues on your instance. You can run a full suite of all 14 checks, run only core checks, run checks for ATF Test Generator and Cloud Runner, or run a single check.
-   **[ATF Health Check checks and configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-health-check-checks.md)**  
Look up all 14 ATF Health Check scans, understand what each check detects, and configure the modified-records threshold to fit your environment.

**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-test-type-testing.md)

**Related topics**  


[Reusable tests]()

[Mutually exclusive tests]()

[Quick start tests]()

[Parallel testing]()

[Accelerate ATF tests failure resolution]()

[Performance profiling]()

[ATF administration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-admin-overview.md)

[Optimizing ATF performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-optimize-perf.md)

[ATF test suites overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-suites-overview.md)

