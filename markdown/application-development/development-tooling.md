---
title: Development tooling
description: Three tools can build a Lux experience: Lux Lab, ServiceNow Lux Lab for VS Code, and the ServiceNow SDK. Lux and ServiceNow Lux Lab for VS Code build on the ServiceNow SDK foundation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/development-tooling.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [Development tooling, Tool comparison]
breadcrumb: [Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Development tooling

Three tools can build a Lux experience: Lux Lab, ServiceNow Lux Lab for VS Code, and the ServiceNow SDK. Lux and ServiceNow Lux Lab for VS Code build on the ServiceNow SDK foundation.

## Tool comparison

The tools differ in how much of the ServiceNow SDK CLI they wrap in a UI, and where that UI lives.

|Tool|What it is|Where it runs|Best for|
|----|----------|-------------|--------|
|[Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/lux-lab-app.md)|A ServiceNow application that combines a project explorer, code editor, instance browser, agent chat panel, source control, and build actions in one window|Standalone desktop app, downloaded from [Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/lux-lab-app.md).|Working in a purpose-built tool, and agent-assisted page and widget authoring|
|[Lux Lab for VS Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/lux-lab-for-vs-code.md)|An extension adding Instance Explorer, Script Runner, Quick Preview, and `Lux:` commands to VS Code|Inside Visual Studio Code|Working in VS Code with Lux tooling alongside an existing setup|
|[ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/now-sdk.md)|The CLI that scaffolds, builds, and deploys a Lux application \(`now-sdk init` / `build` / `install`\)|Terminal, in any editor|Full control, scripting, and continuous integration \(CI\) pipelines|

Lux Lab and ServiceNow Lux Lab for VS Code are separate products that ship side by side. Pick whichever fits your workflow. Neither is a track you graduate from.

Both wrap the ServiceNow SDK rather than replacing it. Lux Lab runs `now-sdk` commands on your behalf when you build and deploy. The VS Code extension requires ServiceNow SDK 4.12 or later to be installed.

## Next steps

After you pick a tool, see [Create your first Lux experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-your-first-experience.md), which uses the Now SDK CLI directly.

