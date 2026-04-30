---
title: Automated Test Framework design considerations
description: Create reliable, scalable, and efficient tests by following these design considerations.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework design considerations

Create reliable, scalable, and efficient tests by following these design considerations.

## General testing

Avoid modifying ServiceNow system tables or tables extending the Application File \[sys\_metadata\] that can potentially change the behavior of the system. Avoid using or modifying any existing records to prevent unexpected results between tests. The following are some of the common examples of system data changes that can cause unexpected results.

-   Impersonate an existing account
-   Delete an existing record.
-   Run a test that disables a business rule or system property
-   Validate with an existing record

## Parallel testing

Reduce test design time by running multiple tests and test suites in parallel. Design tests to run in parallel by avoiding resource conflicts and data dependencies.

**Prevent resource conflicts between parallel tests**

Prevent resource conflicts by running tests that create their own data. Tests that run with existing data prevent other tests that need the same data from running in parallel.

**Note:** If you have two or more resource conflicting tests, see [Mark tests as mutually exclusive](mutual-exclusion-rule.md#section_egk_ztm_thb) to create a mutual exclusion rule that prevents them from running in parallel.

## Parameterized testing

Run a test multiple times with different test data for each run. Create parameters to store test data for each test run. See [Parameterized test components](parameterized-tests.md#section_vgs_nmq_sfb) for more information.

-   Create parameters to store test data for each test run.
-   Ensure that the parameterized tests support standard Automated Test Framework \(ATF\) features, such as reports, test suites, and data rollback. Copying a parameterized test copies all parameters, test run data sets, and test steps.

    **Note:** If a parameterized test including Custom UI test steps is created, the system only uses the first data set to retrieve components.


## Custom UI testing

Test customized user interfaces such as UI pages and UI macros by retrieving their HTML and JavaScript page components and identifying the test actions they support.

-   **Use the page inspector to identify testable page components**

    The page inspector determines which page components are available for custom UI testing. Page components that are unavailable to the page inspector are unavailable to custom UI testing.

-   **Navigate to the custom UI you want to test**

    Use existing test steps to navigate to the target custom UI. For example, to test a Knowledge Base article, use the existing test steps to navigate to a module or to open an existing record. Most custom UI testing requires using existing test step categories as part of the test.

-   **Use the component area to identify page components**

    The component area describes the HTML layout element containing the component such as a `<div>` or `<section>` element. The area helps test designers distinguish between components by providing the location in the page layout.

-   **Test your custom UI rather than ServiceNow AI Platform UI**

    The Automated Test Framework prevents custom UI testing of ServiceNow AI Platform features. For example, you cannot test dashboards or graphical designers. Instead, build tests to validate your custom UI pages and elements because you have direct control over these user interfaces.

-   **Use HTML attributes to override page component testing properties**

    Change the testing properties of a particular page component using HTML attributes that are specific to Automated Test Framework. See [Override component test actions](../task/develop-testable-components.md#).

-   **Retrieve page components again when you move tests to another instance**

    Custom UI test steps don’t store UI components as metadata. Testers must manually retrieve page components again when moving tests between instances.


## Clone tests from production system

Move your tests to the production system to clone the most updated instances for testing. Speed up the testing time by directly copying or cloning a test from the production system to a subproduction instance.

**Note:** By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances.

## Warning messages for all testing

|Warning messages|Design considerations|
|----------------|---------------------|
|`Impersonating an existing user may cause unexpected behavior for this test. Avoid potential issues by adding a 'Create a User' step instead. See the documentation for Test Design Considerations`.|Create a new user to ensure proper roles and groups and avoid using existing records. See [General testing](automated-test-framework-design-considerations.md#section_hq5_mxs_vhb) for more information.|
|`Using a table that extends Application File [sys_metadata] may cause unexpected behavior for other tests running in parallel. See the documentation for Test Design Considerations`.|Avoid running a test with a table that extends the Application File because it might affect other tests. See [Parallel testing](automated-test-framework-design-considerations.md#section_vkd_4jp_nhb) for more information.|
|`Using a system table may cause unexpected behavior for other tests running in parallel. See the documentation for Test Design Considerations`.|Avoid using a system table because it might affect other tests running in parallel. See [Parallel testing](automated-test-framework-design-considerations.md#section_vkd_4jp_nhb) for more information.|
|`Using an existing record may cause unexpected behavior for this test. See the documentation for Test Design Considerations`.|Avoid using existing records because these records might not have the state and values as expected by the test. Use records created during the test to ensure proper state and values. See [General testing](automated-test-framework-design-considerations.md#section_hq5_mxs_vhb) for more information.|
|`Modifying an existing record may cause unexpected behavior for other tests running in parallel. See the documentation for Test Design Considerations`.|Avoid using existing records because it might affect other tests. Use records created during the test. See [General testing](automated-test-framework-design-considerations.md#section_hq5_mxs_vhb) for more information.|
|`Using assert type '--None--' may cause unexpected behavior for server UI actions. Avoid potential issues by setting the assert type and using a timeout. See the documentation for Test Design Considerations`.|Server UI actions cause the current form to submit and the page to reload. Select an assert type other than **None** to avoid any unexpected behavior for server UI actions. Set a timeout to ensure that your test waits for the form to be submitted or not submitted before moving on to the next step. When testing server UI actions, the **None** assert type configures automatically to **Form submitted to server**.|

## Domain separation testing

When testing domain separation, you must set the domain first. This should be part of the first impersonation step of each of the ATF test steps when they are dependent on a domain being set. To learn more about domain separation recommended practices, see [Domain separation recommended practices for service providers](https://www.servicenow.com/docs/access?context=bp-domain-sep-recommended&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Automated Test Framework \(ATF\) reference](atf-ref-overview.md)

