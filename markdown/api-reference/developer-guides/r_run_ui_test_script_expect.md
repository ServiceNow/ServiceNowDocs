---
title: expect — assertions
description: The expect API makes assertions about elements or values in a Run UI Test Script step. Pass a DOM element for element-specific matchers, or pass any other value for value matchers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_expect.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [expect, assertions, matchers, toBeVisible, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# expect — assertions

The expect API makes assertions about elements or values in a Run UI Test Script step. Pass a DOM element for element-specific matchers, or pass any other value for value matchers.

## Element matchers

```
const [btn] = screen.getAllByRole('button', { name: 'Submit' });
expect(btn).toBeVisible();
expect(btn).toBeEnabled();
expect(btn).not.toBeDisabled();
expect(btn).toHaveTextContent('Submit');
```

|Matcher|Asserts|
|-------|-------|
|`.toBeVisible()`|Element is in the DOM and visible, not hidden by CSS.|
|`.toBeHidden()`|Element isn't visible.|
|`.toBeEnabled()`|Form control isn't disabled.|
|`.toBeDisabled()`|Form control is disabled or has `aria-disabled="true"`.|
|`.toBeChecked()`|Check box or radio is checked.|
|`.toBePartiallyChecked()`|Check box is indeterminate.|
|`.toBeInTheDocument()`|Element exists in the document.|
|`.toBeEmptyDOMElement()`|Element has no child nodes.|
|`.toHaveFocus()`|Element has keyboard focus.|
|`.toHaveTextContent(text)`|Element's text content matches a string or RegExp.|
|`.toHaveValue(value)`|Form control's current value matches.|
|`.toHaveDisplayValue(value)`|Visible label of a `<select>` matches.|
|`.toHaveAttribute(name, value?)`|Element has the attribute, optionally with a specific value.|
|`.toHaveClass(...classes)`|Element has all listed CSS classes.|
|`.toHaveStyle(styles)`|Element has the given inline or computed styles.|
|`.toHaveAccessibleName(name)`|ARIA accessible name matches.|
|`.toHaveAccessibleDescription(desc)`|ARIA accessible description matches.|
|`.toContainElement(child)`|Element contains `child`.|
|`.toHaveRole(role)`|Element has the given ARIA role.|
|`.toHaveFormValues(values)`|Form element's fields match the given value map.|
|`.toBeRequired()`|Form control is required.|
|`.toBeValid()`|Form control passes validation.|
|`.toBeInvalid()`|Form control fails validation.|
|`.toHaveErrorMessage(text?)`|Element has an associated error message.|

## Value matchers

When `expect` receives a non-element value, it delegates to value matchers.

```
expect(2 + 2).toBe(4);
expect({ a: 1 }).toEqual({ a: 1 });
expect([1, 2, 3]).toContain(2);
expect('hello').toMatch(/ell/);
expect(null).toBeNull();
expect(undefined).toBeUndefined();
```

## Polling with expect

`expect` throws synchronously on failure. Combine it with `waitFor` to retry.

```
await waitFor(() => {
  expect(screen.getByRole('status')).toHaveTextContent('Saved');
});
```

