---
title: Override an existing page
description: Have existing ServiceNow AI Platform experiences use pages that you create instead of base system pages.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [Override existing page, ServiceNow AI Experience Lab for VS Code]
---

# Override an existing page

Have existing ServiceNow AI Platform® experiences use pages that you create instead of base system pages.

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

5.  Enter the display name for the page you want to override and select the Enter key.

    **Important:** The display name must exactly match the display name for the page you're overriding, in order for the override to be successful. Pages that appear with the circle slash icon \[Omitted image "circle-slash-icon.png"\] Alt text:have already been overridden.

6.  Enter the URL route for the page you want to override and select the Enter key.

    **Important:** The URL route must exactly match the URL route for the page that you're overriding, in order for the override to be successful.

    After entering the URL route, the ServiceNow® AI Experience Lab for VS Code extension creates the folder and page file using the information you provided.


## Result

Your page is created. You can now add elements to the page and preview as needed.

## What to do next

To complete the override process, you must deploy your changes to your instance. For more information, see [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md).

