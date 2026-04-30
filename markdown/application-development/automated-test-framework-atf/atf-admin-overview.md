---
title: Administering the Automated Test Framework \(ATF\)
description: Enable or disable the Automated Test Framework, modify retention policies, move tests between instances, control user access to the Automated Test Framework, and create custom test step configurations and step environments.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Administering the Automated Test Framework \(ATF\)

Enable or disable the Automated Test Framework, modify retention policies, move tests between instances, control user access to the Automated Test Framework, and create custom test step configurations and step environments.

For details about individual properties that control how the Automated Test Framework works, see [Properties](../reference/atf-admin-properties.md).

-   **[Creating custom test step configurations](atf-custom-step-types.md)**  
Step configuration records \(or step configs\) define how each step type behaves. You can create new step configurations that define custom steps that run on the server.
-   **[Working with test step templates](atf-templates.md)**  
Test step templates contain a list of steps to be added all at once to an automated test.
-   **[Testing Configurable Workspace components](atf-conf-ws.md)**  
Simplify test creation by directly interacting with components on most Configurable Workspace pages via the Page Inspector.
-   **[Enable or disable executing Automated Test Framework tests](../task/atf-enable-tests.md)**  
Allow or prevent tests and test suites from executing on this instance.
-   **[Modify data retention policy for ATF test results](../task/atf-edit-table-cleanup.md)**  
Modify the Auto Flush data retention policy, which designates how long the system retains data, and referencing data, for test and test suite results. You can change the frequency of flushing for the sys\_atf\_test\_result or sys\_atf\_test\_suite\_result base tables. This setting controls how far back in time test result data is available.
-   **[Manage status and retention policies for automated test client runners](../task/atf-modify-retention-test-clients.md)**  
Modify how often active client test runners report in to the system and how long the system retains records for inactive client test runners.
-   **[Moving automated tests from one instance to another](../task/atf-move-test.md)**  
Move automated tests from one instance to another using the normal process for update sets.
-   **[Compare results and execution times for different automated test and suite results](../task/atf-compare-runs.md)**  
You can compare execution times for different runs of an automated test or automated test suite. You can also compare results over time for a single automated test suite.
-   **[Administering REST test step configurations](atf-administer-rest.md)**  
Set request and response payload sizes, filter request and response headers, and create basic auth profiles.
-   **[Optimizing automatic test performance](atf-optimize-perf.md)**  
You can troubleshoot automatic test performance by inspecting system transaction log records and potentially shorten execution time by adjusting how often automatic tests capture screenshots.
-   **[Working with scheduled test suites](atf-sched-suites.md#)**  
You can schedule a test suite to run at a specified date and time.

**Parent Topic:**[Automated Test Framework \(ATF\)](atf-landing-page.md)

