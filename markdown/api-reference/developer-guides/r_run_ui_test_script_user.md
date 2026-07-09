---
title: user — user interactions
description: The user API simulates realistic user interactions in a Run UI Test Script step. Each interaction fires the same events a real browser user produces, such as focus, input, change, blur, and keyboard events, so that client scripts and reactive frameworks respond correctly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_user.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [user, user interactions, click, type, keyboard, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# user — user interactions

The user API simulates realistic user interactions in a Run UI Test Script step. Each interaction fires the same events a real browser user produces, such as focus, input, change, blur, and keyboard events, so that client scripts and reactive frameworks respond correctly.

## user methods

|Method|Description|
|------|-----------|
|user.click\(el\)|Single click.|
|user.dblClick\(el\)|Double click.|
|user.tripleClick\(el\)|Triple click, which selects all text in an input.|
|user.hover\(el\)|Move the pointer over the element.|
|user.unhover\(el\)|Move the pointer away from the element.|
|user.type\(el, text\)|Type text character by character, firing key events.|
|user.keyboard\(seq\)|Send a key sequence, for example `'{Enter}'`, `'{Tab}'`, or `'{Control>}a{/Control}'`.|
|user.tab\(opts?\)|Press Tab, or Shift+Tab with `{ shift: true }`.|
|user.clear\(el\)|Select all and delete the current value.|
|user.selectOptions\(el, values\)|Select one or more `<option>` values in a `<select>`.|
|user.deselectOptions\(el, values\)|Deselect options in a multi-select.|
|user.copy\(\)|Copy the selection to the clipboard.|
|user.cut\(\)|Cut the selection to the clipboard.|
|user.paste\(\)|Paste from the clipboard.|

## Usage

All `user.*` methods return Promises — always `await` them.

```
const field = screen.getByRole('textbox', { name: 'Short description' });
await user.click(field);
await user.type(field, 'Cannot connect to VPN');
```

`user.type` fires `keydown`, `keypress`, `input`, and `keyup` for each character. Use it when keystroke-level events matter. For long strings where only the final value matters, use the `user.clear` and `user.type` pattern

