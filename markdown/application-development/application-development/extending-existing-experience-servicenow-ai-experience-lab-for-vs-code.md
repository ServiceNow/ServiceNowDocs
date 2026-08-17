---
title: Extend an existing experience
description: Create an experience that extends an existing experience on the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 2
keywords: [Extend experience, ServiceNow AI Experience Framework, ServiceNow AI Experience Lab for VS Code]
---

# Extend an existing experience

Create an experience that extends an existing experience on the ServiceNow AI Platform®.

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

7.  From the list, select the option **Extend Existing App**.

8.  Select the name of the experience that you want to extend from the list.

    The list of experiences that can be extended are populated from the instance that you're connected to. Verify that the experiences you created and want to extend have been deployed to your instance.

9.  Enter a name for your application scope and then select the Enter key.

    ServiceNow® AI Experience Lab for VS Code extension scaffolds your experience. Once created, Visual Studio Code reloads with your experience files loaded.


## Result

Your extension experience is created. The pages for the experience are located under the `/src/extensions/<your-experience-scope-name>/your-experience-name` folder structure. When you create an extension experience, a sample page and widget are also created.

## What to do next

[Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-page-existing-servicenow-ai-experience-lab-for-vs-code.md) or [extend an existing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/extend-existing-page-servicenow-ai-experience-lab-for-vs-code.md) for your extension experience.

