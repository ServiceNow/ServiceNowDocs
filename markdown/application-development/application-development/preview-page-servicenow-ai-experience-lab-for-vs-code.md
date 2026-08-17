---
title: Preview a page
description: Test that your page appears and functions as intended.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [Preview inline, Inline preview, ServiceNow AI Experience Lab for VS Code, Preview page]
---

# Preview a page

Test that your page appears and functions as intended.

## About this task

Certain pages aren't previewable in the ServiceNow® AI Experience Lab for VS Code extension and must be previewed by deploying to your instance. To learn about deploying, see [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md).

## Before you begin

Role required: none

The ServiceNow® AI Experience Lab for VS Code extension requires the following:

<table id="table_imf_rfb_dkc"><thead><tr><th>

Application

</th><th>

Version

</th><th>

Resources for more information

</th></tr></thead><tbody><tr><td>

Visual Studio Code

</td><td>

1.97 later

</td><td>

[Visual Studio Code updates](https://code.visualstudio.com/updates/v1_132)

</td></tr><tr><td>

Node.js

</td><td>

24 or later

</td><td>

[Node.js](https://nodejs.org/en/download)

</td></tr><tr><td>

pnpm

</td><td>

10 or later

</td><td>

[pnpm](https://pnpm.io/installation)

</td></tr><tr><td>

ServiceNow SDK

</td><td>

4.10 or later

</td><td>

[ServiceNow SDK](https://www.npmjs.com/package/@servicenow/sdk)

</td></tr><tr><td>

ServiceNow instance

</td><td>

-   Australia Patch 5 or later
-   Zurich Patch 12 or later

</td><td>

[Prepare your upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/rn-prepare-landing-page.md)

</td></tr></tbody>
</table>## Procedure

1.  Open a ServiceNow® AI Experience Lab for VS Code project in Visual Studio Code.

2.  In the Explorer panel, navigate to the /pages folder.

3.  Select the expand icon for the page that you want to preview.

4.  Right click or select and hold the page.js file that you want to preview and select **AIUX: Launch Preview**.

    A preview of your page appears. You can preview how your page appears on different devices, expand the preview panel, and interact with page elements.


## What to do next

If your page isn't already accessible from other pages, [add the page to the navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/add-page-to-navigation-servicenow-ai-experience-lab-for-vs-code.md). Otherwise, you can [deploy your changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md).

