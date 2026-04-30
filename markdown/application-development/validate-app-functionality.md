---
title: Validate app functionality
description: As the application is built, validate that it works as expected.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Validate app functionality

As the application is built, validate that it works as expected.

## Unit testing

Unit/Story testing ensures requirements specified in a story are validated before closing the story. A Story/Unit is a smallest testable portion of system or application that can be configured and executed.

When the configuration of the story is complete, developers need to unit test the features not only in the context of that particular story, but also other related stories that share components with the current story.

As a good practice, developers need to assign the story to process owner or designated stakeholder to validate the story configuration meets expected outcomes before closing the story.

ServiceNow’s Automated Test Framework \(ATF\) is primarily meant for automating functional testing of applications but in few cases can be used to automate unit testing of configurations that involve Script Includes and Business Rules.

## System testing

System testing is performed on a complete system when development is completed. Test the overall interaction of components and integrations with other applications within scope. System testing is performed by the QA/Testing team, but developers need to collaborate with the QA team and process owners to ensure test cases provide comprehensive coverage. Developers will be responsible for remediation of issues found during System Testing.

## Automated Test Framework

Automated Test Framework \(ATF\) should be leveraged for automating functional system testing of ServiceNow applications to reduce testing time and costs and make testing repeatable and UI independent. When creating test cases, follow these guidelines.

When creating tests:

-   Use [parameterized testing](https://servicenow.com/docs/bundle/paris-application-development/page/administer/auto-test-framework/concept/parameterized-tests.html) to avoid duplicate test cases.
-   Follow a Test naming standard.
    -   `<app initial>: <functionality that is being tested>`
    -   CSM: Resolve case
-   Describe each test’s use case in its description. For example: Sample that tests use case.
-   Develop tests on a Development instance and promote/run the test on a Test instance.
-   Clones wipe out tests. Use one of these options to preserve tests:
    -   Bundle tests in a scoped app and upload the app to GIT.
    -   Save tests before the clone.
    -   Promote tests to prod instance, but DO NOT EXECUTE THE TESTS IN PROD.
-   Create self-contained tests.
-   Create new server-side or REST test steps any test steps are missing. For example: Email body verification.
-   Use server-side test step whenever possible and when screenshots are not important.
-   Start with the Impersonatestep.
-   Be aware of browser throttling.
-   Use the Test Logs and Test Transactions to troubleshoot test errors.

When creating test suites:

-   Follow a test suite naming standard. For example: ITSM INT: Use cases.
-   Describe the suite.
    -   Test suite description: "This is a sample test suite to test plugin/application".
    -   Provide any additional information possible in the description.
-   Organize test suites by feature areas.

## User acceptance testing

User Acceptance Testing \(UAT\) is a test conducted to evaluate the application’s compliance with the business requirements and assess whether the application is acceptable for delivery. Users, customers, or other authorized stakeholders perform acceptance testing. Developers will be responsible for remediation of issues found during System Testing.

