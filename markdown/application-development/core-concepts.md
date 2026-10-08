---
title: Core concepts
description: Lux apps use six core building blocks to create consistent, maintainable applications: a manifest, pages, loaders, widgets, a layout, and a context API for sharing data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/core-concepts.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 6
keywords: [Core concepts, Core building blocks, Coordination mechanisms, Region DSL, How it all renders]
breadcrumb: [Lux architecture, Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Core concepts

Lux apps use six core building blocks to create consistent, maintainable applications: a manifest, pages, loaders, widgets, a layout, and a context API for sharing data.

This topic introduces each piece and how they relate. For the request lifecycle that ties them together \(proxy, routing, server rendering, hydration\), see [Lux architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/lux-architecture.md). For step-by-step instructions on building with each concept, see the topics on creating pages, widgets, and components.

## Core building blocks

-   **App manifest, `aiux.json`**

    Declares your app's name, its URL basename, and its landing route. The framework reads it to serve your app under `/aiux/<basename>/<route>` and to determine which page to show first.

-   **Page**

    A Lit widget that lives under your app's `pages/` directory. The directory structure maps directly to URLs through file-based routing, so `pages/inventory/page.js` serves `/inventory` and `pages/inventory/[id]/page.js` serves `/inventory/:id`. A page is the default export of its `page.js`. Pages extend AIUXElement, the same base class reusable components extend, so a page is really just a component that the router can address directly.

-   **Loader**

    A static async loader\(ctx\) method on a page or widget. It runs on the server before the component renders and fetches whatever data the component needs. Its return value becomes available on the component as *this.loaderData*. Because loaders run on the server, they fetch data close to your ServiceNow instance rather than over a client round trip.

-   **Widget**

    A reusable Lit UI unit. Widgets extend one of two base classes from `@servicenow/aiux-components-core`. Use AIUXWidgetElement for a discoverable widget that owns its own data, or AIUXElement for a presentational widget that takes its data through properties. Neither extends LitElement directly. The Lux base classes add Tailwind and DaisyUI styling, *this.loaderData*, and getLayoutData\(key\) for reading layout-level data.

-   **Layout**

    A single file, `pages/layout.js`, that renders the app chrome \(header, navigation, footer\) around every page. It extends NavLayout, itself an AIUXAppLayoutElement, and is not itself a page. It's the persistent shell every page renders inside, and it is not re-created when the user navigates from one route to another. The layout is also where an app declares its navigation tree \(`l1Nav`, with nested `l2Nav` and `l3Nav`\). That tree determines both the sidebar and the tab structure pages appear under.

-   **Context API**

    A mechanism for sharing data between components without prop drilling. Use createContext\(\) to establish a context that parent components can provide and child components can consume, enabling state management across the component tree.


## Coordination mechanisms

Beyond this core spine, more mechanisms come up as an app grows. Widgets may need to coordinate with each other, to coordinate with the platform's AI chat, or to sit in a layout an admin can rearrange.

-   **Widget-to-chat protocol**

    How a page participates in a two-way exchange with the ServiceNow Otto chat backend. Widgets push their current state to the AI through `setAiContext()`, and the AI can invoke actions on a widget in response to what the user asks it.

-   **Region DSL**

    The `region` tagged template, imported from `@servicenow/aiux-components-core`. It's a constrained, HTML-like domain-specific language \(DSL\) for arranging widgets inside a page, deliberately restricted to a known set of layout primitives \(`row`, `column`, `raw`\) and widget tags. Arbitrary HTML, `class` and `style` attributes, event bindings, directives, and text children are all rejected at parse time. The restriction is what lets a visual editor parse, manipulate, and serialize a layout programmatically. A stored region has to be expressible as a value in a database column and a field in a property panel.

    The admin-facing region editor lets a configuration admin restructure a rendered page's regions: add and remove rows, columns, and widgets, resize column spans, move containers. The editor saves the result as an override row in `sys_aix_page_region`. A page whose regions have never been overridden has no row at all. The renderer records the code-authored structure so the editor has something to open.


## Where a region lives and what it renders

A region is not written inline in a page's render\(\). It lives in its own file under `<projectRoot>/regions/`, and that file's default export is a thunk that takes no arguments and returns the tagged template. The region's name comes from its file path. The page imports the thunk and calls it once per render. That call is what lets the runtime read the current request's stored overrides instead of a snapshot taken when the module loaded. Importing `region` anywhere outside `regions/` fails the build, and so does a function that takes arguments.

Every rendered region is enclosed in exactly one wrapper element, `<div data-aiux-region="{name}" class="flex flex-col gap-layout overflow-hidden">`. That wrapper is part of the rendered-output contract, so anything that needs to find a region in the DOM queries `data-aiux-region` as a literal. The renderer's constants aren't exported. The wrapper is a real layout box. It stacks the region's top-level rows as a flex column on `gap-layout`, the same theme-able gutter a `row` puts between its columns. So two top-level rows sit exactly one gutter apart. The consequence for the page is that a region is one item of the page's own grid or flex parent, rather than each of its rows being one.

A region has one spacing value and no padding. The `gap` and `padding` attributes are deprecated. They are still parsed, so they never reach the rendered element, and they are ignored on any tag with any value. Retune the gutter with the `--layout-gap` custom property at `:root`, or `--spacing-layout` on an ancestor to scope one subtree.

**Important:**

A widget is a leaf. A widget in a region holds no children. An element inside one throws at parse time, and text children are rejected outright. `<slot>` is a blocked tag, because a slot projects the host element's light DOM and a region doesn't own that. `<raw>` is not the workaround: it emits whatever markup it is given, widget tags included, but its content is unsanitized trusted-input-only markup. A widget nested that way is invisible to both the editor and the structural rules. Composition hosts \(`aiux-layout-host`\) were removed outright. To compose one widget inside another, write plain Lit `html` with Tailwind classes. For more information about widgets, see [Lux Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/widgets.md).

## How it all renders

All of this UI is built with Lit and styled with Tailwind and DaisyUI, applied automatically through adopted stylesheets, so you don't import styles manually. Every page and widget renders on both the server, for first paint, and the client, during hydration and on later re-renders. So `render()` must be pure: same input, same output, every time. For what drives that server and client split, see [Lux architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/lux-architecture.md).

