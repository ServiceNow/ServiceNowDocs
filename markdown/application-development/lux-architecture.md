---
title: Lux architecture
description: Lux renders UI as a separate service in front of a ServiceNow instance. It builds pages, sends HTML to the browser, and calls back for data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/lux-architecture.html
release: zurich
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 6
keywords: [Lux architecture, Request pipeline, Server rendering, then hydration, Built on Lit widgets, Subsystem map, Where an app runs]
breadcrumb: [Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Lux architecture

Lux renders UI as a separate service in front of a ServiceNow instance. It builds pages, sends HTML to the browser, and calls back for data.

This architectural split shapes everything else about how a Lux app behaves.

## Request pipeline

A request to a Lux app passes through four layers before a response reaches the browser. Each layer has one job: routing, version selection, rendering, and data fetching.

-   **HTTP proxy, port 80**

    Entry point for every request, and a plain Node.js HTTP server. It matches the incoming URL against the `/aiux` gateway basename, strips the prefix, injects authentication and forwarding headers, and then forwards the request to the version router. Anything that doesn't start with `/aiux` is proxied straight through to the ServiceNow instance, so Lux intercepts only its own traffic.

-   **Version router, port 3000**

    Decides which running version of the rendering service handles the request. Requests to `/aiux/*` go to the current version \(vN, port 3001\), and requests to `/aiux-1/*` go to the previous version \(vN-1, port 3002\). If a version is unavailable, the router falls back to vN. It adds an `x-aiux-version` response header, so you can tell which version answered.

-   **Rendering service, ports 3001 and 3002**

    One Fastify service per live version. For a page request it creates a request context and resolves the route to a page widget. It then runs every loader in the tree \(the page's, its layout's, and any widgets it contains\) in parallel rather than one after another. Finally it server-renders the Lit widgets to an HTML string and streams that string back.

-   **ServiceNow instance, port 8080 or a remote host**

    Target of the data calls a page makes. Loaders call back into the instance over REST, GraphQL, and Table API endpoints to fetch the data a page needs. Those calls are authenticated as the logged-in user. The rendering service forwards that user's session cookie and cross-site request forgery \(CSRF\) token rather than using a separate service credential.

    **Note:**

    Basename matching order. The gateway basenames are a fixed, ordered list: `/aiux-1`, `/aiux-2`, `/aiux`. The first match wins. Bare `/aiux` has to stay last, or it shadows the versioned prefixes. Three basenames are matched; two version tiers run.

    Running loaders concurrently instead of sequentially is a deliberate performance choice. A page pulling from several different ServiceNow APIs fires all of those calls at once instead of waiting on each in turn. The results are serialized into the HTML, so the browser doesn't re-fetch them on first paint.

    Loaders don't get the raw request to do this, though. They receive a filtered, loader-safe context exposing only what they need.


## How Lux renders pages

Lux builds pages on the server first, then adds browser behavior second.

When a user opens a Lux app, the framework does the following:

1.  It runs your data-fetching code on the server.
2.  It builds the UI as an HTML string.
3.  It streams the HTML to the browser.

The user sees the full content immediately. No blank screen or loading spinner shows while JavaScript downloads.

After the HTML arrives, the browser downloads the JavaScript bundles. Then the JavaScript makes the page interactive. It adds event listeners and reactive behavior to the page elements that already exist. It does not build these elements again.

After this step, the page works like a single-page app. The browser does later navigation on the client. It does not reload the full page.

This method gives these measurable benefits:

-   Content appears fast. The browser does not wait for JavaScript to show content.
-   The first HTML contains real content, not an empty shell. This helps search engines and assistive technology.
-   Data fetching happens on the server, close to the ServiceNow instance. The browser does not make extra round trips.

An experience can declare resource hints in `aiux.json`, under `experienceProperties.resourceHints`. The hints apply to every page of the experience. Lux resolves the hints before it builds the head HTML of the response.

The `render()` output of each widget must be the same on the server and on the client. For this reason, the contract is stricter than the contract of a client-only UI framework. The `render()` function must be pure and deterministic. It must not use browser globals, such as `window` or `document`, unless a guard checks for the server environment first.

For more about this contract, and for where side effects are allowed, refer to [Core concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/core-concepts.md)

## Built on Lit widgets

All UI in Lux is built with Lit, which provides web components with Shadow DOM. You don't extend Lit's base class directly. You extend a Lux base class that layers SSR support, styling, and data fetching on top of Lit.

**Warning:**

Two copies of Lit break hydration. Lit is externalized into a single `lit-core` bundle loaded through an import map. If your app bundles its own copy, hydration and `instanceof` checks break. In a non-core component package, list `lit` as a `peerDependency`, not a `dependency`.

## Lux building blocks

A handful of concepts recur throughout a Lux app. The following table names each one.

|Concept|What it is|
|-------|----------|
|App manifest \(`aiux.json`\)|Declares an app's name, its URL basename, and its landing route.|
|Pages|Lit widgets under a `pages/` directory. The directory structure maps directly to URLs, so routing follows file layout rather than a separate route table.|
|Loaders|`static async loader(ctx)` methods that fetch data on the server before a page or widget renders. A loader's return value is available on the widget as `this.loaderData`.|
|Widgets|Reusable UI units, either self-fetching and independently discoverable or purely presentational, depending on which base class they extend.|
|Layout|`pages/layout.js`, the single file that renders the shared app chrome \(header, navigation, footer\) around every page.|
|Context API|Shares data between widgets without passing it down through props at every level.|

Each of these gets its own treatment in [Core concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/core-concepts.md).

## Subsystem map

Beyond the request pipeline, the framework groups into a handful of subsystems. You rarely touch them directly, but their vocabulary shows up in error messages. The following table describes what each subsystem covers.

|Subsystem|Responsibility|
|---------|--------------|
|Rendering and SSR|`@lit-labs/ssr` rendering, hydration, streaming, and the isolate pool that runs untrusted widget code.|
|Routing and navigation|File-based route resolution, the client-side router, prefetch and hover-prefetch, navigation guards.|
|Data and state|Loaders, the Context API, batch fetch, caching, and dirty-state tracking.|
|Local development|The dev proxy, the widget dev server, hot reload, and the command-line interface \(CLI\).|
|Build and bundling|Rollup and SWC pipelines that emit separate SSR and browser builds, with Lit externalized into a single `lit-core` bundle.|
|Observability|Structured backend logging, browser log forwarding, tracing, and server timing.|
|Advanced UI|Modal teleporting, side panels, the window manager, page alerts, and layout overrides.|

## Where a Lux app runs

The pipeline you develop against locally is the same pipeline that runs in production: proxy, version router, rendering service, and calls back to a ServiceNow instance. That is what makes local behavior a reliable predictor of production behavior.

In production, that pipeline is a cloud deployment sitting in front of many ServiceNow instances rather than something deployed per instance. When someone navigates to `/aiux/*` on their ServiceNow instance, the request is proxied to the Lux deployment. The deployment identifies the tenant from the hostname, runs loaders against that tenant's instance APIs with the user's session, and streams the HTML back.

This shared deployment model has a consequence worth knowing at the architecture level. Because one deployment serves many tenants at once, it has to stay compatible with every ServiceNow version still in use, not just the newest one.

For how the files behind these concepts are laid out in a project \(`aiux.json`, `pages/`, the layout, widgets\), see [Project structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/project-structure.md).

