---
title: Quick start tests for Talent Development Core
description: Validate that these Talent Development Core features still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Talent Development Core
classification: talent-development-core
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configure, Talent Development Core, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Quick start tests for Talent Development Core

Validate that these Talent Development Core features still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Quick start tests are disabled and read-only test templates. By default, they only produce a pass result when you run them with the default demo data that is provided with the application or feature plugin.

To make quick start tests produce a pass result when you run them with your instance-specific data, copy and configure them to use your instance data.

Use Performance Profiling to compare tests to detect performance degradation when you upgrade your instance, so you can investigate and fix the issues. See [Performance profiling](https://www.servicenow.com/docs/access?context=atf-perf-prof&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

The Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests \(com.snc.sdlc.agile.2.0.atf\) plugins must be enabled.

**Note:** When running, demo data is required.

## Growth plans

Growth plans quick start tests require activating the Talent Development Core application \(sn\_egd\_core\) and loading demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|Create and verify a growth plan.|Create a growth plan from the guided flow for Emily Scollan and verify the growth plan on the details page.|Zurich|

To learn more about Growth plans, see [Growth plans overview](../concept/egd-growth-plans-ovrvw.md).

## Aspirations

Aspirations quick start tests require activating the Talent Development Core application \(sn\_egd\_core\).

|Test|Description|Release version|
|----|-----------|---------------|
|Create and verify an aspiration.|Creates an aspiration and verifies that the aspiration is in the Aspirations table \[sn\_egd\_core\_aspiration\].|Zurich|

To learn more about Aspirations, see [Aspirations overview](../concept/egd-aspirations-overview.md).

-   **[Run quick start tests for Talent Development Core](../task/egd-td-core-run-quick-start-test.md)**  
Run quick start tests to verify the Talent Development Core app and features still work after each upgrade and deployment of new applications or integrations. If you customized Talent Development Core, you must configure the quick start tests to ensure they're compatible with your customizations.

**Parent Topic:**[Installing and configuring the Talent Development Core app](../concept/egd-install-config.md)

