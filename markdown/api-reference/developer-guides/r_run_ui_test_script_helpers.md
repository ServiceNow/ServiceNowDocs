---
title: Script helper functions
description: A Run UI Test Script step provides 4 global helper functions for polling, scoping queries, and reading data from other parts of the test: waitFor, within, steps, and params.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_helpers.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [waitFor, within, steps, params, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# Script helper functions

A Run UI Test Script step provides 4 global helper functions for polling, scoping queries, and reading data from other parts of the test: `waitFor`, `within`, `steps`, and `params`.

## waitFor\(callback, options?\)

waitFor\(\) polls `callback` repeatedly until it stops throwing. Use this function for conditions that aren't expressible as a single `findBy*` query.

```
await waitFor(
  () => expect(screen.getByRole('progressbar')).not.toBeInTheDocument(),
  { timeout: 10000, interval: 200 }
);
```

|Option|Default|Description|
|------|-------|-----------|
|`timeout`|5000 ms|Maximum time to wait.|
|`interval`|50 ms|How often to retry.|

**Note:**

`screen.waitFor` and the top-level `waitFor` are the same function.

## within\(element\) — scoped queries

within\(\) scopes all queries to a subtree. Use it to disambiguate when the same text or role appears multiple times on the page.

```
const form = screen.getBySelector('form');
const submitBtn = within(form).getByRole('button', { name: 'Submit' });
await user.click(submitBtn);
```

## steps\(stepSysId\) — access prior step outputs

steps\(\) reads output variables from a previously run step in the same test. The argument is the sys\_id of the step record, not the step result.

```
// Read a flat output value
const incidentSysId = String(steps('abc123def456...').record_sys_id);

// Dotwalk through a reference field
const deptName = String(steps('abc123def456...').assigned_to.department.name);
```

Behavior notes:

-   Returns a lazy Proxy. No network call is made until the value is coerced to a string, through a template literal, `==`, `String()`, or string concatenation.
-   Use `==` rather than `===` for comparisons. Strict `===` against a string literal doesn't match the Proxy object.
-   Returns an empty string for unknown step IDs or unresolvable dotwalk paths.
-   Resolves dotwalked, multi-segment paths through a synchronous server call on first access.

**Note:** `steps(SYS_ID)` takes the sys\_id of the step record, not the step result. Find it in the URL when you open the step record.

## params\(paramName\) — parameter set values

params\(\) reads a parameter value from the active parameter set when the test runs with a **Test Data — Parameter Set** entry.

```
// Read a simple parameter
const username = String(params('username'));

// Dotwalk through a reference field on the parameter value
const deptName = String(params('assigned_to').department.name);
```

Behavior notes:

-   Returns a lazy Proxy, with the same lazy resolution and caching behavior as `steps()`.
-   Returns an empty string \(`''`\) when the test isn't parameterized or the named parameter doesn't exist.
-   Use `==` rather than `===` for comparisons.

## Comparison behavior with steps\(\) and params\(\)

steps\(\) and params\(\) return ES6 Proxy objects, not plain strings. Coercing them to a string works correctly, through template literals, `==`, or `String()`, but strict equality \(`===`\) against a string literal is always `false`. This behavior is similar to the server-side `GlideElement`.

```
// Correct
if (String(steps('abc').state) === '1') { … }
if (steps('abc').state == '1') { … }
const val = `${steps('abc').state}`;

// Does not work as expected
if (steps('abc').state === '1') { … } // always false
```

