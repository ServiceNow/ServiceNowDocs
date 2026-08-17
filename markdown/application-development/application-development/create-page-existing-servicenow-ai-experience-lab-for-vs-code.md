---
title: Create a page
description: Create a new page for an existing experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 2
---

# Create a page

Create a new page for an existing experience.

## About this task

The following procedure describes how to complete this task manually. You can also complete the task using agentic development tools, such as Claude Code.

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

1.  In the ServiceNow® AI Experience Lab for VS Code extension, open an experience that extends an existing experience.

    For more information about extending existing experiences, see [Extend an existing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/extending-existing-experience-servicenow-ai-experience-lab-for-vs-code.md).

2.  Access the command palette by pressing Ctrl+Shift+P on Windows or Command+Shift+P on macOS, or by navigating to **View** &gt; **Command Palette**.

3.  Select **AIUX: Create Page**.

4.  From the list, select **AIUX: New Page**.

    You can also create pages that extend existing pages. For more information, see [Extend an existing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/extend-existing-page-servicenow-ai-experience-lab-for-vs-code.md).

5.  Enter a display name for the page and select the Enter key.

    **Important:** The display name you enter must be unique. If the display name matches the name of another page in your extension experience, the new page will override the existing page with the same name. For more information about overriding pages, see [Override an existing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/override-existing-page-servicenow-ai-experience-lab-for-vs-code.md).

6.  Enter a URL route for the new page and select the Enter key.

    After entering the URL route, the ServiceNow® AI Experience Lab for VS Code extension creates the folder and page file using the information you provided.


## Result

Your new page is created. You can now add elements to the page and preview as needed. Certain pages aren't previewable in the ServiceNow® AI Experience Lab for VS Code extension and must be previewed by deploying to your instance.

## What to do next

-   [Preview a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/preview-page-servicenow-ai-experience-lab-for-vs-code.md)
-   [Add a page to the navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/add-page-to-navigation-servicenow-ai-experience-lab-for-vs-code.md)
-   [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md)

