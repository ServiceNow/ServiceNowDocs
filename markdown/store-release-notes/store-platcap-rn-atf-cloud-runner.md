---
title: ATF Test Generator and Cloud Runner release notes
description: Version history for the ATF Test Generator and Cloud Runner on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-atf-cloud-runner.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ATF Test Generator and Cloud Runner release notes

Version history for the ATF Test Generator and Cloud Runner on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.5 - May 2026**
    -   Removed legacy ca certificate which is no longer necessary for mutual auth
    -   Fixed a bug that prevented an invalid cloud user from being properly unset
    -   Fixed an issue in TestUserAPILibrary that failed to detect invalid users
-   **Version 3.0.0 - March 2026**
    -   Fixed a bug where users with glide.invalid\_query.returns\_no\_rows set to true were unable to set the cloud user properly
    -   Fixed a bug that caused date and time fields in catalog items to be handled improperly by test generation
-   **Version 2.9.1 - December 2025 \(Zurich\)**
    -   Fixed:
        -   Tests with UI steps time out when Limit Concurrent Sessions plugin is active and set for Cloud Runner user
        -   Record producer steps are timing out in Cloud Runner
-   **Version 2.8.0 - August 2025**
    -   Fixed:
        -   Fixed wait timeouts in Client and Cloud runners to mitigate difference in test results in multiple runs
        -   Fixed REST API for running test suites to mitigate test execution errors when testId is passed
        -   Fixed Non-admin user access to ATF test generator table with 2.7.3 ATF Cloud Runner store app
-   **Version 2.7.3 - May 2025**

    Customers can now see the number of Cloud Runner Lanes they are entitled to displayed on the ATF Test Generator page.

-   **Version 2.6.1 - February 2025**
    -   Fixed:
        -   Customers with alt sys\_id for admin can set cloud runner
        -   Improved network error handling, helping with test execution
-   **Version 2.5.4 - November 2024**

    Starting with the 2.5 release, with the same single click test generation experience, generated tests will automatically include test steps for flows for forms.

-   **Version 2.4.6 - August 2024**

    Flow Generation: Starting 2.4.6 release, with the same single click test generation experience, Service Catalog generated tests will automatically include test steps that drive the associated Flow to completion.

-   **Version 2.3.8 - May 2024**
    -   Application is now available for customers in the Australia SPP restricted environment
    -   General performance and stability improvements
-   **Version 2.2.7 - April 2024**
    -   Fixed:
        -   PRB1740597: Intermittent timeouts causing failures in 2.1+
        -   PRB1746799: Broken ACL has wrong Script Include name and is missing roles
-   **Version 2.2.5 - February 2024**
    -   New:
        -   Ability to save generated tests in a specific Scope
        -   Ability to automatically save generated tests under the scope their table or catalog item belong to
        -   Server-side JavaScript API and REST API to perform common Test Generator and Cloud Runner operations including:
            -   Starting a test
            -   Canceling a test
            -   Querying test status
            -   Starting test generation
            -   Canceling test generation
            -   Set Cloud User
            -   and more
    -   Fixed:
        -   Generation errors when attempting to generate Service Catalog tests that lack permission
        -   Other general stability and performance improvements
-   **Version 2.1.11 - November 2023**
    -   New:
        -   Generation Presets
            -   Allows customers to create new and more advanced generation options and save them for reusability
    -   Changed:
        -   Advanced test generation options
            -   Users can now leverage Condition Builder to create complex generation options for Users \(including Groups and Roles using Related List condition\), Tables, and Service Catalog items
    -   Fixed:
        -   PRB1698533: ATF Test Generator and Cloud Runner: Update sets are not always set to "Completed" state
        -   Other miscellaneous stability fixes
-   **Version 2.0.4 - August 2023**
    -   Changed: Expanded Test Generator support for Service Catalog:
        -   Service Catalog Item test generation
        -   Service Catalog Record Producer test generation
    -   Fixed:
        -   Improved Browser Orchestration Queue table progress bar accuracy
        -   Fixed Tests with custom events failing in Cloud Runner
        -   Fixed Cloud Runner tests timing out due to Max Waiters Reached error
        -   Other miscellaneous stability improvements
-   **Version 1.2.6 - May 2023**
    -   Faster generation times
    -   Ability to generate tests by Scope
    -   Increased job progress visibility in the Browser Orchestration Queue table in the form of Journal Entries
    -   Various stability fixes
-   **Version 1.1.1 - February 2023**
    -   Fixed:
        -   Inactive and Locked users are not filtered from cloud users list
        -   Harmless console error for sandbox attribute "allow-downloads-without-user-activation" - not a valid attribute in Chrome anymore
        -   When navigating to a page, getting a non-200 error causes the browser to become stuck.
        -   Wrong message shown when login is rejected and browser is redirected
-   **Version 1.0.7 - November 2022**
    -   New:
        -   You have the ability to automatically generate tests for an instance with the click of a button.
        -   You have the ability to run all test in ATF on the cloud runner that is hosted in ServiceNow infrastructure.
        -   Customers can run up to two tests in parallel for free on the cloud runner.

