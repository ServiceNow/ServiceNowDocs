---
title: Embed the playbook in Service Portal
description: Add a playbook that Service Portal users can launch and run by creating a Playbook Content Item.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Playbooks in Service Portal, Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Embed the playbook in Service Portal

Add a playbook that Service Portal users can launch and run by creating a Playbook Content Item.

## Before you begin

-   Role required: admin, or portal admin
-   If you don't have a playbook that you want to customize for Service Portal yet, build one in Workflow Studio. To learn more about building a playbook in Workflow Studio, see [Building playbooks](../concept/building-a-process.md).
-   Create a record generator, if there isn't already one you want to use. To learn more about creating a playbook record generator, see [Playbook record generator](../../workspace/concept/playbook-record-generator-overview.md).
-   You may need to set up mappings between your Portal theme and the UXF theme, if they are very different. To set up mappings between your Portal theme and the UXF theme, see [Set up mappings between themes](set-up-mappings-between-themes.md).

## About this task

In a Playbook content item, the admin specifies the URL that points to the portal page.

## Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Content Items**.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the playbook.|
    |Active|Uncheck this box if you don't want users to be able to run the playbook in Service Portal.|
    |Catalogs|Enter the catalog that you want this playbook to be added to. There is no default, but the playbook is not searchable if you don't add it to a catalog.|
    |Category|Enter the catalog category that you want this playbook to be in. There is no default, but the playbook is not searchable if you don't pick a category for the playbook.|
    |Icon|Upload a small image that appears next to the name when the item is displayed in the service catalog. Supported file types are jpg, png, bmp, gif, and jpeg.|
    |Application|Choose an application scope that you want your Service Portal playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).|
    |Picture|Upload an image showing the item. Supported file types are jpg, png, bmp, gif, and jpeg.|
    |Short description|Enter some descriptive details about your playbook.|
    |Table|Enter the parent table that the playbook opens on. If not specified, defaults to the Incident table.|
    |Record ID|Enter the parent Sys ID of the record you want to open in the record generator table. If you want to use the record generator, leave it as -1. If not specified, defaults to -1.|
    |Playbook Experience|Choose the playbook experience record with the playbook configurations that you want for your Service Portal users. If not specified, defaults to the Global Playbook Experience.|
    |Playbook Experience Record Generator|Choose the record generator with the playbook that you want to show.|
    |Portal Page|Enter a Service Portal page that you want to open the playbook in. If not specified, the playbook is launched in the out-of-the-box Playbook Portal page.|
    |Title|Add a title for any components that use the title property in the Portal Playbook widget's UI Builder page.|
    |Meta|Add tags to the playbook item for Service Portal home screen searches.|


For issues that seem like process execution related, check the execution logs on the sys\_pd\_context that is related to the process that was run. You can find these in the "today's executions" module within the navigator.

For issues that are flow designer related, debug using the flow debugger options​. To learn more about flow debugger options, see \[an article linked to debugging flows\].

For other issues:

-   Check the instance logs around the execution time of the sys\_pd\_context records and see if you can find any errors that seem related \(record watchers, flow exceptions, or any other exceptions seeming relevant\).
-   Make sure versions of playbook are as follows:​
    -   now-playbook-experience version 25.1.4 or greater​
    -   playbook-experience version 25.1.2 or greater​
-   Verify that you are using the out-of-the-box Portal Playbook widget.

## What to do next

Customize the runtime playbook experience in the Service Portal Designer.

-   **[Portal Playbook Widget](../reference/portal-playbook-widget.md)**  
Explore the Portal Playbook Widget.

**Parent Topic:**[Playbooks in Service Portal](../concept/playbooks-service-portal.md)

