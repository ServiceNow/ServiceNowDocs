---
title: Automatically closing stale test results in Configuration Compliance
description: You can activate the Auto-Close Stale Test Results feature to automatically close older test results not recently found by your third-party integrations. Moving these test results to Closed-Stale reduces the number of active test results and remediation tasks in your instance and helps you reconcile assets in your Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Automatically closing stale test results in Configuration Compliance

You can activate the Auto-Close Stale Test Results feature to automatically close older test results not recently found by your third-party integrations. Moving these test results to **Closed-Stale** reduces the number of active test results and remediation tasks in your instance and helps you reconcile assets in your Configuration Management Database \(CMDB\).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Overview

The Auto Close Stale Test Results module helps you automatically close older, stale test results not recently found by your third-party integrations. Test results are moved to **Closed-Stale** based on the conditions you set in the condition builder.

## Key terms

-   **Test result**

    Tests results are imported results from libraries of configuration tests that are mapped to frameworks, policies, and authoritative sources that define how a class of technology assets should be governed. The Configuration Compliance application does not calculate the test results but imports them with third-party integrations.

-   **Asset last scanned date**

    Refers to the value of Last configuration compliance scan date column of the Discovered Item table that is related to the test result. This date refers the most current date and time an asset was last scanned by a third-party scanner.

-   **Last failed date**

    Refers to the Last seen column date of the Test Results table when the **Result** field value is \[failed\].

-   **Stale test results**

    Refers to test results in your instance that are aged and have not been found, updated, or detected by third-party integration scans for a significant amount of time.

-   **Test Results last found**

    This search option uses a date and time provided by the third-party scanner. This term refers to the most current, or latest date \(days ago\) that test results were found again by the scanner. This parameter can be configured.


## Use case

At times, assets \(configuration items\) might be decommissioned in your environment or purged by third party-scanners. When this happens, the assets' associated configuration test results are not updated in the Configuration Compliance application by imported detections and they become inactive \(stale\).

To reduce the number of active test results \(TRs\) and remediation tasks \(RTs\) in your instance, activate the Auto-Close Stale Test Results feature. This feature closes aged test results automatically that have unchanged states or have not been recently imported by your integrations.

As an example, suppose a particular configuration item \(CI\) has multiple asset IDs, and one of these IDs has not been imported on detections from a third-party scanner in the last 90 days. If you set the condition builder in the Auto-Close Stale Test Results module to close tests results that have not been found or updated in the past 90 days or more, this feature automatically closes any test results that match this filtering.

**Note:** This feature only closes test result detections based on the filter conditions that you set in the condition builder and are detected by your third-party scanner integrations.

## The Resolution field

To differentiate between the detections that are closed by third-party scanners such as the Qualys and Tenable.io products and the Auto-Close Stale Test Results feature in your instance, a new value for the **Resolution** field, \[Closed-Stale\], has been added. **Closed-Stale** indicates that a TR was closed by the auto-close feature. **Closed** or **Fixed-Closed** indicates that a TR was closed by a scanner.

## Rollup of TR states to TRGs with the Auto-Close feature

The state progression and precedence for test results is: **Open** &gt; **Closed** &gt; **Fixed-Closed** &gt; **Closed-Stale**.

1.  If any TRs in a TRG are **Open**, the TRG state is not changed.
2.  If at least one TR is **Closed - Fixed** and the rest are **Closed - Stale**, the TRG state transitions to **Closed - Fixed**.
3.  If all the TRs in a TRG are **Closed - Stale**, the TRG state transitions to **Closed - Canceled**.

## Supported integrations

For more information on the third-party integrations that support this feature, see [Understanding the Qualys Vulnerability Integration](../../secops-integration-vr/qualys/concept/c_QualysVulnIntegration.md) and [Tenable.io integrations with the Vulnerability Response and Configuration Compliance applications](../../secops-integration-vr/tenable/reference/tenable-io-integrations-list.md).

