---
title: Lux Lab interface
description: The Lux Lab interface divides the app into regions for project files, code editing, agent chat, panel output, and instance status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/lux-lab-interface.html
release: brazil
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Lux Lab interface, Interface regions]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Lux Lab interface

The Lux Lab interface divides the app into regions for project files, code editing, agent chat, panel output, and instance status.

## Interface regions

When you open a project, the Lux Lab interface is composed of the following primary regions:

```
┌─────────────────────────────────────────────────────────────┐
│  Workspace tabs              Run  |  Preview  |  Deploy      │  ← Top Bar
├────┬──────────────┬──────────────────────────┬──────────────┤
│    │              │                          │              │
│ A  │   Project    │      Code Editor         │  Agent Chat  │
│ c  │   Explorer   │  (tabs + breadcrumb)     │    Panel     │
│ t  │              │                          │              │
│ i  ├──────────────┴──────────────────────────┤              │
│ v  │  Terminal | Build | Console |           │              │
│ i  │  Problems | Tests                       │              │
│ t  ├─────────────────────────────────────────┘              │
│ y  │  Instance  •  Work Items                               │
└────┴────────────────────────────────────────────────────────┘
│  Status Bar                                                  │
└──────────────────────────────────────────────────────────────┘
```

The following table describes the purpose of each region.

|Region|Purpose|
|------|-------|
|Top Bar|Workspace tabs on the left, and the **Run**, **Preview**, and **Deploy** action buttons on the right|
|Activity Bar|Narrow icon strip on the far left that switches between Explorer, Source Control, Search, and other views|
|Project Explorer|File tree for your local project, shown when the Explorer icon is active|
|Code Editor|Main editing area with tabs and a breadcrumb trail, with support for split views|
|Agent Chat Panel|AI assistant panel for conversational agent interactions|
|Bottom Panel|Tabbed panel with Terminal, Build, Console, Problems, and Tests|
|Instance and Work Items|Area pinned at the bottom of the left sidebar that shows the connected instance and current work items|
|Status Bar|Bottom strip with the branch name, sync status, IntelliSense, and other indicators|

