---
title: Lux Widgets
description: A widget in Lux is a custom UI unit authored for a specific application. The platform ships no widgets; every widget on an instance was authored for an app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/widgets.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [Widgets, Project shape, Choosing a base class, The extends chain may be transitive, Discoverability, Metadata decorators, requiresPageType, Resolving a widget at runtime, See also]
breadcrumb: [Build with Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Lux Widgets

A widget in Lux is a custom UI unit authored for a specific application. The platform ships no widgets; every widget on an instance was authored for an app.

This topic covers what a widget is, how it gets registered, and how the runtime resolves one by tag name. To learn how to build a Lux widget, see .

Everything you render in a Lux app is a Lit widget. A Lux widget is a Lit custom element, registered as a `sys_aix_widget` record, extending one of two platform base classes. Both give it Tailwind/DaisyUI styling, and server-side rendering \(SSR\) safety; the difference is discoverability and how it gets its data.

## Project shape

```
my-widget/
                ├── aiux.json              # { "basename": "my-widget", "scope": "x_demo_widget", "scopeId": "…" }
                ├── now.config.json
                ├── package.json
                └── widgets/
                ├── _shared/           # NOT a widget (no index.js): discovery skips it
                │   └── chart.js
                ├── weather/
                │   └── index.js       # <x-demo-weather>
                └── air-quality/
                └── index.js       # <x-demo-air-quality>
```

Discovery convention: each sub directory of `widgets/` that contains an `index.{js,ts}` is one widget. Sub directories without an index entry \(helpers, fixtures, shared modules like `_shared/`\) are ignored silently, with no warning. Widgets and pages coexist: a project can contain only `widgets/`, only `pages/`, or both, and the build discovers whatever is present.

## Choosing a base class

`AIUXWidgetElement` extends `AIUXElement`: it's a superset, so the real question is whether the widget needs what the superset adds. The choice affects runtime capabilities, not how the file builds: both go through the same discovery, analysis, and bundling pipeline.

|Base class|Use it for|Adds|
|----------|----------|----|
|`AIUXElement`|A presentational widget that receives its data through `@property` from a parent, or a page; every `pages/<route>/page.js` extends `AIUXElement`|Tailwind + DaisyUI styling, `this.loaderData`, `getLayoutData(key)`, the `static async loader(ctx)` convention, `this.server`, and `trackEvent()` telemetry|
|`AIUXWidgetElement`|A discoverable, self-contained widget that owns its data; the platform can register it and the AI can place it|Everything `AIUXElement` has, plus a reactive `this.data` populated by `this.server`'s result, dependency injection through `this.deps`, and chat context through `setAiContext()`|

**Note:** `this.server` and `trackEvent()` live on the shared `AIUXElement` base and are available either way. `AIUXWidgetElement` is what makes `this.server`'s result land in a reactive `this.data`. Reach for `AIUXWidgetElement` when you need that reactive property, not to get `this.server` itself.

Start with `AIUXElement`. Reach for `AIUXWidgetElement` only when the widget genuinely needs to be a discoverable, self-fetching unit; because it's a superset, you can upgrade later without rewriting render logic. Pages are always `AIUXElement`. Never extend `LitElement` directly; that loses the automatic styling, `loaderData`/`data`, and the loader and server-script conventions.

