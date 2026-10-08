---
title: Lux Lab development server
description: Running your Lux application starts a local development server that serves your application and reflects code changes automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/lux-lab-development-server.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Lux Lab development server, Starting the development server, Monitoring the development server, Hot Module Replacement, Stopping the development server, Build errors, Production build]
breadcrumb: [Using Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Lux Lab development server

Running your Lux application starts a local development server that serves your application and reflects code changes automatically.

## Starting the development server

## From the title bar

You can start the development server from the title bar at the top of the app, using the following buttons:

-   **Run** starts the development server.
-   **Preview** starts the development server and opens the Preview panel at the same time.

As the server starts, the button updates to reflect its current state. The button labels for each state are listed in the following table.

|State|Button label|
|-----|------------|
|Server stopped|**Run**|
|Server starting|Transitioning \(indicator shown\)|
|Server running|**Stop**|

You can select **Stop** at any time to stop the development server.

## From the terminal

You can also start the development server manually from the integrated terminal.

```
pnpm dev
```

## Monitoring the development server

While the development server is running, all of its logs stream into the **Console** tab of the bottom panel. These logs include startup messages, HMR updates, errors, and console output from your application.

The Console tab shows the following activity:

-   Development server startup progress
-   Hot Module Replacement \(HMR\) activity when files are saved
-   Runtime logs and errors from your running application

## Hot Module Replacement

While the development server is running, saving any source file triggers HMR. Lux Lab recompiles only the changed module and pushes the update to the preview without a full page reload, preserving component state where possible.

Changes to configuration files, such as `aiux.json`, take effect only after you restart the development server.

## Stopping the development server

To stop the development server, select **Stop** in the title bar, which is shown while the server is running. You can also press `Ctrl+C` in the terminal session that is running the development server.

## Build errors

Errors that keep the development server from starting or from serving a module appear in the following tabs:

-   **Console** tab: runtime errors from the running application
-   **Problems** tab: linter and type errors in your source files
-   **Build** tab: build pipeline failures

Selecting an error in the **Problems** tab opens the offending line in the editor.

## Production build

To build a production bundle before deploying, run the build command.

```
pnpm build
```

The build writes its output to the `dist/` directory. Build logs stream into the **Build** tab of the bottom panel.

