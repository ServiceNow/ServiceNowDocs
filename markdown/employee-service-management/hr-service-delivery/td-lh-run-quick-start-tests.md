---
title: Run quick start tests for Leader Hub
description: Run quick start tests to verify the Leader Hub app still works after each upgrade and deployment of new applications or integrations. If you customized Leader Hub, you must configure the quick start tests to ensure they're compatible with your customizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/td-lh-run-quick-start-tests.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Quick start tests, Configure, Leader Hub, HR Service Delivery, Employee Service Management]
---

# Run quick start tests for Leader Hub

Run quick start tests to verify the Leader Hub app still works after each upgrade and deployment of new applications or integrations. If you customized Leader Hub, you must configure the quick start tests to ensure they're compatible with your customizations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Search and select the quick start tests you want to run.

    For information on available quick start tests, see [Quick start tests for Leader Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/quick-start-tests-leader-hub.md).

3.  Click **Run Test**.

    The Test Steps tab provides each step of the quick start test.

    After the tests run, the Step Results tab shows the status of each test step. Screen shots also appear at the top of the form as attachments.


## What to do next

Use Performance Profiling to compare tests to detect performance degradation when you upgrade your instance, so you can investigate and fix the issues. See [Performance profiling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/automated-test-framework-atf/atf-perf-prof.md).

**Parent Topic:**[Quick start tests for Leader Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/quick-start-tests-leader-hub.md)

