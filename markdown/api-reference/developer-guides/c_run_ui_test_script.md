---
title: Run UI Test Script Developer Guide
description: The Run UI Test Script test step runs a client-side test script in the browser to drive and verify the user interface with no server-side execution needed. Use this step to automate multi-step UI journeys on both classic and Now Experience pages, like navigating, filling fields, clicking, impersonating users, uploading attachments, and asserting page state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/c\_run\_ui\_test\_script.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 4
keywords: [Run UI Test Script, Automated Test Framework, ATF, UI testing, client-side test script]
breadcrumb: [Developer guides, API implementation and reference]
---

# Run UI Test Script Developer Guide

The Run UI Test Script test step runs a client-side test script in the browser to drive and verify the user interface with no server-side execution needed. Use this step to automate multi-step UI journeys on both classic and Now Experience pages, like navigating, filling fields, clicking, impersonating users, uploading attachments, and asserting page state.

The Run UI Test Script step is an Automated Test Framework \(ATF\) test step that runs a JavaScript test script entirely in the browser, with no server-side execution. The script drives the tested page and verifies its state through a set of browser-side APIs: shadow-DOM-aware element queries, realistic user-interaction simulation, and utilities for navigation, page evaluation, impersonation, and file uploads. The tested page loads in an iframe inside the Client Test Runner, and the script interacts with it through these APIs.

## Release availability

The Run UI Test Script step is available only on ZP10/ AP3 releases and higher.

## Who uses this step

Test authors, QA engineers, and developers who build automated UI tests use the Run UI Test Script step when the built-in, low-code ATF UI steps don't cover a scenario. The step gives a script full programmatic control of the page, so it suits teams that need to test Now Experience or UI Builder components, validate multi-step user journeys, or assert detailed UI state that the built-in steps don't expose.

## When to use this step

Use the Run UI Test Script step to do any of the following:

-   Verify UI state after user actions, such as field values, element visibility, and disabled state.
-   Simulate realistic user interactions, such as clicks, typing, keyboard shortcuts, and tab order.
-   Navigate between pages and assert state across navigations.
-   Test Now Experience components whose DOM lives inside shadow roots.
-   Upload attachments to classic forms, Service Portal, workspaces, or catalog variables.
-   Impersonate a different user and verify what they see.

This step applies to UI journeys that span multiple user actions. For simpler assertions about page state after a built-in step, consider the built-in **Verify field value** or **Assert current page** steps first. For example, confirming that a record opened.

## How scripts work

Scripts run as an `async` function so you can use `await` anywhere. A synchronous script, such as one with no `return` or `await`, resolves automatically when the last statement runs. An async script must return a Promise. The `async` wrapper is applied automatically; `await` works without any extra boilerplate.

```
// Click a button and verify the resulting state
const [btn] = await screen.findAllByRole('button', { name: 'Submit' });
await user.click(btn);
await screen.findByText('Record saved');
```

The step timeout defaults to 30 seconds. An explicit `step.timeout` value on the step record overrides the default. When a timeout occurs, the step fails with `Test timed out after Nms`.

The internal DOM structure of ServiceNow pages and components can change between releases. A UI test script that passes in one release may fail in a later release if a component is restructured, even if the visible UI looks identical. You may need to update scripts to reflect changes made in the underlying DOM.

## Scripting APIs

The test step has access to the following global APIs. Each has its own reference topic.

-   [screen — DOM queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_screen.md) — find elements on the tested page with shadow-DOM-aware queries.
-   [user — user interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_user.md) — simulate realistic user interactions, such as clicks, typing, and keyboard input.
-   [sn\_atf — utility APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_sn_atf.md) — navigate, evaluate code in the page, impersonate users, upload attachments, and use shadow-DOM utilities.
-   [expect — assertions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_expect.md) — assert element and value conditions.
-   [Script helper functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_helpers.md) — `waitFor`, `within`, `steps`, and `params`.
-   [Element predicates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_predicates.md) — synchronous Boolean checks such as `isVisible` and `isEnabled`.

For end-to-end scripts, see [UI Test Script examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_examples.md). For common issues, see [Troubleshooting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_troubleshooting.md).

## Shadow DOM support

Now Experience components render their content inside shadow roots, which are normally invisible to `document.querySelector`. All `screen` queries traverse these boundaries transparently, so you can query by role or text whether the element is in light DOM or shadow DOM. This makes the step suitable for testing modern ServiceNow interfaces as well as classic Jelly and UI16 pages.

