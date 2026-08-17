---
title: Build Agent workflow
description: The Build Agent workflow automates building applications, testing, and deploying update sets on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/build-agent-workflow.html
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Build Agent workflow

The Build Agent workflow automates building applications, testing, and deploying update sets on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.

A general workflow for using Build Agent in either ServiceNow Studio or the ServiceNow IDE is the following:

1.  Make sure that everything you need is properly configured in the settings, such as supported MCP server connections. For more information, see [Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/configure-build-agent.md).
2.  Open ServiceNow Studio or the ServiceNow IDE to access the Build Agent panel in the workspace.
3.  Describe what to create or change in natural language.
4.  Let Build Agent parse requirements and propose the application and files to create or modify.
5.  Build Agent edits code or metadata or scaffolds a new application.
6.  Review proposed edits, diffs, and summaries, and approve or adjust before applying changes. Review checkpoints and manual edit update sets. In ServiceNow Studio, view generated app details from the **Apps** tab, and inspect the source code from the **Explorer** tab.
7.  Iterate until the desired metadata changes are complete. For more information, see [Supported metadata in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent-supported-metadata.md).
8.  Prompt Build Agent to create and run Automated Test Framework \(ATF\) tests to verify that the tests execute as expected. Depending on your configuration, Build Agent may ask you if you want to run ATF tests. If there are failures, auto troubleshooting triages the tests and produces a regression test suite that you can use to monitor app health.
9.  Instruct Build Agent to build the application; verify results in the File Navigator or Metadata Explorer.
10. Deploy the application. If you're using source control, you can push to Git.For more information, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent-deployment.md).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/exploring-build-agent.md)

