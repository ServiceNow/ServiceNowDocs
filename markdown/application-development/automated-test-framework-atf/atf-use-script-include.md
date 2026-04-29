---
title: Automated Test Framework use case: test a script include
description: This use case illustrates testing a script include with the Automated Test Framework.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: test a script include

This use case illustrates testing a script include with the Automated Test Framework.

To test a script include with the Automated Test Framework, create a test that performs these steps:

-   a step that causes the system to execute the script include. Examples:
    -   Run Server Side Script test step that calls the script include.
    -   Form action step script – such as open a form, submit or form, or set a field value – that invokes the script include.
-   A step that validates that the script include took the expected actions. The specific test step for this validation depends on what the script include is designed to do. Examples:
    -   Field values validation, if the script sets a field value
    -   Field state validation, if the script changes a field state
    -   Record Query, if the script generates a new record

This example shows a test with one test step: Run Server Side Script. The script associated with this test step calls a script include that returns the value of its argument plus three. If the value returned from the script include is 8, the script include has worked as intended and the test passes.

![Automated test to test a script include](../image/atf-script-include.png "Automated Test to test a script include")

![Run server side script test step](../image/atf-server-side-script-01.png "Automated test step for testing script include")

![Script include](../image/atf-server-side-script-02.png "Script include to test with Automated Test Framework")

**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

