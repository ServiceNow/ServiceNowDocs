---
title: UI test steps
description: Test user interfaces by mimicking user actions and interacting with the visible components of a page.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# UI test steps

Test user interfaces by mimicking user actions and interacting with the visible components of a page.

## Client test runner dependency

UI test steps require an active client test runner to act directly on the visible components of a page. A tester must manually start one or more client test runners for UI testing. Test designers can schedule selecting an open client test runner from a test suite. See [Working with client test runners](atf-test-runners.md).

## Intelligent wait mechanism

UI test steps have an intelligent wait mechanism triggered by UI changes such as clicking a component or setting a value. The wait mechanism requires the UI change to complete before the next UI test step can proceed. Test designers do not need to manually add wait mechanisms between UI test steps.

-   **[Custom UI test steps](custom-ui-test-steps.md)**  
Test customized user interfaces such as UI pages and UI macros by retrieving their HTML and JavaScript page components and identifying the test actions they support.
-   **[Browser recommendations for Automated Test Framework](browser-recommendations-atf.md)**  
Configure client test runner browsers to run automated tests and avoid performance degradations.
-   **[Working with client test runners](atf-test-runners.md)**  
If an automated test includes steps that involve a form or any other user-interface \(UI\) element, it runs those steps in a browser tab or window called a test runner or client test runner.
-   **[Pick a browser](../task/atf-pick-a-browser.md)**  
If the test or test suite you are running contains steps that work with a form \(any step involving a UI\), or any other UI test step element \(such as Automated Service Catalog test steps\), work with the Pick a Browser dialog.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

