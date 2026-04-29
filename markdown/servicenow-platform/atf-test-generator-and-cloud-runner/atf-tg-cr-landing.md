---
title: Exploring ATF Test Generator and Cloud Runner
description: Use the ATF Test Generator and Cloud Runner application to generate tests depending on the instance behavior and workflows. You can also execute the generated tests using the Cloud Runner option.
locale: en-US
release: australia
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Exploring ATF Test Generator and Cloud Runner

Use the ATF Test Generator and Cloud Runner application to generate tests depending on the instance behavior and workflows. You can also execute the generated tests using the Cloud Runner option.

## ATF Test Generator and Cloud Runner overview

These are the main modules in the application.

-   [Select Cloud User](atf-tg-cr-configure.md#): Setting up credentials for cloud runner user.

    ![Image showing the landing page for Select Cloud User module](../image/atf-app-credentials.png)

-   [Generate tests](../task/atf-tg-cr-generate-tests.md): Auto-generating tests and test suites to be executed on cloud runner.

    ![Image showing the Generate Tests module](../image/atf-app-test-generator.png)

-   [Executing tests](../task/atf-tg-cr-execute-tests.md): Executing the generated tests using the Cloud Runner option.

    ![Image showing the test execution with Cloud Runner option](../image/atf-tg-cr-execute-tests.png)

    **Note:** This dialog box is visible when you try executing an ATF test or suite.


## ATF Test Generator and Cloud Runner users

ATF Test Generator and Cloud Runner has the following users.

|Users|Description|
|-----|-----------|
|System Administrator \[admin\]|The System Administrator user is required to access and use the ATF Test Generator and Cloud Runner store application.|

## ATF Test Generator and Cloud Runner benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Set up cloud user to generate and run tests|[Set up cloud user](atf-tg-cr-configure.md#)|System administrator|
|Generate test automatically using ATF Test Generator and Cloud Runner|[Generating the tests](../task/atf-tg-cr-generate-tests.md)|System administrator|
|Execute the tests using the Cloud Runner browser option|[Executing the tests using Cloud Runner](../task/atf-tg-cr-execute-tests.md)|System administrator|
|Schedule tests and test suites execution and nightly runs|[Scheduling test execution](../task/atf-tg-cr-schedule-test-run.md)|System administrator|
|Review the log entries in the BOQ form to debug errors during the execution of the test suites|[Log entries in the BOQ form](atf-tg-cr-log-boq-form.md)|System administrator|

## What to explore next

To learn more about using Log Export Service, see:

-   [Configuring ATF Test Generator and Cloud Runner](atf-tg-cr-configure.md#)
-   [Operating ATF Test Generator and Cloud Runner](atf-tg-cr-operate.md)
-   [Using ATF Test Generator and Cloud Runner](atf-tg-cr-use.md)
-   [ATF Test Generator and Cloud Runner reference](atf-tg-cr-ref.md)

