---
title: Create and configure a custom artifact
description: Create and configure custom artifacts of your choice to use the Localization Framework functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-framework/create-configure-custom-artifact.html
release: australia
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Artifact configurations, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create and configure a custom artifact

Create and configure custom artifacts of your choice to use the Localization Framework functionality.

## Before you begin

Ensure that you are in the application scope that you want for your custom artifact.

Role required: localization\_admin and script\_include\_admin.

## About this task

From the Zurich release, your custom artifacts can be made available in [Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/localization-workspace.md). For information about making custom artifacts selectable in Localization Workspace translation requests, see [Dynamic artifact detection in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-dynamic-artifact-detection.md).

## Procedure

1.  Ensure that you are in the application scope that you want for your custom artifact, and navigate to **All** &gt; **Localization Framework** &gt; **Artifact Configurations** \[sn\_lf\_config\].

2.  Select **New**.

3.  In the Artifact Configuration form, fill in the fields.

<table id="table_uly_1hv_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifier of the artifact record.

</td></tr><tr><td>

Internal name

</td><td>

An internal name for the artifact.

</td></tr><tr><td>

Table name

</td><td>

Identifier of the table where information of the artifact is stored. For example, Catalog Items \[sc\_cat\_item\] table.

</td></tr><tr><td>

Processor script

</td><td>

Extracts the translatable content associated with the translation request and saves the translations into the database.You can select a script include using the search \[Omitted image "magnifying\_glass.png"\] Alt text: magnifying glass icon icon, or you can create a new script include.The processor script contains the following functions:

-   getTranslatableContent: Extracts the translatable content.
-   saveTranslatedContent: Saves the translated content back to the system.
For more information, see [Processor script functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/processor-script-functions.md).To create a new processor script for the artifact, see [Create a processor script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/create-processor-script.md).

**Note:** Under **Related Links** on an existing artifact record, you can switch to **Legacy View** for script editing.

</td></tr><tr><td>

Application

</td><td>

Application scope. The value is the current application selected for the logged-in user session. For more information, see [Select an application from the application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_SelectAnAppFromTheAppPicker.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the configuration record.

</td></tr><tr><td>

Generate insights

</td><td>

Option to turn on or turn off the localization insights for the artifact. For more information, see [Localization Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/localization-insights-dashboard.md).

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

For examples of Localization Framework artifacts that you can set up, see the LF Artifact blog posts list on [https://www.servicenow.com/community/international-localization/need-to-translate-a-par-dashboard-check-this/ta-p/2839751](https://www.servicenow.com/community/international-localization/need-to-translate-a-par-dashboard-check-this/ta-p/2839751) in the ServiceNow Community. These examples include Processor scripts.

**Parent Topic:**[Artifact configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/framework-configuration.md)

