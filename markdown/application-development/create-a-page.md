---
title: Create a page
description: Add a page to a Lux app. A page is a Lit web component that Lux registers as a route based on where you put its file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-a-page.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [Create a page, Goal, Prerequisites, Verify, See also]
breadcrumb: [Build with Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Create a page

Add a page to a Lux app. A page is a Lit web component that Lux registers as a route based on where you put its file.

## Before you begin

-   Role required: admin
-   A scaffolded Lux app \(see the getting-started topic for your app; out of scope here\). You need an existing `pages/` directory and a working `pnpm build`/dev server setup.
-   Familiarity with Lit \(`html`, `customElement`, reactive properties\).

## About this task

Create a working page that renders at a URL in your app, optionally fetching data on the server before it renders.

## Procedure

1.  Create a directory under `pages/`

    Lux uses file-based routing: the directory path under `pages/` becomes the URL path. Create one directory per route segment.

    ```
    mkdir -p pages/risk
    ```

    A nested path becomes a nested route:

    ```
    mkdir -p pages/settings/preferences
    ```

    `pages/settings/preferences/page.js` maps to `/settings/preferences`.

2.  Add the page file.

    Inside the directory, create `page.js` \(or `page.ts`\). The build looks for a file named `page.js`/`page.ts` to terminate a route; anything else in that directory is ignored.

    Older applications may name the page file `index.js` instead. Both work: `page.js` is preferred for new code, and an existing app can migrate gradually.

    ```
    // pages/risk/page.js
    import {html} from 'lit';
    import {customElement} from 'lit/decorators.js';
    import {AIUXElement} from '@servicenow/aiux-components-core';
    
    @customElement('my-app-risk-page')
    export default class RiskPage extends AIUXElement {
      static async loader(ctx) {
        return {title: 'Risk'};
      }
    
      render() {
        return html`<h1>${this.loaderData?.title}</h1>`;
      }
    }
    ```

    A page file must meet the following requirements:

    -   Extend `AIUXElement`, not `LitElement` directly: it supplies Tailwind/DaisyUI styling, the `loaderData` accessor, and SSR safety.
    -   `@customElement(...)` registers the tag. Prefix it with your app name so it doesn't collide with another app's tags \(`my-app-risk-page`, not `risk-page`\).
    -   `export default`: the build's page discovery looks for the default export. Any other component you define in the same directory should use a named export instead.
    -   `render()` must be pure and deterministic: it runs during server-side rendering and in the browser, so it can't touch `window`, `document`, or `localStorage`.
3.  Fetch data with a loader.

    `static async loader(ctx)` runs on the server before the page renders. Its return value is JSON-serialized into the page and becomes available as `this.loaderData`.

    ```
    import {AIUXElement, getHeaders} from '@servicenow/aiux-components-core';
    
    @customElement('my-app-risk-page')
    export default class RiskPage extends AIUXElement {
      static async loader(ctx) {
        const res = await fetch(
          `${ctx.protocol}://${ctx.hostname}/api/now/table/sn_risk_risk`,
          {headers: getHeaders(ctx)}
        );
        return {items: (await res.json()).result ?? []};
      }
    
      render() {
        const {items} = this.loaderData;
        return html`
          <section class="p-4 flex flex-col gap-2">
            ${items.map(item => html`<div class="aiux-card">${item.number}</div>`)}
          </section>
        `;
      }
    }
    ```

    Use `getHeaders(ctx)` from `@servicenow/aiux-components-core` when calling ServiceNow table APIs: it forwards the session cookie and CSRF token in one call. `loader` runs on the server, so no browser globals here either.

    **Note:** Route parameters and query parameters on `ctx` are strings: cast them yourself if you need a number or boolean.

4.  Add a dynamic route segment.

    Wrap a directory or file name in square brackets to declare a path parameter:

    ```
    mkdir -p "pages/risk/[riskId]"
    ```

    `pages/risk/[riskId]/page.js` maps to the route pattern `/risk/:riskId`. The value lands on `ctx.params` in the loader:

    ```
    static async loader(ctx) {
      const {riskId} = ctx.params; // a string
      // fetch the record identified by riskId ...
      return {riskId};
    }
    ```

    You can nest dynamic segments, for example `pages/risk/[riskId]/controls/[controlId]/page.js` for `/risk/:riskId/controls/:controlId`.

5.  Build and check the route.

    ```
    pnpm build
    ```

    The build walks `pages/` and writes a route manifest mapping each route pattern to its bundle and tag name. Your app's basename \(from `aiux.json`\) is prepended to every route to form the production URL: `/aiux/<basename><route>`. For a basename of `my-app`, `pages/risk/page.js` serves at `/aiux/my-app/risk`.

6.  Link to the page.

    A page isn't reachable until something links to it. Either use a normal anchor tag:

    ```
    render() {
      return html`<a href="/risk">Go to Risk</a>`;
    }
    ```

    or navigate programmatically from an event handler:

    ```
    import {navigate} from '@servicenow/aiux-client';
    
    _openRecord(e) {
      const {riskId} = e.currentTarget.dataset;
      navigate(`/risk/${riskId}`);
    }
    ```

    The router intercepts a same-origin `<a href>` select automatically and swaps in the new page client-side, without a full reload. It intercepts only a plain left click, with no modifier keys, no `target="_blank"`.


## Verify

-   `pnpm build` succeeds.
-   Open the route in a browser \(or check the Network tab's response preview during SSR\) and confirm your rendered content and loader data appear.
-   If the page uses `navigate()` or a sidebar link, select it and confirm client-side navigation works without a full page reload.

## What to do next

-   [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/page-collections.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/page-collections.md): serving different page implementations from the same route
-   [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/layouts-and-editable-regions.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/layouts-and-editable-regions.md): wiring a page into the app's shell and navigation
-   [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/data-and-apis.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/data-and-apis.md): the full loader contract and `ctx` shape

