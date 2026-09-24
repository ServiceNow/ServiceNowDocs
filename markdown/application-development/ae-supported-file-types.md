---
title: Supported file types for Autonomous Engineer
description: Autonomous Engineer accepts images, documents, code files, and file types specific to ServiceNow as uploads. Supported formats, size limits, and general guidelines apply when generating apps and metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-supported-file-types.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Supported file types for Autonomous Engineer

Autonomous Engineer accepts images, documents, code files, and file types specific to ServiceNow as uploads. Supported formats, size limits, and general guidelines apply when generating apps and metadata.

## File types

|Category|Extensions|
|--------|----------|
|Code and scripts|.js, .ts, .tsx, .jsx, .py, .java, .css, .html, .xml, .json|
|Documents|.txt, .md, .csv, .log|
|Images|.png, .jpg, .jpeg, .gif, .svg, .webp|
|Specific to ServiceNow|.now.ts \(Fluent DSL\), .xml \(update sets\)|

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

**Parent Topic:**[Autonomous Engineer reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer-reference-landing.md)

