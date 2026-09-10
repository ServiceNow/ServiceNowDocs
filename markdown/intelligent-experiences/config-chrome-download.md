---
title: Configure Chrome to download files automatically
description: Configure Chrome so that the files can automatically complete downloads without manual intervention, and each download's status and path can be tracked automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/config-chrome-download.html
release: australia
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 1
keywords: [configure, file download, web agent, Chrome]
breadcrumb: [Adaptive desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Configure Chrome to download files automatically

Configure Chrome so that the files can automatically complete downloads without manual intervention, and each download's status and path can be tracked automatically.

## Before you begin

Role required: none

## About this task

The agent needs to detect when a download completes and capture the resulting file name and path. Chrome's default behavior is to prompt the user to choose a save location for every download. This blocks the detection. Turning off the default behavior enables the agent to save the downloaded file automatically and track it.

## Procedure

1.  Enter `chrome://settings/downloads` in the Chrome address bar, and press **Enter**.

2.  Turn off the **Ask where to save each file before downloading** option.


## Result

The files get downloaded automatically without any prompt. The Web agent extension can now detect each download's completion and report its status and file path to the reasoning layer.

**Parent Topic:**[Configuration for adaptive path desktop actions for web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ad-adaptive-path-da.md)

**Related topics**  


[File upload and download in adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/upload-download-file.md)

[Considerations for file upload and download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

