---
title: Document an application using Build Agent
description: Generate documentation for the structure, tables, and UI components of an application. Build Agent reads the codebase and creates a README file describing the application architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ba-document-an-app.html
release: zurich
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [Build Agent, document application, README, ServiceNow IDE, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Document an application using Build Agent

Generate documentation for the structure, tables, and UI components of an application. Build Agent reads the codebase and creates a README file describing the application architecture.

## Before you begin

Role required: admin

## About this task

Build Agent processes the application's codebase and produces a README file summarizing the application's tables, sample data, and UI structure. Review the generated documentation for accuracy before sharing or publishing it. AI-generated results may not be accurate in all cases.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

2.  Enter a prompt requesting documentation for the application, such as `Document this app`, in the Build Agent chat box that appears on the ServiceNow Studio home page.

    You can also select the Conversations icon in the Navigator panel \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text:to open Build Agent.

3.  Review the response in the Build Agent chat panel.

    Build Agent processes the existing files in the application and generates a README file.

4.  In the File Explorer, open the `README` file that Build Agent creates.

    The README file displays a description of the application's tables, sample data, and UI page.


## Result

The README file is available in the File Explorer for review and distribution.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

