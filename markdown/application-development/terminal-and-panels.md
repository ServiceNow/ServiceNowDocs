---
title: Terminal and panels
description: The bottom panel in Lux Lab contains five tabs that help you run commands, monitor your running application, track build and deploy progress, and review code quality issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/terminal-and-panels.html
release: zurich
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [Terminal and panels, Terminal, Console, Build, Problems, Tests]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Terminal and panels

The bottom panel in Lux Lab contains five tabs that help you run commands, monitor your running application, track build and deploy progress, and review code quality issues.

The following table describes the purpose of each tab.

|Tab|Purpose|
|---|-------|
|**Terminal**|Full OS shell for running any CLI command|
|**Console**|Live logs from the running dev server|
|**Build**|Build output and deployment details|
|**Problems**|Linter diagnostics across the project|
|**Tests**|Test runner output|

To toggle the entire bottom panel, press Cmd+J \(macOS\) / Ctrl+J \(Windows\). To open directly to the **Terminal** tab, press Ctrl+\`.

## Terminal

The integrated terminal is a full OS shell. On macOS it runs bash or zsh, and on Windows it runs PowerShell or cmd, depending on your system default. You can run any command you would normally run in a terminal, such as installing dependencies, using Git, running scripts, and invoking CLIs.

## Terminal sessions

-   Press Ctrl+\` to open the Terminal tab.
-   Select the **+** button in the terminal toolbar to start a new terminal session.
-   Multiple sessions appear as tabs in the terminal tab bar. Select any tab to switch between them.
-   Right-click a tab to rename, split, or close a session.

You can keep a dev server running in one session while running other commands in separate sessions at the same time.

## Shell configuration

Lux Lab uses your system's default shell. To change it, go to **App Settings** &gt; **Terminal** &gt; **Default Shell** and select from the detected shells or enter a custom path.

## Panel size

Drag the top edge of the bottom panel up or down to resize it. Press Cmd+J / Ctrl+J to hide and show the panel.

## Console

The **Console** tab shows the live log output from your running dev server. When you start the development server \(`pnpm dev`\), the Console streams all console logs, warnings, and errors from the running application in real-time.

Use the Console to do the following:

-   Monitor network requests and application logs during development.
-   Catch runtime errors and warnings from your Lux application.
-   See Hot Module Replacement \(HMR\) activity as you edit files.

## Build

The **Build** tab shows the output from build operations and deployments:

-   Build logs: Output from compiling and bundling your Lux application, such as `pnpm build`
-   Deploy logs: Progress and results when you deploy to a ServiceNow instance

Each time you trigger a build or deploy, the output streams into this tab so you can monitor progress and diagnose any failures.

## Problems

The **Problems** tab lists all linter diagnostics reported across your entire project, including errors, warnings, and informational messages. It works the same as the Problems panel in VS Code.

## Problems list columns

Each entry shows the columns in the following table.

|Column|Description|
|------|-----------|
|**Severity icon**|Red circle \(error\), yellow triangle \(warning\), or blue circle \(info\)|
|**Message**|Description of the problem|
|**Source**|Tool that reported the problem, for example `eslint` or `ts`|
|**File**|File containing the problem|
|**Line:Column**|Exact location|

## Navigating to a problem

-   Select any entry to jump to the exact location in the editor.
-   Use F8 / Shift+F8 to cycle through problems in the current file from the editor.

## Filtering

Use the filter bar at the top of the panel to search by message text or file name. To filter by severity, toggle the **Errors**, **Warnings**, or **Info** buttons.

## Tests

The **Tests** tab captures output from your test runner scripts. When you run your tests from the Terminal, Lux Lab captures and displays the results here.

## Next steps

-   [Agents and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/agents-and-skills.md)
-   [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/deploy-changes.md)

