---
title: Lux Lab for VS Code
description: ServiceNow AI Experience Lab for VS Code brings project creation, instance browsing, local preview, build, and deployment into Visual Studio Code. It ships alongside the standalone Lux Lab desktop app as a separate product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/lux-lab-for-vs-code.html
release: zurich
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 4
keywords: [Lux Lab for VS Code, Requirements, Instance connections, What it provides, Commands, Workflow]
breadcrumb: [Development tooling, Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Lux Lab for VS Code

ServiceNow® AI Experience Lab for VS Code brings project creation, instance browsing, local preview, build, and deployment into Visual Studio Code. It ships alongside the standalone Lux Lab desktop app as a separate product.

Use the Lux Lab VS Code extension, rather than the standalone Lux Lab app, when you want the same build/preview/deploy workflow inside an editor you already use. The extension adds project creation, instance browsing, local preview, build, and deployment commands to VS Code.

For the desktop app, see [Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-lab-app.md).

## Requirements

|Requirement|Minimum version|
|-----------|---------------|
|Visual Studio Code|1.97|
|Node.js|24|
|pnpm|10|
|now-sdk|4.12|
|Target instance|Zurich Patch 12 or later, or Australia Patch 5 or later|

The **Lux: Show Environment Check** command displays the required and detected versions for Node.js, pnpm, and ServiceNow SDK. After fixing a failure, run **Lux: Re-check Environment**.

**Warning:** The Environment Check page offers **Skip checks and proceed anyway**. Skipping leaves the extension's features enabled while the checks are unmet, and commands may fail. The check must pass before you can create a project.

## Instance connections

You connect to an instance from **Instance Explorer** in the [Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-lab-app.md) activity bar view by selecting **Connect to ServiceNow**, or by running **Lux: Add ServiceNow Instance**. You enter the instance name or full URL, then select an authentication method.

-   **Basic**

    You enter your username, password, and a unique profile alias. The extension validates the credentials against the instance, then stores the profile in VS Code SecretStorage. The extension masks passwords and doesn't write them to the project.

-   **OAuth**

    You enter a profile alias, open the authorization URL the extension displays, authorize in the browser, and paste the returned code into a masked input. The extension exchanges it using Authorization Code with PKCE and stores the token in VS Code SecretStorage. You don't enter a username or password in the extension.

    Remote instances must use HTTPS.


## What it provides

-   **Instance Explorer**

    Browses Experiences, Pages, and Widgets on a connected instance. Select an artifact to open its metadata, open its source, or launch a preview.

-   **Script Runner**

    Creates projects, installs dependencies, and runs dev, build, and deploy. Actions include **Dev**, **Build**, **Deploy**, **Stop**, **Show Command Output**, and **Show Dev Server Terminal**.

-   **Quick Preview**

    Opens local preview-able pages and widgets without leaving VS Code. Save the file first, then select it in Quick Preview. You can also select and hold \(or right-click\) a preview-able file and select **Lux: Open Preview**.

    An AI agent can drive page and widget creation through the project's bundled skills. The extension isn't tied to a specific agent vendor.


## Commands

Open the **Command Palette** \(`Cmd+Shift+P` on macOS, `Ctrl+Shift+P` on Windows and Linux\) and search for `Lux:`.

-   `Lux: Show Welcome Page`
-   `Lux: Show Environment Check`
-   `Lux: Re-check Environment`
-   `Lux: Add ServiceNow Instance`
-   `Lux: Sign in to Active Instance`
-   `Lux: Refresh Instance Explorer`
-   `Lux: Create LUX Project`
-   `Lux: Create Page`
-   `Lux: Run Script...`
-   `Lux: Build`
-   `Lux: Deploy`
-   `Lux: Open Preview`
-   `Lux: Show Command Output`

Selecting and holding \(or right-clicking\) a project, page, widget, or preview-able file in the **Explorer** or [Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-lab-app.md) views gives the same actions in context. The context menu also opens a terminal and reveals a project in **Finder** or **File Explorer**.

## Workflow

The `Lux: Create Lux Project` command scaffolds a standalone application. You select the instance, the parent folder, the application name, the project folder name, the **Standalone App** template, and the scope suffix. When the extension retrieves the vendor prefix from the instance, the prefix is fixed and only the suffix is editable. The extension then scaffolds, installs dependencies, and opens the project. The `Lux: Create Page` command adds a route and creates `pages/<page-slug>/page.js`.

For extension applications rather than standalone ones, see [Create an extension application with Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-an-extension-application-with-lux-lab.md).

**Related topics**  


[Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-lab-app.md)

[ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/now-sdk.md)

