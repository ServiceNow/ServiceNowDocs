---
title: File upload and download in adaptive desktop actions
description: Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/upload-download-file.html
release: australia
topic_type: concept
last_updated: "2026-08-21"
reading_time_minutes: 1
keywords: [file upload, file download, web agent, human in the loop]
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# File upload and download in adaptive desktop actions

Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.

**Important:**

Generative AI may produce inaccurate or incomplete information. Always validate AI-generated content.

## Overview of the feature

Previously, a file could not be downloaded from or uploaded to a browser when using adaptive desktop actions. The tasks that required attaching a document or had a downloadable output were impacted. Now, these issues are resolved.

## Key benefits

This functionality provides the following benefits:

-   Completes tasks that require attaching a document, such as uploading a file to a form or a ticket.
-   Completes tasks that produce downloadable output, such as exporting a report.
-   Confirms upload success or failure with an actionable reason, instead of assuming the result.
-   Reuses a file downloaded earlier in the same task as the input to a later upload step.
-   Hands off to a the user when the agent can't proceed safely, rather than guessing or retrying indefinitely.

## Considerations

-   A downloaded file's path carries forward automatically only within the same task session. If the upload happens in a different session, the agent asks the user for the file path instead of guessing.
-   Blocked file types and download status values are listed in the file transfer reference.
-   Automated downloads require Chrome configuration. For more information, see [Configure Chrome to download files automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/config-chrome-download.md).

**Parent Topic:**[Configuration for adaptive path desktop actions for web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ad-adaptive-path-da.md)

**Related topics**  


[Configure Chrome to download files automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/config-chrome-download.md)

[Considerations for file upload and download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

