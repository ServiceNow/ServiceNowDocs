---
title: Document an application using Build Agent
description: Generate documentation for an application's structure, tables, and UI components. Build Agent reads the codebase and creates a README file describing the application architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/ba-document-an-app.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [Build Agent, document application, README, ServiceNow IDE, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Document an application using Build Agent

Generate documentation for an application's structure, tables, and UI components. Build Agent reads the codebase and creates a README file describing the application architecture.

## Before you begin

Role required: admin

## About this task

Build Agent processes the application's codebase and produces a README file summarizing the application's tables, sample data, and UI structure. Review the generated documentation for accuracy before sharing or publishing it. AI-generated results may not be accurate in all cases.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the lower corner of your browser. You can also select the Sparkle icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the application banner.\[Omitted image "sn-studio-access-build-agent.png"\] Alt text: If Build Agent isn't open, open it from the status bar in the corner of your browser.

2.  Enter a prompt requesting documentation for the application in the Build Agent chat panel.

    For example, enter `Document this app`.

3.  Allow Build Agent to process the request.

    Build Agent processes the existing files in the application and generates a README file.

4.  In the File Explorer, open the `README` file that Now Assist for Build Agent creates.

    The README file displays a description of the application's tables, sample data, and UI page.


## Result

The README file is available in the File Explorer for review and distribution.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/use-build-agent.md)

