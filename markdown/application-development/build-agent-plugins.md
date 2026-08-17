---
title: Build Agent plugins
description: The plugins for Build Agent depend on whether you're using the free/trial version or premium version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-plugins.html
release: zurich
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent plugins

The plugins for Build Agent depend on whether you're using the free/trial version or premium version.

Build Agent is available in both ServiceNow Studio and the ServiceNow IDE.

**Note:** The trial app was formerly called "Build Agent" and has been renamed to "Build Agent \(Trial\)."

## Plugins for Build Agent \(Trial/Free\)

The following plugins are required:

1.  `sn_glider`: the only required plugin for Build Agent in the Australia EA \(Australia patch 0\) version
2.  `sn_build_agent`: required for Australia starting with Patch 1

## Plugins for Build Agent \(Premium\)

If you exceed the free interaction limit, you must wait 30 days for a reset, or install the paid version of Build Agent.

1.  For Australia starting with Patch 1, the `sn_now_creator` plugin is required, which contains the `sn_build_agent_pro` plugin.
2.  For the Australia EA \(Australia patch 0\) version, you must manually update ServiceNow Studio and the Unified Developer Core \(UDC\) in the ServiceNow Store before installing ServiceNow Otto for Creator.

**Parent Topic:**[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configure-build-agent.md)

