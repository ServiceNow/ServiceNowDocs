---
title: Run the UI Test Script
description: Learn how to use the Run UI Test Script step to navigate to records, fill fields, click buttons, impersonate users, upload attachments, and assert UI state on classic and Now Experience pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [Run UI Test Script, Automated Test Framework, ATF, test step, UI testing]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# Run the UI Test Script

Learn how to use the Run UI Test Script step to navigate to records, fill fields, click buttons, impersonate users, upload attachments, and assert UI state on classic and Now Experience pages.

The test script has access to shadow-DOM-aware query APIs, realistic user-interaction simulation, and utility APIs for navigation, page evaluation, impersonation, and file uploads. For an overview of the step and the scripting APIs, see [Run UI Test Script Developer Guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/c_run_ui_test_script.md). For more examples about how to use the test script, see [UI Test Script examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_examples.md).

## Input fields

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer that specifies the order in which the test runs this step. As you create steps, the system assigns each step an incremental value so that the test runs steps in the order that you create them. To change the default order, edit the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option that activates this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. The system sets this value automatically from the field values of the test step. This field appears after you submit the test step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. The default is 30.

</td></tr><tr><td>

Script

</td><td>

Test body to run. Available APIs:-   `expect` assertions,
-   `screen`: DOM queries such as `getByRole`, `findByText`, and `getBySelector`.
-   `sn_atf`: `navigate`, `evaluate`, `upload`, `impersonate`, `getAttachmentFile`, `querySelector`, `delay`, and `waitForElementToBeRemoved`.
-   `user`: user interactions such as `click`, `type`, `keyboard`, `tab`, and `clear`.
-   Script helpers: `waitFor` \(polling\), `within` \(scoped queries\), `steps` \(prior step outputs\), `params` \(parameter set values\).
-   Element predicates: such as `isVisible`, `isEnabled`, and `hasClass`. Return a Promise or use `async`/`await`.

</td></tr></tbody>
</table>**Note:** The test script runs as an `async` function automatically. All element interactions, such as `user.click()` and `user.type()`, return Promises — use `await`. A synchronous script that doesn't use `await` resolves automatically when the last statement runs.

## Add the step to a test

To add a script to a text:

1.  Open your test record and click **Add test step**.
2.  In the step picker, select the **UI** category and choose **Run UI Test Script**.
3.  Write your script in the **Script** field.
4.  Save the test step.

The step runs inside the browser context of the Client Test Runner. The tested page loads in an iframe, and your script interacts with it through the scripting APIs.

For script test examples, see [UI Test Script examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_examples.md).

