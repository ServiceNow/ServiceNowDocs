---
title: Supported file types for Build Agent
description: Build Agent accepts images, documents, code files, and file types specific to ServiceNow as uploads. Supported formats, size limits, and general guidelines apply when generating apps and metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/ba-supported-file-types.html
release: australia
product: Building Applications
classification: building-applications
topic_type: reference
last_updated: "2026-06-04"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Supported file types for Build Agent

Build Agent accepts images, documents, code files, and file types specific to ServiceNow as uploads. Supported formats, size limits, and general guidelines apply when generating apps and metadata.

|Category|Extensions|
|--------|----------|
|Code and scripts|.js, .ts, .tsx, .jsx, .py, .java, .css, .html, .xml, .json|
|Documents|.txt, .md, .csv, .log|
|Images|.png, .jpg, .jpeg, .gif, .svg, .webp|
|Specific to ServiceNow|.now.ts \(Fluent DSL\), .xml \(update sets\)|

You can also use MCP server connections, such as for Figma, to provide context for Build Agent. For more information, see [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/accelerate-design-to-development-with-figma-mcp-server.md).

**Note:** You must be on Australia Patch 3 or higher to upload any file types besides images.

## Size limits

|Category|Description|
|--------|-----------|
|Individual file|Up to 10 MB per attachment.|
|Images|View and analyze screenshots and diagrams directly in the chat.|

## File upload guidelines

-   Upload text-based files to let Build Agent read and analyze the full content, then incorporate it into your app.
-   Upload images or screenshots to provide UI mockups, error screenshots, or architecture diagrams as context for development.
-   If an attachment is not visible after a window reload, re-upload the file.

## File uploads and your project

Uploaded files are available only within the current conversation and aren't added to your ServiceNow project or application automatically.

|Upload|What Build Agent can do|
|------|-----------------------|
|A script file \(.js, .ts\)|Read the file, then write the content into your app using the appropriate source file tool.|
|A screenshot of an error|Analyze the screenshot and help resolve the issue.|
|A CSV or data file|Use the data to inform table design or generate test data.|
|A mockup or diagram|Use the file as a reference to build a UI page.|
|An XML update set|Analyze the file and recreate the metadata using Fluent APIs.|

**Note:**

-   Uploading a file does not add it to your app. To incorporate file content into your project, ask Build Agent to do so explicitly, for example, "Add this script to my app as a script include."
-   Uploaded files don't persist across sessions. If the window reloads, re-upload the file for Build Agent to access the content again.

**Parent Topic:**[Build Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-reference-landing.md)

