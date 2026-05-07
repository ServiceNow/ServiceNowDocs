---
title: Quick start tests for Leader Hub
description: Validate that Leader Hub still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install and configure, Leader Hub, HR Service Delivery, Employee Service Management]
---

# Quick start tests for Leader Hub

Validate that Leader Hub still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=australia&pubname=australia-application-development&ft:locale=en-US).

All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Quick start tests are disabled and read-only test templates. By default, they only produce a pass result when you run them with the default demo data that is provided with the application or feature plugin.

To make quick start tests produce a pass result when you run them with your instance-specific data, copy and configure them to use your instance data.

Use Performance Profiling to compare tests to detect performance degradation when you upgrade your instance, so you can investigate and fix the issues. See [Performance profiling](https://www.servicenow.com/docs/access?context=atf-perf-prof&version=australia&pubname=australia-application-development&ft:locale=en-US).

The Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests \(com.snc.sdlc.agile.2.0.atf\) plugins must be enabled.

**Note:** When running, demo data is required.

## Leader Hub

Leader Hub quick start tests require activating the Leader Hub plugin \(sn\_egd\_lh\) and loading demo data.

<table id="table_ugs_4cx_2dc"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

\[Leader hub\] - Validate LH flows

</td><td>

-   Verifies that the following widgets are present on the At a glance page for user Maria Davies:
    -   Org talent
    -   Skill growth area
    -   Growth engagement
-   Verifies the employee card for the leader who has accessed Leader Hub appears at the top of the organizational chart on the Org talent page.
-   Verifies that selecting the **View team details** button on a card for an employee navigates the leader to the Team details page.

-   Verifies that the Skills widget is present on the Org Skills page.

 **Note:** Requires demo data.

</td><td>

Xanadu

</td></tr></tbody>
</table>To learn more about Leader Hub, see [Leader Hub](../../../product/td-leader-hub/concept/td-lh-landing.md).

-   **[Run quick start tests for Leader Hub](../../../product/td-leader-hub/task/td-lh-run-quick-start-tests.md)**  
Run quick start tests to verify the Leader Hub app still works after each upgrade and deployment of new applications or integrations. If you customized Leader Hub, you must configure the quick start tests to ensure they're compatible with your customizations.

**Parent Topic:**[Installing and configuring Leader Hub](../../../product/td-leader-hub/concept/td-lh-install-config.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

