---
title: screen — DOM queries
description: The screen API is the primary interface for finding elements on the page tested by a Run UI Test Script step. All query methods pierce shadow roots automatically, so they work with Now Experience components as well as classic Jelly and UI16 pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_screen.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [screen, DOM queries, getByRole, findByText, shadow DOM, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# screen — DOM queries

The screen API is the primary interface for finding elements on the page tested by a Run UI Test Script step. All query methods pierce shadow roots automatically, so they work with Now Experience components as well as classic Jelly and UI16 pages.

## Query method variants

Each query type comes in the following variants.

|Variant|Returns|Throws when missing?|Async?|
|-------|-------|--------------------|------|
|`getBy*`|Single element|Yes, throws immediately|No|
|`getAllBy*`|Array of elements|Yes, if empty|No|
|`queryBy*`|Single element or `null`|No|No|
|`queryAllBy*`|Array, which may be empty|No|No|
|`findBy*`|Single element|Yes, rejects the Promise|Yes, polls until found|
|`findAllBy*`|Array of elements|Yes, if empty|Yes, polls until found|

Use `findBy*` when the element appears asynchronously, such as after an API response, animation, or navigation. Use `getBy*` when the element must already exist. Use `queryBy*` to check whether an element is absent.

## Query types

Each variant supports the following query types.

|Type|Finds elements by|Example|
|----|-----------------|-------|
|`Role`|ARIA role, implicit or explicit|`screen.getByRole('button', { name: 'Save' })`|
|`Text`|Visible text content|`screen.findByText('Incident created')`|
|`LabelText`|Associated `<label>` text|`screen.getByLabelText('Short description')`|
|`PlaceholderText`|`placeholder` attribute|`screen.getByPlaceholderText('Search…')`|
|`AltText`|`alt` attribute|`screen.getByAltText('Company logo')`|
|`Title`|`title` attribute|`screen.getByTitle('Close dialog')`|
|`TestId`|`data-testid` attribute|`screen.getByTestId('submit-btn')`|
|`DisplayValue`|Current display value of a form control|`screen.getByDisplayValue('High')`|
|`Selector`|CSS selector, shadow-piercing|`screen.getBySelector('input[name="priority"]')`|

`getByRole` is the recommended default because it validates accessibility as it queries. Use `getBySelector` only when no accessible query matches.

## screen.waitFor\(callback, options?\)

Polls `callback` until it stops throwing. Use this method to wait for a condition that isn't directly an element query.

```
await screen.waitFor(() => {
  expect(screen.getByRole('status')).toHaveTextContent('Complete');
});
```

Options: `{ timeout: 5000, interval: 50 }`, in milliseconds.

## screen.debug\(element?\)

Logs the outer HTML of `element`, or the whole page body when omitted, to the browser console, including shadow root contents. Use it when a query doesn't match what you expect.

```
screen.debug(); // log the full page
screen.debug(screen.getByRole('form')); // log a specific subtree
```

## Shadow DOM traversal

All `screen.getBy*`, `screen.findBy*`, and `screen.queryBy*` queries automatically pierce shadow roots. Now Experience components render their content inside shadow roots, which are normally invisible to `document.querySelector`. The ATF testing library traverses these boundaries transparently, so you can query by role or text whether the element is in light DOM or shadow DOM.

`getByRole` resolves accessible names by reading shadow root text content when the host element's own text content is empty, matching the behavior that a screen reader reports.

`getBySelector` uses a custom shadow-piercing CSS selector engine that handles cross-shadow combinators, for example `now-typeahead input`.

