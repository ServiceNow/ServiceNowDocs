---
title: Project structure
description: A scaffolded Lux app has a fixed file layout: two manifests, an app-level lifecycle module, a theme file, and directories for pages, widgets, and regions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/project-structure.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [Project structure, What each entry is for, Fields in aiux.json, What the tree compiles to]
breadcrumb: [Lux architecture, Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Project structure

A scaffolded Lux app has a fixed file layout: two manifests, an app-level lifecycle module, a theme file, and directories for pages, widgets, and regions.

```
my-app/
├── aiux.json              # Lux app manifest
├── now.config.json        # ServiceNow scope manifest (now-sdk)
├── package.json           # Depends on @servicenow/karuna + @servicenow/sdk
├── application.js         # App-level lifecycle hooks (setup, navigate, teardown)
├── theme.js               # AppTheme tokens (colors, radii)
├── pages/                 # File-based routing (one directory per route)
│   ├── layout.js          # App chrome (header, nav) wrapped around every page
│   ├── home/
│   │   ├── page.js        # AIUXElement page (default export)
│   │   └── components/    # Components co-located with the page that uses them
│   │       └── aiux-feature-card.js
│   └── incidents/
│       └── page.js        # Page with `static async loader(ctx)`
├── widgets/               # Custom AIUXWidgetElement widgets (+ server scripts)
│   └── aiux-hello-world/
│       ├── index.js
│       └── server-script.js
├── regions/               # Region DSL files (one thunk per named region)
├── eslint.config.mjs      # ESLint flat config (aiux plugins)
├── scripts/               # setup-agent-skills.mjs (postinstall helper)
├── AGENTS.md              # Canonical guidance for AI coding agents
├── CLAUDE.md / GEMINI.md  # Point back to AGENTS.md
├── .claude/               # Hooks + settings for Claude Code
└── .nvmrc / .gitignore

```

## What each entry is for

|Entry|Purpose|
|-----|-------|
|`aiux.json`|Lux app manifest \(the experience's declaration\).|
|`now.config.json`|ServiceNow scope manifest that `now-sdk` reads on build and deploy. Your app has two manifests, not one.|
|`package.json`|Dependency and script declarations. `@servicenow/karuna` and `lit` are dependencies; `@servicenow/sdk`, the `eslint-plugin-aiux-*` rules, and the agent packs are dev dependencies. Holds the `dev`, `build`, `serve`, `deploy`, and `lint` scripts.|
|`application.js`|App-level lifecycle hooks: `setup()`, `navigate()`, and `teardown()`.|
|`pages/layout.js`|The layout every page in the experience renders inside \(header, navigation, footer\). It extends `NavLayout` and is not re-created when the user navigates between routes.|
|`theme.js`|The experience's theme tokens: colors, radii.|
|`pages/`|File-based routing. Each subdirectory is a route, and `page.js` in that directory is an `AIUXElement` page \(the file's default export, optionally with `static async loader(ctx)` for server-side data fetching\).|
|`pages/<name>/components/`|Components scoped to the page that uses them, co-located rather than shared globally.|
|`widgets/`|Custom `AIUXWidgetElement` widgets, each with an `index.js` and an optional `server-script.js`.|
|`regions/`|Region DSL files. Each one default-exports a nullary thunk returning a `region` template, and its region name comes from its path. `region` can't be imported from anywhere else.|
|`eslint.config.mjs`|ESLint flat config with the `eslint-plugin-aiux-*` rules.|
|`scripts/`|Build and setup helpers, such as `setup-agent-skills.mjs`, run through `postinstall`.|
|`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`|AI coding agent guidance. `CLAUDE.md` and `GEMINI.md` point back to `AGENTS.md`.|
|`.claude/`|Hooks and settings for Claude Code.|
|`.nvmrc`, `.gitignore`|Standard Node project files.|

Note the split between the two files at the app root that are easy to confuse. `pages/layout.js` is the layout \(the persistent chrome your pages render inside, and a widget class in its own right\). `application.js` is the app's lifecycle module: three hooks, no markup. They are separate files with separate jobs.

## Fields in aiux.json

|Field|What it defines|
|-----|---------------|
|`name`|The human-readable application name.|
|`basename`|The URL prefix \(everything under `/aiux/<basename>` is this experience\).|
|`landing`|The route served when someone opens the app with no path.|
|`development.token`|A basic-auth token used only for local development.|
|`build.exclude`|Glob patterns kept out of production builds.|
|`experienceAcls`|Who is allowed into the experience at all.|
|`scope` / `scopeId`|The ServiceNow application scope that owns the records. Added at deploy time, not by hand.|

## What the tree compiles to

Deploying compiles each source file into its corresponding platform record.

|Source|What it becomes|
|------|---------------|
|`aiux.json`|The experience itself \(name, URL prefix, landing page, per-experience settings, and any menus declared in it\)|
|`pages/<route>/page.js`|One page record per page|
|`pages/layout.js`|The app's layout|
|`widgets/<name>/index.js`|Reusable, discoverable widgets|
|`theme.js`|Theme tokens|
|Static assets|Attachments in your scope \(images, fonts, JSON\)|
|Compiled bundles|JavaScript attachments on the widget records, served by the runtime|

Pages, widgets, layouts, and internal helper components all compile to the same kind of widget record. A `category` field is what distinguishes them: `page`, `layout`, `discoverable`, or `internal`. So there's one schema to learn, not three.

**Related topics**  


[Core concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/core-concepts.md)

[Build with Lux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-with-lux.md)

