---
title: Build Agent workflow
description: The Build Agent workflow automates the process of building, testing, and deploying applications on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-workflow.html
release: zurich
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent workflow

The Build Agent workflow automates the process of building, testing, and deploying applications on the ServiceNow AI Platform. Build Agent streamlines development by handling code compilation, quality checks, and deployment steps without manual intervention.

A general workflow for using Build Agent in either ServiceNow Studio or the ServiceNow IDE is the following:

1.  Open ServiceNow Studio or the ServiceNow IDE to access the Build Agent panel in the workspace.
2.  Describe what to create or change in natural language.
3.  Let Build Agent parse requirements and propose the application and files to create or modify.
4.  Build Agent edits code or metadata or scaffolds a new application.
5.  Review proposed edits, diffs, and summaries, and approve or adjust before applying changes.
    1.  If you're using ServiceNow Studio, look at the generated app details.
    2.  If you're using the ServiceNow IDE, inspect the code.
6.  Iterate until the desired metadata changes are complete. For more information, see [Supported metadata in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-supported-metadata.md).
7.  Prompt Build Agent to create Automated Test Framework \(ATF\) tests, and then run them.
8.  Instruct Build Agent to build the application; verify results in the File Navigator or Metadata Explorer.
9.  Deploy the application. For more information, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-deployment.md).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

