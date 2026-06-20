---
title: Combined Automated Test Framework release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Automated Test Framework from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-automatedtestframework-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Automated Test Framework release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Automated Test Framework from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Automated Test Framework release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Automated Test Framework to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

 The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://servicenow-staging.fluidtopics.net/access?context=available-quick-start-tests&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

 The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://servicenow-staging.fluidtopics.net/access?context=available-quick-start-tests&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Automated Test Framework.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Reusable tests](https://servicenow-staging.fluidtopics.net/access?context=atf-reuse-tests&family=yokohama&ft:locale=en-US)**

Reduce duplication of tests while invoked in several other tests by creating reusable tests, enabling test design to be more modular, reducing the effort and time while duplicating tests to manage a large number of tests across your instance. You can access the reusable tests from the new Reusable Test test step category. Use the Reusable Input Variables and Reusable Output Variables related lists to define data passing from one test step to another.

-   **[Reusable Tests category](https://servicenow-staging.fluidtopics.net/access?context=test-steps-reusable-tests-category&family=yokohama&ft:locale=en-US)**

Reuse the test records created in the Reusable Test table from the new Reusable Test test step category. By default, the test records show up in the Reusable Test test step category, unless you define the record in a custom category in the Category field.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ATF failure insights](https://servicenow-staging.fluidtopics.net/access?context=atf-test-triage&family=zurich&ft:locale=en-US)**

Reduce the time to resolve your ATF test failures with actionable support from the new ATF failure insights feature.

-   **[Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=atf-conf-ws&family=zurich&ft:locale=en-US)**

Enable simplified test creation through direct component interaction on Configurable Workspace pages via the Page Inspector.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Automated Test Framework features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Automated Test Framework features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Automated Test Framework features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Automated Test Framework.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Automated Test Framework is a ServiceNow AI Platform feature that is active by default.

**Note:** By default, the system property that is used to run automated tests is turned off to help prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. For more information, see [Enable or disable executing Automated Test Framework tests](https://servicenow-staging.fluidtopics.net/access?context=atf-enable-tests&family=yokohama&ft:locale=en-US).

 To use the quick start tests for an application, activate the plugin that is associated with the application. For more information, see [Available quick start tests by application or feature](https://servicenow-staging.fluidtopics.net/access?context=available-quick-start-tests&family=yokohama&ft:locale=en-US).

 Set the **sn\_atf.runner.enabled** property to **True** to activate the content pack for the ATF Test Generator and Cloud Runner store application.

</td></tr><tr><td>

Zurich

</td><td>

Automated Test Framework is a ServiceNow AI Platform feature that is active by default.

**Note:** By default, the system property that is used to run automated tests is turned off to help prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. For more information, see [Enable or disable executing Automated Test Framework tests](https://servicenow-staging.fluidtopics.net/access?context=atf-enable-tests&family=zurich&ft:locale=en-US).

 To use the quick start tests for an application, activate the plugin that is associated with the application. For more information, see [Available quick start tests by application or feature](https://servicenow-staging.fluidtopics.net/access?context=available-quick-start-tests&family=zurich&ft:locale=en-US).

 Set the **sn\_atf.runner.enabled** property to **True** to activate the content pack for the ATF Test Generator and Cloud Runner store application.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Automated Test Framework we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Automated Test Framework we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Automated Test Framework supports running tests only from desktop browsers. You can't run tests or test suites from tablets, mobile browsers, or the mobile UI. Some desktop browsers require additional configuration. For more information, see [Browser recommendations for Automated Test Framework](https://servicenow-staging.fluidtopics.net/access?context=browser-recommendations-atf&family=yokohama&ft:locale=en-US).

 Automated Test Framework offers limited support for test design on tablets. You can't add new custom UI test steps from tablets because tablets can't retrieve components. Review any existing custom UI test steps that were added from a desktop browser instead.

</td></tr><tr><td>

Zurich

</td><td>

Automated Test Framework supports running tests only from desktop browsers. You can't run tests or test suites from tablets, mobile browsers, or the mobile UI. Some desktop browsers require additional configuration. For more information, see [Browser recommendations for Automated Test Framework](https://servicenow-staging.fluidtopics.net/access?context=browser-recommendations-atf&family=zurich&ft:locale=en-US).

 Automated Test Framework offers limited support for test design on tablets. You can't add new custom UI test steps from tablets because tablets can't retrieve components. Review any existing custom UI test steps that were added from a desktop browser instead.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Automated Test Framework, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Automated Test Framework we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Automated Test Framework we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create and schedule test suites to organize and run tests in batches.
-   Reduce test design time by copying quick start tests and test suites. You can also create custom test steps to expand test coverage.

 See [Automated Test Framework \(ATF\)](https://servicenow-staging.fluidtopics.net/access?context=atf-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create and schedule test suites to organize and run tests in batches.
-   Reduce test design time by copying quick start tests and test suites. You can also create custom test steps to expand test coverage.

 See [Automated Test Framework \(ATF\)](https://servicenow-staging.fluidtopics.net/access?context=atf-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

