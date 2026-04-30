---
title: Activate Multi Provider Document Services Framework
description: You can activate the Multi Provider Document Services Framework plugin \(com.snc.multiprovider\_documents\) for Document Services if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Multi Provider Document Services Framework

You can activate the Multi Provider Document Services Framework plugin \(com.snc.multiprovider\_documents\) for Document Services if you have the admin role.

## Before you begin

Role required: admin

## About this task

The following items are installed with the Multi Provider Document Services Framework:

-   Plugin
-   Roles
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Multi Provider Document Services Framework plugin \(com.snc.multiprovider\_documents\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Multi Provider Document Services Framework](../concept/multi-provider-documents-framework.md)

**Related topics**  


[Installed with Multi Provider Document Services Framework](../reference/installed-with-multi-provider-framework.md)

[Microsoft OneDrive integration with Document Services](../concept/one-drive-integration.md)

[Google Drive integration with Document Services](../concept/google-drive-integration.md)

[Create provider details](create-provider-details-mp.md)

[Create document actions](create-document-actions.md)

[Create provider permissions](create-provider-permissions-mp.md)

[Configure permissions](configure-permissions-mp.md)

