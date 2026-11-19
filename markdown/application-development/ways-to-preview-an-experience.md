---
title: Ways to preview a Lux experience
description: Four mechanisms show you an app before it ships, from the Lux Lab Preview panel to a local production build. No shareable preview link is available, and no server-side staging view exists separate from your local dev server or a deployed instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ways-to-preview-an-experience.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 5
keywords: [Ways to preview an experience, Preview in Lux Lab, Preview locally with the dev server, Preview a production build locally, Verify server-rendered output]
breadcrumb: [Test and deploy a Lux app, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Ways to preview a Lux experience

Four mechanisms show you an app before it ships, from the Lux Lab Preview panel to a local production build. No shareable preview link is available, and no server-side staging view exists separate from your local dev server or a deployed instance.

The four are the Lux Lab Preview panel, a local dev server with hot reload, a local production build, and server-rendered output on a deployed instance.

## Preview in Lux Lab

Lux Lab has a dedicated **Preview** panel: a live, embedded browser view of your running app, opened as an editor tab. The same local dev server described later in this topic backs the panel, proxied to the ServiceNow instance you are logged in to.

The methods for opening the panel are described in the following table.

|Method|What happens|
|------|------------|
|**Preview** in the title bar|Starts the dev server if it isn't running, then opens the preview tab|
|**Run** in the title bar|Starts the dev server; the preview tab opens when the server is ready|
|Auto-open|The preview opens by itself when the dev server finishes starting|

The **Run** button doubles as the stop control. It displays **Run** when the server is stopped, shows a transition indicator while it starts, and is set to **Stop** after the server is running.

The preview panel carries a floating toolbar. Its controls are described in the following table.

|Control|What it does|
|-------|------------|
|URL bar|Shows the current preview URL, and is editable. Enter a path or URL and press Enter to navigate|
|**Refresh**|Reloads the preview page|
|**Open in browser**|Opens the current URL in your default system browser|
|Device presets|Switches between Mobile, Tablet, and Desktop viewport widths|
|**Screenshot**|Captures the preview and sends the image to the Agent Chat panel|

Beyond the three presets, you can drag the resize handles at the edges of the preview frame for a custom viewport width. Dragging the tab's edge resizes the preview against the code editor.

Saving a file refreshes the preview automatically through hot module replacement \(HMR\); the toolbar's Refresh button is for a manual reload. Changes to configuration files such as `aiux.json` are the exception, those need a dev-server restart to take effect.

Logs from the dev server, startup progress, HMR activity, runtime errors, stream into the **Console** tab of the bottom panel. Linter and type errors appear in **Problems**, where selecting an error jumps to the offending line; build-pipeline failures appear in **Build**.

For the Lux Lab app that hosts this panel, see [Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/lux-lab-landing.md).

## Preview locally with the dev server

`pnpm dev` starts the full request pipeline on your machine with hot reload: proxy, version router, server-side rendering \(SSR\) service, and Core UI. You see real server-rendered output, not a static mock.

```
cd my-app
pnpm dev
```

Open `http://localhost/aiux/<basename>/<landing>` in your browser. Editing a file under `pages/` or `components/` recompiles and reloads the app automatically, and the build writes development artifacts to `.dev` directories.

The dev server starts the same layered pipeline as production. The services and their ports are provided in the following table.

|Service|Port|Role|
|-------|----|----|
|HTTP proxy|80|Entry point for all requests|
|Version router|3000|Routes to versioned SSR services|
|SSR service|3001+|Renders your pages server-side|
|Core-UI service|4000|Serves list, record, and dashboard pages|
|Core static server|4999|Serves shared widget bundles|

To run more than one app's dev server at once, set `AIUX_INSTANCE` to a number from 1 to 9 before starting it. Setting it shifts the whole port range so the stacks don't collide. `AIUX_INSTANCE=1` moves the proxy from port 80 to 31000 and its services into the 31001+ range, `AIUX_INSTANCE=2` uses 32000, and so on.

```
AIUX_INSTANCE=1 pnpm dev
```

If port 80 requires elevated permissions or is already taken, set `PROXY_PORT` in your `.env` file instead, and access your app at `http://localhost:<PROXY_PORT>/aiux/...`.

To diagnose a local setup problem, run the diagnostic tool before digging further:

```
aiux doctor --check
```

It diagnoses and reports common configuration problems.

For the automated checks that run against the same code, see [Test an app locally](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/test-an-app-locally.md).

## Preview a production build locally

`pnpm dev` runs an unoptimized dev build. To see what actually ships, the built `dist/vN/` bundles, no hot reload, build and serve it locally before you deploy:

```
pnpm build
pnpm serve
```

Open the same `http://localhost/aiux/<basename>/<landing>` URL. This is the closest you get to your production artifact without touching a ServiceNow instance.

## Verify server-rendered output

Your app can be deployed and running either locally or on an instance. In both cases, the rendered HTML your loader produced appears on the document request's **Preview** tab in **DevTools** &gt; **Network**. A blank Preview with a working browser page means your loader is generating an error server-side, check the service logs at `https://<instance>/aiux/<basename>/logs`.

Do not confuse this DevTools **Preview** tab with the Lux Lab Preview panel or the `pnpm serve` command described earlier: three unrelated mechanisms that share the word "preview." The tab inspects one request's rendered HTML; the panel and `pnpm serve` each run your whole app.

For deeper inspection of a running page, widget properties, re-render causes, network calls, see . That topic covers Lux DevTools, a different tool from the browser's built-in DevTools panel described earlier in this topic.

Confirming that server-rendered output arrives is also an item on the ship checklist in [Deploy to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/deploy-to-an-instance.md).

