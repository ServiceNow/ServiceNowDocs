---
title: Lux Lab
description: Lux Lab is the standalone desktop app for building Lux applications, not a VS Code extension. It combines a project explorer, code editor, instance browser, agent chat panel, source control, and build actions in one window.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/lux-lab-app.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 6
keywords: [Lux Lab, System requirements, Installation, First launch, What's in the window, Project templates, Run and preview actions, Deployment, Privacy]
breadcrumb: [Development tooling, Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Lux Lab

Lux Lab is the standalone desktop app for building Lux applications, not a VS Code extension. It combines a project explorer, code editor, instance browser, agent chat panel, source control, and build actions in one window.

Lux Lab is one of the tools you can use to create or extend Lux experiences. The other is [Lux Lab for VS Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/lux-lab-for-vs-code.md). Pick whichever fits your workflow; neither is a track you graduate from.

## System requirements

|Requirement|Minimum|Recommended|
|-----------|-------|-----------|
|Operating system|macOS 12 \(Monterey\) or later|macOS 13 \(Ventura\) or later|
|Processor|Apple Silicon \(M1 or later\)|Apple Silicon M2 or later|
|RAM|8 GB|16 GB or more|
|Disk space|2 GB free|10 GB or more free|

|Requirement|Minimum|Recommended|
|-----------|-------|-----------|
|Operating system|Windows 10 \(64-bit\) or later|Windows 11|
|Processor|Intel Core i5 / AMD Ryzen 5|Intel Core i7 / AMD Ryzen 7 or better|
|RAM|8 GB|16 GB or more|
|Disk space|2 GB free|10 GB or more free|

You also need Node.js v24 or later, pnpm v10 or later, Git v2.30 or later, and an internet connection for instance connectivity and agent features.

## Installation

Download the Lux Lab app using the following link. [Lux Lab installation files](https://install.service-now.com/glide/distribution/builds/package/app-signed/aiux/Lux-Lab-official-release.zip).

For more information on installing Lux Lab, see [Install Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/installing-lux-lab.md).

-   macOS ships as a `.dmg` you drag into `/Applications`
-   Windows ships as an `.exe` installer

## First launch

On the first macOS launch, the operating system may block the app. Open it from **System Settings** &gt; **Privacy &amp; Security** by selecting **Open Anyway**.

A guided setup screen walks you through three steps before you reach the home page.

|Step|What it does|Required|
|----|------------|--------|
|**Environment**|Checks for Node.js v24+, pnpm v10+, and Git v2.30+|Yes|
|**Agents**|Detects whether the agents the Agent Chat Harness needs are installed, and offers to install them|No|
|**Instance sign-in**|Signs in to a provisioned ServiceNow instance that can run Lux applications, using your instance URL, username, and password \(basic authentication\)|Yes|

A failing environment check gets a **Run Fix** button that installs or resolves the issue and re-validates. All environment checks must pass before you continue. The Agents step completes automatically if the agents are already present, and you can configure agents later from the Agents and Skills panel. The home page is not accessible without signing in to an instance.

Agent support is vendor-neutral. The Agents and Skills panel lists every ACP-compatible agent configured on your system, such as Claude, Devin, or Codex. The panel also lists the skills bundled with Lux Lab and any project-level skills in your project.

## Lux Lab home

|Region|Purpose|
|------|-------|
|Top bar|Workspace tabs, plus the **Run**, **Preview**, and **Deploy** actions|
|Activity bar|Icon strip that switches between Explorer, Source Control, Search, and other views|
|Project Explorer|File tree for your local project|
|Code Editor|Editing area with tabs and a breadcrumb trail; supports split views|
|Agent Chat panel|Conversational agent interactions|
|Bottom panel|Tabbed: Terminal, Build, Console, Problems, Tests|
|Instance / Work Items|The connected instance and current work items, pinned in the sidebar|
|Status bar|Branch name, sync status, IntelliSense, and other indicators|

The editor gives language-server-based, context-aware completions as you type, using the same IntelliSense engine as VS Code.

## Project templates

The **Create New Project** dialog scaffolds from one of three templates, or imports an existing local folder or Git repository.

|Template|What it scaffolds|
|--------|-----------------|
|**Base AIUX template**|A full starter with nav layout, pages, and a hello-world widget|
|**Extension template**|An extension to an existing application|
|**Collections template**|A collections-based Lux application|

Lux Lab scaffolds the project, installs dependencies, and opens it. For the same project structure explained from the CLI side, see [Create your first Lux experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-your-first-experience.md).

## Run and preview actions

**Run** starts the local dev server. The button shows **Stop** while the server is up. **Preview** starts the dev server and opens the preview at the same time. Saving a source file triggers hot module replacement, which compiles only the changed module and pushes it to the preview without a full reload. Changes to configuration files such as `aiux.json` need a dev server restart.

The preview opens as an editor tab showing your application in an embedded browser frame. Lux Lab serves it on localhost and proxies it to the instance you're connected to in the app.

Dev server logs and hot-reload activity stream into the **Console** tab. Linter and type errors land in **Problems**; build failures land in **Build**.

## Deployment

Lux Lab's deploy pipeline follows the ServiceNow SDK deployment process. When you trigger a deploy, Lux Lab builds the application, compiling and bundling the source into deployable artifacts. It then runs `now-sdk install` to push the built metadata and artifacts to the target instance. The target is the instance you're currently signed in to. The process is identical to running the ServiceNow SDK deployment from the command line.

The **Deploy** button in the title bar runs a full build and deploy \(`Cmd+Shift+D` on macOS, `Ctrl+Shift+D` on Windows\). Its drop-down menu adds three options.

|Option|What it does|
|------|------------|
|**Build**|Runs the build step only, without deploying|
|**Custom Deploy**|Deploys to a different instance you have previously connected to but aren't currently signed in to|
|**Project scripts**|Runs any script defined in the project's `package.json`|

Deploy output streams into the **Build** tab. If several projects are open in the workspace, **Deploy** asks which one to deploy.

Before deploying, confirm that the project builds, that you're connected to the target instance, and that your account has permission to deploy applications on it.

Under **App Settings**, the ServiceNow SDK version Lux Lab uses for a project defaults to the latest. For what those commands do if you want the manual workflow instead, see [ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/now-sdk.md).

## Privacy

Lux Lab collects only installation status, a signal used to count active installations. It doesn't collect or transmit code, project files, prompts, agent conversations, or instance credentials. To opt out, open **App Settings** &gt; **Advanced** and turn off the installation status telemetry toggle.

**Related topics**  


[Lux Lab for VS Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/lux-lab-for-vs-code.md)

[ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/now-sdk.md)

