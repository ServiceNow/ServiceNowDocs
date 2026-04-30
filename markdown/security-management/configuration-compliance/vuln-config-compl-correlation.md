---
title: Configuration Compliance correlation
description: Configuration Compliance provides prioritization and test result grouping \(into remediation task\) to aid remediation of non-compliance issues.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance imported data, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance correlation

Configuration Compliance provides prioritization and test result grouping \(into remediation task\) to aid remediation of non-compliance issues.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Asset-Centric Prioritization

Configuration scans can produce large number of findings. Prioritize findings for greatest risk reduction. Priority includes both configuration test criticality and asset criticality. Configuration test result priority is expressed as a 0–100 scale risk score. Calculator groups compute risk score and can be customized.

When the third-party import is complete, Configuration Compliance sends an event to indicate end-of-import actions. For every active result group, the following actions are taken:

-   Resolved remediation tasks with failed results return to the **Awaiting implementation** state.
-   Remediation tasks where all results passed are **Closed**.
-   The state of test results that are in active remediation tasks is updated.
-   The flag indicating whether a result is part of an active remediation task is updated.

## Remediation Tasks order of precedence

When test results belong to more than one group, the **State** of a test result is derived according to an order of precedence.

The **State** and **Resolution** fields in the **Configuration Test** form and the **Result** field in the **Test Result** form, are calculated following this order of precedence.

**Note:**

The group membership precedence only applies to items where the item did not pass the configuration test. **Passed** items are always in the **Closed-Fixed** state.

The **Result** value determines the state. We ignore remediation tasks in the **Closed-Fixed** and **Closed-Canceled** state. The item state is computed from the states of all other remediation tasks it belongs to or is set to **Open**, if no other group exists for the item.

![Remediation task order of precedence](../image/OrderOfPrecedence.png)

## Remediation Tasks creation

Configuration Compliance Remediation Tasks are created manually.

There are two ways to create and populate **Remediation Tasks**.

-   From the **Remediation Tasks** module and using filters that automatically populate the **Test Results** tab.

    This way is good for when you know what filtering you want to use. For example, capturing all failed test results that are moderate and higher criticality, affect the windows-based infrastructure, and apply only to the SAP supply chain application.

-   By selecting test results in the **Test Results** list and creating a remediation task from the **Actions on selected rows...** menu.

    This method is good for results that are not easily filtered, or situations where you want to specify test results for remediation. For example, outliers that have nothing in common.


**Note:** If you create a remediation task from the **Test Results** list and you later decide to use a filter for that remediation task, your original entries are removed and replaced by the filter results.

## Ungrouped Test Results

**Ungrouped Test Results** contain all non-pass test results that are not members of an active \(non-**Closed**\) remediation task. This module is updated after every import and whenever test results are added or removed from a remediation task.

