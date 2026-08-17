---
title: Create a page
description: Create a page using the ServiceNow® AI Experience Lab for VS Code extension to create tailored experiences.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 2
keywords: [ServiceNow AI Experience Lab for VS Code, Create page, ServiceNow AI Experience Framework]
---

# Create a page

Create a page using the ServiceNow® AI Experience Lab for VS Code extension to create tailored experiences.

## About this task

This procedure describes how to create pages for new experiences. To create a page that extends an existing experience, see [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-page-existing-servicenow-ai-experience-lab-for-vs-code.md).

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

1.  In the ServiceNow® AI Experience Lab for VS Code extension, create an experience or open an existing experience.

    For information about creating an experience, see [Create a new experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-a-new-experience-servicenow-ai-experience-lab-for-vs-code.md).

2.  In your experience, create a page.

    -   Create a page manually in the explorer panel.
        1.  Select the /pages folder.
        2.  With the /pages folder highlighted, select the create folder icon \[Omitted image "create-folder-icon.png"\] Alt text: or right click and select **New folder**.
        3.  Enter a name for the new folder and select the Enter key.
        4.  In the new folder, select the create file icon \[Omitted image "create-file-icon.png"\] Alt text:or right click in the folder and select **New file**.
    -   Create a page using the command palette.
        1.  Access the command palette by pressing Ctrl+Shift+P on Windows or Command+Shift+P on macOS, or by navigating to **View** &gt; **Command Palette**.
        2.  Select **AIUX: Create page**.
    -   Create a page conversationally using Claude Code or your preferred AI tool.
        1.  Open the panel for your preferred AI tool.
        2.  Enter a prompt describing the page that you want to create.

            For example, `Create a new page in my example-experience project.`

3.  Enter a name for the page and select the Enter key.

4.  Enter a URL route for the new page and select the Enter key.

    After entering the URL route, the ServiceNow® AI Experience Lab for VS Code extension creates the folder and page file using the information you provided.


## Result

Your new page is created. You can now add elements to the page and preview as needed.

## What to do next

-   [Preview a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/preview-page-servicenow-ai-experience-lab-for-vs-code.md)
-   [Add a page to the navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/add-page-to-navigation-servicenow-ai-experience-lab-for-vs-code.md)
-   [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md)

