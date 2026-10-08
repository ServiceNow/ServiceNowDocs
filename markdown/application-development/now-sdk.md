---
title: ServiceNow SDK
description: ServiceNow SDK is the command-line tool that scaffolds, builds, and deploys a Lux application. It's distributed as the npm package @servicenow/sdk and invoked as now-sdk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/now-sdk.html
release: australia
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [Now SDK, Requirements, Versions, Installation, Commands, Reference documentation]
breadcrumb: [Development tooling, Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow SDK

ServiceNow SDK is the command-line tool that scaffolds, builds, and deploys a Lux application. It's distributed as the npm package `@servicenow/sdk` and invoked as `now-sdk`.

## ServiceNow SDK overview

Use the ServiceNow SDK CLI directly, rather than Lux Lab, when you need full control over your development environment. Lux Lab is a desktop application that bundles an editor, an AI coding agent, a local dev server, and a one-click deploy action into a single window. The CLI exposes those same operations as separate commands \(now-sdk build, now-sdk install, etc.\). You can run these commands in whatever editor, terminal, and CI/CD pipeline you choose.

## Requirements

-   Node.js 24 or later
-   pnpm 10 or later — the project's package manager
-   Git 2.30 or later
-   Access to a ServiceNow instance \(local or remote\) with credentials

## ServiceNow SDK Versions

|Version|Notable changes|
|-------|---------------|
|4.12.x \(latest\)|Lux fixes and enhancements, async app installs by default, expanded `auth` and `cicd` commands. The floor for [Lux Lab for VS Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/lux-lab-for-vs-code.md).|
|4.10.x|The `now-sdk cicd` command, for CI/CD pipeline integration|
|4.9.x|Maintenance and reliability fixes for the build and transform pipeline. The floor at which `@servicenow/sdk` became the customer-facing CLI for the Lux dev server.|

Check which version a project uses:

```
cat package.json | grep @servicenow/sdk
```

## Installation

```
npm install -g @servicenow/sdk@latest
```

## Commands

|Command|What it does|
|-------|------------|
|`now-sdk auth`|Configure authentication to an instance|
|`now-sdk init` \(alias: `create`\)|Initialize a new application, apply a template to an existing one, or convert a legacy application|
|`now-sdk download <directory>`|Download application metadata from the instance|
|`now-sdk build [source]`|Compile sources into app files and generate an installable package|
|`now-sdk install` \(alias: `deploy`\)|Install or update the application on the instance|
|`now-sdk dependencies [sysIds..]`|Download configured dependencies and TypeScript type definitions|
|`now-sdk transform`|Convert XML records from the instance or a local path into Fluent source code|
|`now-sdk clean [source]`|Clean the output directory|
|`now-sdk pack [source]`|Zip the built app into an installable artifact|
|`now-sdk explain [topic]`|Display documentation for an SDK topic|
|`now-sdk query <table>`|Query records from a table on the instance|
|`now-sdk cicd`|Integrate builds and installs into a CI/CD pipeline|
|`now-sdk run dev`|Start the local dev server with hot reload|

A scaffolded project wraps the common ones as `package.json` scripts — `pnpm dev`, `pnpm build`, `pnpm deploy`, `pnpm deploy:reinstall`, `pnpm lint`. So day to day you run those instead of calling `now-sdk` directly. For the scaffold those scripts come from, see [Create your first Lux experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-your-first-experience.md).

Those are the only scripts a scaffolded app ships with. The `build:force`, `storybook`, `test`, and `typecheck` scripts exist only inside the Lux monorepo and won't be in your app's `package.json`.

## Reference documentation

The SDK's own documentation covers the commands, `now.config.json`, and the Fluent language in depth.

|Resource|URL|
|--------|---|
|SDK documentation home|`https://servicenow.github.io/sdk/`|
|CLI reference|`https://servicenow.github.io/sdk/cli`|
|`now.config.json` reference|`https://servicenow.github.io/sdk/config/now-config-reference`|
|npm package|`https://www.npmjs.com/package/@servicenow/sdk`|
|Release notes|`https://github.com/servicenow/sdk/releases`|

**Related topics**  


[ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/now-sdk.md)

