---
title: Create process configurations using content packs
description: Create process configurations using content packs to use the configuration already created for the content packs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/process-config-content-pack.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [With content pack templates, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Create process configurations using content packs

Create process configurations using content packs to use the configuration already created for the content packs.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the Process configurations icon \(\[Omitted image "icon-process-config.png"\] Alt text: Process configuration builder\).

3.  Select the **Content pack templates** tab.

    **Note:** Ensure that the content pack is installed from which you want to use the configurations.

4.  Open the table from the list.

    **Note:** You will get the list of tables on which the content packs are created for all the content packs that are installed.

    \[Omitted image "process-config-cp.png"\] Alt text: Process configuration from content pack template

5.  Select the **Copy as process configuration** button.

    **Note:** Content pack configurations are not editable. You can copy them to your process configuration, but you cannot edit the content pack itself.

6.  Select **Create** on the dialog box that appears.

7.  Select the import button \[Omitted image "icon-import-cp.png"\] Alt text: Import preferences from content pack.

    If the content pack has any configuration, it is imported. When you select the import button, you are guided to first remove your original configuration for that particular field. Only then you can import the configurations from the content pack template. However, if in that section some fields are populated and some are not, then it will be clearly mentioned which values will be imported.

    **Note:** The content pack template does not overwrite your prior configuration for that table automatically.

8.  Configure the process table using the content pack template from the Process Configuration Builder.

    For more information, see [Create process configuration using Process Configuration Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/process-config-builder.md).


**Parent Topic:**[Creating process configurations using content pack templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/content-pack-config.md)

