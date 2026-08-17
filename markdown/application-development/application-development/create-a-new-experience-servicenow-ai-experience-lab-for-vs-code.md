---
title: Create a new experience
description: Develop ServiceNow® AI Experience Lab for VS Code experiences from scratch.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 2
keywords: [ServiceNow AI Experience Lab for VS Code, Create experience, ServiceNow AI Experience Framework]
---

# Create a new experience

Develop ServiceNow® AI Experience Lab for VS Code experiences from scratch.

## About this task

This procedure describes how to create net new experiences. To create an experience that extends an existing application, see [Extend an existing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/extending-existing-experience-servicenow-ai-experience-lab-for-vs-code.md).

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

1.  Navigate to Visual Studio Code.

2.  Select the ServiceNow \[Omitted image "servicenow-youmoji-icon.png"\] icon in the side panel to open the ServiceNow® AI Experience Lab for VS Code extension.

3.  On the home page, select **+ New project**.

    \[Omitted image "servicenow-ai-experience-new-project.png"\] Alt text: Select + New project to create an experience in ServiceNow® AI Experience Lab for VS Code.

4.  Select the instance that you want to deploy changes to.

    During ServiceNow® AI Experience Lab for VS Code extension setup, you connect to the instance that contains the files you want to access and where you want to preview and deploy changes. For more information or to connect another instance, see [Connect ServiceNow® AI Experience Lab for VS Code extension to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/connect-servicenow-ai-experience-lab-for-vs-code-to-instance.md).

5.  Select the location where you want your want your project to live on your local drive.

6.  Enter a name for your experience and then select the Enter key.

7.  Enter a name for the folder for your experience and then select the Enter key.

8.  From the list, select the option **Standalone App**.

9.  Enter a name for your application scope and then select the Enter key.

    ServiceNow® AI Experience Lab for VS Code extension scaffolds your experience. Once created, Visual Studio Code reloads with your experience files loaded.


## Result

Your new experience is created. Inside your experience, you can see sample pages, widgets, and other ServiceNow® AI Experience Lab for VS Code experience metadata.

## What to do next

Start creating pages and widgets within your experience. For more information, see [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-page-servicenow-ai-experience-lab-for-vs-code.md).

