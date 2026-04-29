---
title: Properties
description: On the Properties form, you can set parameters that control how the system executes automated tests and test suites.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administration, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Properties

On the Properties form, you can set parameters that control how the system executes automated tests and test suites.

<table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable test/test suite execution

 **sn\_atf.runner.enabled**

</td><td>

If checked, enables running tests and test suites on this instance. This setting is unchecked by default to prevent users from unintentionally running tests on production instances.

</td></tr><tr><td>

Enable scheduled test suite execution

 sn\_atf.schedule.enabled

</td><td>

If checked, enables scheduling test suites on this instance.

</td></tr></tbody>
</table><table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable additional debugging functionality

 **sn\_atf.debug**

</td><td>

Enables additional debugging functionality, including adding a debugging tab on the client Test Runner UI page and saving UI Test Result JSON to the test result record.

</td></tr></tbody>
</table><table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable or disable screenshot capture during test execution.

 **sn\_atf.screenshots.mode**

 **Note:** For additional information, see [Set the system property to control when the Automated Test Framework captures screenshots](../concept/atf-screenshot-modes.md#)

</td><td>

-   To capture screenshots for all steps, select **Enable for all steps**.
-   To capture screenshots only for failed steps, select **Enable for all failed steps**.
-   To capture no screenshots, select **Disable for all steps**.

</td></tr><tr><td>

Enable the GlideScreenshot feature

 **sn\_atf.screenshots.use\_glide\_screenshot**

</td><td>

Improves the fidelity of screenshots on Workspaces and other interfaces.**Note:** IE and Safari don't support this property.

If this property is disabled or your current browser doesn't support it, html2canvas is used to take screenshots.

If you are upgrading to a new release version, this property is set to false by default.

</td></tr><tr><td>

Enable capturing the full page when taking a screenshot

 **sn\_atf.screenshots.capture\_full\_page**

</td><td>

Enables dynamic resizing of the test frame and capturing the full page while taking a screenshot.**Note:** By default, the property is set to false because it can significantly slow test execution time

If the property is disabled, only the portion of the page that is visible in the test frame is captured.

</td></tr><tr><td>

Screenshot timeout

 **sn\_atf.atf\_test\_runner.screenshot\_timeout**

</td><td>

Skips a screenshot capture attempt in the Client Test Runner if it exceeds this value in seconds. Users should review performance settings and browser caches on affected client systems before increasing this value.

</td></tr><tr><td>

Number of pixels for screenshot height

 **sn\_atf.atf\_test\_runner.testframe.min\_height**

</td><td>

Numeric value representing the number of pixels for the screenshot height.

 Default value: 600

</td></tr><tr><td>

Number of pixels for screenshot width

 **sn\_atf.atf\_test\_runner.testframe.min\_width**

</td><td>

Numeric value representing the number of pixels for the screenshot width.

 Default value: 800

</td></tr></tbody>
</table><table id="table_op4_f5n_5fb"><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable tests with Custom UI steps to capture page data each time they are run.

 **sn\_atf.page\_data\_capture.enabled**

</td><td>

When true, Custom UI test steps retrieve page data every time the test runs. Set this property to true when developing custom UI pages to always run tests on the most recent page version.

When false, Custom UI test steps do not retrieve page data unless the test designer manually selects **Retrieve Components** during test design. Set this property to false when UI development is complete to enable faster test runs.

</td></tr></tbody>
</table><table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test runner timeout

 **sn\_atf.runner.heartbeat.timeout**

</td><td>

If there is no heartbeat from the test runner within this period of time in seconds, the status changes from online to offline. The value of this property should be between 120 and 1800.

 Default value: 120

</td></tr><tr><td>

Test runner heartbeat interval

 **sn\_atf.runner.heartbeat.interval**

</td><td>

Time interval in seconds for sending a heartbeat from the test runner to the server.

</td></tr><tr><td>

Offline test runner retention interval

 **sn\_atf.runner.offline\_retention.timeout**

</td><td>

If an offline test runner does not communicate with the system for this period of days, the system deletes that test runner.

</td></tr></tbody>
</table><table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test suite report properties

 **sn\_atf.schedule.reports.suite.aging\_threshold**

</td><td>

The number of test suite results to display in the test suite aging report.

</td></tr></tbody>
</table><table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean value for results displayed in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.only\_show\_failed\_results**

</td><td>

When true, the scheduled suite test result emails only show results that failed. When false, displays all results.

</td></tr><tr><td>

Maximum number of test results to be displayed in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.max\_test\_history**

</td><td>

Maximum number of test results to be displayed in scheduled suite result emails.

</td></tr><tr><td>

Maximum depth when printing suite results in suite result emails.

 **sn\_atf.schedule.suite\_result\_email.max\_depth**

</td><td>

Maximum depth when printing suite results in suite result emails.

</td></tr><tr><td>

Color to indicate an ATF test failed in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.fail\_color**

</td><td>

Hexadecimal code for color to indicate an ATF test failed in scheduled suite result emails.

</td></tr><tr><td>

Color to indicate an ATF test errored in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.error\_color**

</td><td>

Hexadecimal code for color to indicate an ATF test errored in scheduled suite result emails.

</td></tr><tr><td>

Color to indicate an ATF test passed in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.pass\_color**

</td><td>

Hexadecimal code for color to indicate an ATF test passed in scheduled suite result emails.

</td></tr><tr><td>

Color to indicate an ATF test was skipped in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.skip\_color**

</td><td>

Hexadecimal code for color to indicate an ATF test was skipped in scheduled suite result emails.

</td></tr><tr><td>

Color to indicate an ATF test was canceled in scheduled suite result emails.

 **sn\_atf.schedule.suite\_result\_email.cancel\_color**

</td><td>

Hexadecimal code for color to indicate an ATF test was canceled in scheduled suite result emails.

</td></tr></tbody>
</table>**Parent Topic:**[Administration](atf-test-admin-module.md)

