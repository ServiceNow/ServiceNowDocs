---
title: Download and modify the manifest file for Employee Center for GCC-H or DoD
description: Download and modify the package file to provide the information that is required to make Employee Center available in your organization.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Employee Center with Microsoft Teams for GCC-H or DoD, Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Download and modify the manifest file for Employee Center for GCC-H or DoD

Download and modify the package file to provide the information that is required to make Employee Center available in your organization.

## Before you begin

Role required: admin

## About this task

To download, edit, and upload the manifest file, refer to this [Knowledge Base](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1430840) article.

## Procedure

1.  Download the `Employee_Center_Integration_With_Teams_For GCCH.zip` file from this [Knowledge Base](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1430840) article and extract its contents.

    The manifest zip file that you downloaded from the Knowledge Base article includes the following files:

    -   Color.png
    -   Manifest.json
    -   Outline.png
2.  Open the manifest.json file and replace **INSERT\_CLIENT\_ID** with your Application \(Client\) ID next to `id` under `version`, `id` under `webApplicationInfo`, and `botId` under `composeExtensions`.

3.  Replace **INSERT\_COMPLETE\_INSTANE\_URL** with your URL next to `contentUrl` and **INSERT\_COMPLETE\_INSTANE\_URL** next to `websiteUrl` under `staticTabs`.

4.  Customize the values of `packageName`, `short` name, `full` name, and **accent color** in the manifest file to re-brand your self-configured bot.

    If you would like to change the bot icon and outline icon, you can replace the color.png and outline.png files with your desired images.

    **Note:** Ensure that you have not changed the names for these files while uploading.

    For more information about image requirements, see [Microsoft documentation](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/apps-package).

5.  Add additional domains in the manifest file to preview content using the task module for content outside of the default ServiceNow domain, you can add additional domains in the manifest file.

    **Note:** By default, the manifest file already contains the ServiceNow domain under validDomains. It also includes a `true` attribute next to `"supportsFiles"`, which adds the file attachment icon in your Virtual Agent conversation. If you do not want to include additional domains for the content preview feature, you can skip this step.

6.  Save the updated files and compress the three files \(manifest.json, color.png, and outline.png\) into a new zip file.

    Select all three files and click **Compress** instead of compressing the folder itself.


**Parent Topic:**[Integrating Employee Center with Microsoft Teams for GCC-H or DoD](../concept/ec-teams-integration-gcch.md)

