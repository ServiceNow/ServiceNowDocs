---
title: Troubleshooting
description: Resolve common issues with the Run UI Test Script step, including reference errors, elements that aren't found, step timeouts, comparison failures, and impersonation failures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_troubleshooting.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [Run UI Test Script, troubleshooting, ATF, timeout]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# Troubleshooting

Resolve common issues with the Run UI Test Script step, including reference errors, elements that aren't found, step timeouts, comparison failures, and impersonation failures.

-   **user.type times out on a Workspace input**

    In certain Workspace \(SOW\) input components, user.type\(\) can stall waiting for network activity that never completes, causing the step to time out. When this occurs, set the field value through the native browser DOM APIs directly. This approach is not part of the ATF testing library — it relies on standard web platform APIs available to any browser-side script — and should be treated as a targeted workaround rather than a general pattern. Prefer user.type\(\) for all other contexts.

    ```
    const input = screen.getByRole('searchbox', { name: 'Caller' });
    await user.click(input);
    
    const nativeSetter = Object.getOwnPropertyDescriptor(
      HTMLInputElement.prototype,
      'value'
    ).set;
    
    nativeSetter.call(input, 'Abel Tuter');
    input.dispatchEvent(
      new InputEvent('input', {
        bubbles: true,
        composed: true,
        inputType: 'insertText',
      })
    );
    input.dispatchEvent(
      new Event('change', { bubbles: true, composed: true })
    );
    
    const host = input.getRootNode?.()?.host;
    if (host) {
      host.dispatchEvent(
        new InputEvent('input', { bubbles: true, composed: true })
      );
      host.dispatchEvent(
        new Event('change', { bubbles: true, composed: true })
      );
    }
    ```

-   **`ReferenceError: X is not defined`**

    When a variable name isn't recognized, the error message lists all available APIs. The most common causes are:

    -   `waitForElementToBeRemoved` — Use `sn_atf.waitForElementToBeRemoved(el)`, not a top-level function.
    -   `fill` — There is no `fill` function. Use `user.type(el, text)`, or `user.clear(el)` and then `user.type(el, text)`.
-   **Element not found**
    -   The element might be inside a shadow root. All `screen.*` queries pierce shadow roots. If the element still isn't found, use `screen.debug()` to inspect the DOM.
    -   The element might not yet exist. Use `findBy*`, which is async and polls, instead of `getBy*`, which is synchronous and throws immediately.
    -   The element might exist but not be visible to the query type. Use `getBySelector` with a CSS selector as a fallback.
-   **Step times out**
    -   The default timeout is 30 seconds. If your test involves slow navigations or network requests, configure a longer timeout on the step record.
    -   A `findBy*` query waits up to 5 seconds by default before failing. Pass `{ timeout: 15000 }` in the second argument to extend it, for example `screen.findByRole('button', { name: 'Save', timeout: 15000 })`. Timeout must go inside the second argument alongside name.
    -   Ensure that all Promises are awaited. An unawaited Promise silently discards its result, and the step might resolve before the action completes.
-   **Comparison with `steps()` or `params()` always fails**

    Use `==` or `String()` for comparisons. See the 'Comparison behavior' section in [Script helper functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/r_run_ui_test_script_helpers.md) for more information.

-   **Impersonation fails**
    -   The ATF runner session requires the `impersonator` role.
    -   Verify that the user identifier, sys\_id or user\_name, is correct. The error message includes the resolved ID.
    -   The step restores the session on exit, including on timeout, so a session that isn't restored after a test failure doesn't occur in practice.

