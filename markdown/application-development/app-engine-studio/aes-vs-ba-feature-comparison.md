---
title: App Engine Studio and Build Agent feature comparison
description: App Engine Studio \(AES\) and Build Agent differ across interface, artifact scope, scripting access, application scope, and governance. Use this feature comparison to understand what changes when you migrate to Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-engine-studio/aes-vs-ba-feature-comparison.html
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [App Engine Studio vs. Build Agent, Feature comparison, Learn about Build Agent, AES vs Build Agent]
breadcrumb: [Migrating to Build Agent, Explore, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# App Engine Studio and Build Agent feature comparison

App Engine Studio \(AES\) and Build Agent differ across interface, artifact scope, scripting access, application scope, and governance. Use this feature comparison to understand what changes when you migrate to Build Agent.

| |App Engine Studio \(AES\)|Build Agent in ServiceNow Studio|
|---|-------------------------|--------------------------------|
|Primary interface|Guided wizard interface|Conversational prompt interface inside ServiceNow Studio|
|Developer persona|Citizen and low-code developers|All developer experience levels, from citizen to pro-code|
|Artifact types|Tables, forms, flows, and workspaces within wizard constraints|Full platform set of artifacts: business rules, Script Includes, Client Scripts, flows, ACLs, UI Builder pages, packaging, and README|
|Script access|Not directly available. Requires converting to ServiceNow Fluent and opening app in an integrated development environment \(IDE\)|Built-in script writing and reading|
|Application scope|Scoped applications only|Scoped and global applications|
|Existing application modification|Applications you created only|Any application, including base system applications|
|Session context|Stateless|Persistent within a session and accumulates over the course of a session|
|External integrations at build time|None|Model Context Protocol Server Console \(MCP\) client connections. For a full list of MCP connections, see [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/accelerate-design-to-development-with-figma-mcp-server.md)|
|Governance|App Engine Management Center \(AEMC\) optional deployment path|Several deployment options, including App Engine Management Center \(AEMC\). See[Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md)|
|AI capability embedding|Manual post-build step|In-app AI agents and skills can be embedded in workflows at build time|

## What does not change

The following remain consistent across both tools:

-   App files built in AES are already accessible in ServiceNow Studio. No re-creation or export is required.
-   Workflow Studio flows created in AES are the same records in ServiceNow Studio.

