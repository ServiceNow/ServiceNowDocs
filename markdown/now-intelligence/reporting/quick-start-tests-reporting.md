---
title: Quick start tests for Reporting
description: Validate that Reporting still works after you make any configuration change such as applying an upgrade. Copy and customize these quick start tests to pass when using your instance-specific data.You can customize these pre-configured example test steps.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Quick start tests for Reporting

Validate that Reporting still works after you make any configuration change such as applying an upgrade. Copy and customize these quick start tests to pass when using your instance-specific data.

The Reporting quick start test Automated Test Framework - Reporting plugin \(com.glide.automated\_testing\_impl.report\) is active by default or instance reboot.

**Note:** Reporting quick start tests do not test report access from dashboards. To test dashboards, see [Quick start tests for Dashboards](quick-start-tests-dashboards.md).

|Test|Description|Release version|
|----|-----------|---------------|
|Report Visibility|Confirm whether reports are still visible to users whom they are shared with.|Madrid|

**Parent Topic:**[Administering reports](../../../use/reporting/concept/c_AdminsteringReports.md)

**Related topics**  


[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/quick-start-tests.md)

## Report Visibility test steps

You can customize these pre-configured example test steps.

### Before you begin

Role required: admin.

### About this task

The Report Visibility test contains two types of steps:

-   **Impersonate**

    When configuring this step, select which user to impersonate when executing the Confirm steps that follow. Select a user with the role or roles whose access you are testing.

-   **Report Visibility**

    When configuring this step, select which report to test. Also select whether the test succeeds with positive results or with negative results. In other words, set whether Report Visibility succeeds when the user can view the report or when the user cannot view the report.


The example test included in the plugin includes the following three steps.

### Procedure

1.  Impersonate the user.

2.  Confirm a test report can be viewed by the test user.

3.  Confirm a test report cannot be viewed by the test user.


### What to do next

However, when you customize a test, you can combine steps in any logical sequence by adding and configuring the two types of steps. For example, you could configure the Report Visibility test as follows:

1.  Impersonate a user.
2.  Confirm that this user can view a report.
3.  Confirm that this user can view another report.
4.  Confirm that this user cannot view a third report.

