---
title: Writing resilient tests: Query Selection and Debugging
description: Resilient automated tests are built by querying components semantically, through ARIA roles and accessible names, rather than relying on implementation details that teams can change at any time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/writing-reslient-ATF-tests.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# Writing resilient tests: Query Selection and Debugging

Resilient automated tests are built by querying components semantically, through ARIA roles and accessible names, rather than relying on implementation details that teams can change at any time.

## Building Resilient Test Queries

The foundation of reliable automated testing rests on a single principle: query your components the way users interact with them, not the way they're built internally.

When you select elements using ARIA roles and accessible names, through queries like `getByRole` and `getByLabelText`, your tests reflect the semantic contract of the component. This approach proved invaluable in a recent case where the SoW team restructured the DOM of a critical component. Tests written against role-based queries continued to pass seamlessly, while tests relying on CSS selectors and internal element IDs shattered immediately. The difference was striking: semantic queries stayed resilient through refactoring, while implementation-dependent queries became brittle.

Recommended query hierarchy:

-   Start with `getByRole` and `getByLabelText` as your primary tools. These queries prioritize accessibility and semantic meaning, ensuring your tests validate what users actually experience.
-   Only reach for `getBySelector` when no accessible query satisfies your needs. Document why the accessible option wasn't viable.
-   Avoid anchoring tests to element IDs, generated class names, or deeply nested CSS paths. Component teams can refactor these implementation details without warning, leaving your tests fragile and your test suite unmaintainable.

## Handling Asynchronous Content

Automated tests must account for the reality of modern interfaces: content doesn't always appear immediately. After navigation events, API calls, or animations complete, elements enter the DOM asynchronously. In these cases, `findBy*` queries \(such as `findByRole`\) are essential. They poll the DOM at intervals until the element appears or the timeout expires—a far more reliable approach than `getBy*`, which throws an exception immediately if the element isn't found on the first check.

## Debugging Failed Queries

When a query doesn't match what you expected, start with screen.debug\(\). This method outputs the complete live DOM of the tested page directly to your browser console, including shadow root contents. You're seeing the actual markup your query runs against, an invaluable reference point for diagnosis.

For scenarios where you need to inspect computed values or execute code in the page context, use `sn_atf.evaluate(() => ...)`. This function runs arbitrary JavaScript inside the tested iframe and returns the result, giving you direct access to component state and runtime values.

When async failures occur, wrap your assertion in `waitFor` with an extended timeout and monitor the console for intermediate states. This technique isolates timing issues and reveals whether content is appearing later than expected or not appearing at all. Combined with screen.debug\(\) calls at key moments, you can identify the root cause and adjust your test accordingly.

