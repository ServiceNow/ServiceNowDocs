---
title: Exploring Lux
description: Lux is a framework for building widget-based UI experiences on a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/exploring-lux.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [Lux, Server-rendered, then hydrated, Built on Lit widgets, What you build with it, Who this is for]
breadcrumb: [Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Exploring Lux

Lux is a framework for building widget-based UI experiences on a ServiceNow instance.

Lux streams the rendered HTML to the browser and hydrates it into a fully interactive single-page app.

Your app is served under `/aiux/<app-basename>/<route>`. The `aiux` prefix is the platform's public URL surface. It also appears in package names such as **@servicenow/aiux-components-core** and in API identifiers such as `AIUXElement`. Those are real names you type in code, and they don't change.

## Faster page loading

When a user navigates to your Lux app they will see fully rendered content immediately, with no loading spinners or blank screens. Subsequent navigation happens client-side, so the app feels like a single-page app.

Lux provides the following benefits:

-   The browser shows the first screen quickly.
-   The markup is accessible and search engines can read it.
-   Data retrieval is efficient. Loaders run on the server, near your ServiceNow instance. This helps prevent the delay of a round trip that client-side fetches cause.

## Built on Lit widgets

You build all Lux UI with Lit widgets. Your widgets extend a platform base class from the package **@servicenow/aiux-components-core**. Use `AIUXElement` for a simpler presentational widget or a page. Never extend `LitElement` directly.

The base classes carry the SSR, styling, and data-fetching plumbing:

-   Tailwind and DaisyUI styling, applied automatically through adopted stylesheets, so your widgets inherit the design system without manual imports.
-   SSR-safe `this.loaderData`, holding the result of your widget's `static async loader(ctx)` method during both server render and client hydration.
-   `getLayoutData(key)`, reading layout-level data shared across all pages.
-   The `static async loader(ctx)` convention, a framework-managed pattern for fetching data before render.

The fundamental building blocks are described in the following table.

|Building block|Description|
|--------------|-----------|
|`aiux.json`|The app manifest: app name, URL basename, landing route|
|Pages|Lit widgets under `pages/`; directory structure maps directly to URLs \(file-based routing\)|
|Loaders|A `static async loader(ctx)` method on a page or widget that fetches data on the server before render; the result becomes `this.loaderData`|
|Widgets|Reusable Lit UI units extending `AIUXWidgetElement` \(discoverable, self-fetching\) or `AIUXElement` \(presentational\)|
|Layout|A single `pages/layout.js` that renders the app chrome \(header, navigation, footer\) around each page|
|Context API|`createContext()` for sharing data across widgets without prop-drilling|

## What you build with it

You build a scoped ServiceNow application that depends on Lux. Your application lives in its own repository, separate from Lux itself. It deploys to a ServiceNow instance on its own schedule using the [ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/now-sdk.md).

## Who this is for

Lux is for developers building custom UI experiences on a ServiceNow instance. You should know JavaScript \(ES modules\) and basic HTML and CSS, plus web components or a component framework. Prior Lit experience helps but isn't required.

