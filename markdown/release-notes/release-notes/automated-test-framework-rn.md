---
title: Automated Test Framework release notes
description: The ServiceNow Automated Test Framework enables you to create and run automated tests to confirm that your modified instance works after an upgrade, during application development, or when deploying instance configurations with update sets. Review failed test results to identify the changes that caused the failure and the changes that you should review. Automated Test Framework was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Automated Test Framework release notes

The ServiceNow® Automated Test Framework enables you to create and run automated tests to confirm that your modified instance works after an upgrade, during application development, or when deploying instance configurations with update sets. Review failed test results to identify the changes that caused the failure and the changes that you should review. Automated Test Framework was enhanced and updated in the Zurich release.

## Automated Test Framework highlights for the Zurich release

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create and schedule test suites to organize and run tests in batches.
-   Reduce test design time by copying quick start tests and test suites. You can also create custom test steps to expand test coverage.

See [Automated Test Framework \(ATF\)](https://www.servicenow.com/docs/access?context=atf-landing-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

**Important:** ATF Test Generator and Cloud Runner is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Automated Test Framework to Zurich

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## New in the Zurich release

-   **[ATF failure insights](https://www.servicenow.com/docs/access?context=atf-test-triage&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Reduce the time to resolve your ATF test failures with actionable support from the new ATF failure insights feature.

-   **[Configurable Workspace](https://www.servicenow.com/docs/access?context=atf-conf-ws&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Enable simplified test creation through direct component interaction on Configurable Workspace pages via the Page Inspector.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Automated Test Framework is a ServiceNow AI Platform feature that is active by default.

**Note:** By default, the system property that is used to run automated tests is turned off to help prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. For more information, see [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

To use the quick start tests for an application, activate the plugin that is associated with the application. For more information, see [Available quick start tests by application or feature](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Set the **sn\_atf.runner.enabled** property to **True** to activate the content pack for the ATF Test Generator and Cloud Runner store application.

## Browser requirements

Automated Test Framework supports running tests only from desktop browsers. You can't run tests or test suites from tablets, mobile browsers, or the mobile UI. Some desktop browsers require additional configuration. For more information, see [Browser recommendations for Automated Test Framework](https://www.servicenow.com/docs/access?context=browser-recommendations-atf&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Automated Test Framework offers limited support for test design on tablets. You can't add new custom UI test steps from tablets because tablets can't retrieve components. Review any existing custom UI test steps that were added from a desktop browser instead.

**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

