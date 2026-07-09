---
title: Element predicates
description: Element predicates are synchronous Boolean checks available in a Run UI Test Script step. Use them inside .find\(\) or .filter\(\) callbacks to pick one element from a list based on its state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_predicates.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [element predicates, isVisible, isEnabled, hasClass, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# Element predicates

Element predicates are synchronous Boolean checks available in a Run UI Test Script step. Use them inside .find\(\) or .filter\(\) callbacks to pick one element from a list based on its state.

## Element predicates

These functions return `true` or `false` synchronously.

```
// Find the first visible element with the text "Number"
const labels = await screen.findAllByText(/^Number$/);
const visible = labels.find(el => isVisible(el));
```

|Predicate|Tests|
|---------|-----|
|isVisible\(el\)|Element is visible.|
|isHidden\(el\)|Element isn't visible.|
|isEnabled\(el\)|Form control is enabled.|
|isDisabled\(el\)|Form control is disabled or has `aria-disabled="true"`.|
|isChecked\(el\)|Check box or radio is checked.|
|isPartiallyChecked\(el\)|Check box is indeterminate.|
|isInDocument\(el\)|Element is connected to the document.|
|isEmpty\(el\)|Element has no child nodes.|
|hasFocus\(el\)|Element has keyboard focus.|
|hasClass\(el, ...classes\)|Element has all listed CSS classes.|
|hasAttribute\(el, name, value?\)|Element has the attribute, optionally with a value.|
|hasText\(el, text\)|Element's text content matches.|
|hasValue\(el, value\)|Form control's current value matches.|
|hasFormValues\(el, values\)|Form's field values match the given map.|
|hasRole\(el, role\)|Element has the given ARIA role.|
|hasStyle\(el, styles\)|Element has the given styles.|
|hasAccessibleName\(el, name\)|ARIA accessible name matches.|
|hasAccessibleDescription\(el, desc\)|ARIA accessible description matches.|
|containsElement\(el, child\)|`el` contains `child`.|

