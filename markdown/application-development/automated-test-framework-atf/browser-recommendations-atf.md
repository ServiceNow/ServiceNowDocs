---
title: Browser recommendations for Automated Test Framework
description: Configure client test runner browsers to run automated tests and avoid performance degradations.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [UI test steps, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Browser recommendations for Automated Test Framework

Configure client test runner browsers to run automated tests and avoid performance degradations.

## Periodic browser restarts

These browsers have memory-management limitations that make it necessary to occasionally close and restart the browser when running the client test runner.

-   Internet Explorer
-   Edge
-   Older versions of Firefox

How often you should close the browser depends on the memory allocation in the browser application.

## Browser CPU throttling

Some browsers throttle CPU usage for windows that are out of focus. Follow these guidelines to avoid CPU throttling issues.

-   Run each client test runner in its own browser window.
-   Ensure that the client test runner browser window is always partially visible on the screen.
-   Ensure that the system screen is not locked or shut off.

## Browser zoom level

Client test runners take screen shots as they run tests. For best results with screen shots, leave the browser zoom level set to 100%.

## OS X CPU throttling

On OS X with the client test runner on Chrome or Safari: If the screen is locked or the client test runner tab is not shown, when the system attempts to run the test suite, tests run significantly slower and may time out. For best performance, run client test runners for scheduled suites in a virtual machine \(VM\) environment in which the screen does not become locked or disabled.

## Rollback in browser sessions

The session cookies roll back all the changes made during a test. When a test is running, everything performed in that session is recorded for rollback. Don't modify your instance when a test is running in the same browser session. For example, if you modify records while a test is running in the same session, the changes are rolled back after the test completes. If you navigate around in other tabs in the same session, your work may be rolled back and interfere with tests that rely on implicit navigation.

## Parallel testing

Follow these guidelines to avoid issues when running multiple tests in parallel.

-   **Run each client test runner in an incognito or private window**

    Because parallel tests roll back all changes tied to the same browser session, it's possible for legitimate changes made in another browser tab to be rolled back during parallel testing. To prevent unwanted rollback of changes, always run client test runners in their own browser session. Opening client test runners in an incognito or private window ensures that they always have their own browser session.

-   **Close client test runner windows when testing is complete**

    To prevent unwanted rollback of changes, always close client test runners after testing is complete. Closing the browser window ensures that test rollback doesn't revert any legitimate changes made in another browser tab.


**Parent Topic:**[UI test steps](ui-test-steps.md)

