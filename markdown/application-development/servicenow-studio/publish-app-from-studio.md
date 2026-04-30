---
title: Legacy - Publish an application from ServiceNow Studio when linked to Source Control
description: You can publish a custom application from ServiceNow Studio when linked to Source Control.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Publish an application from ServiceNow Studio when linked to Source Control

You can publish a custom application from ServiceNow Studio when linked to Source Control.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin

## About this task

When you publish an application from ServiceNow Studio that is linked to Source Control, there is a different outcome than when you publish via the sys\_app or sys\_store\_app **Publish** related link.

## Procedure

1.  When you select **Publish**, the sys\_app or sys\_app\_customization record for the application is updated with the new version.

2.  The current state of the application is committed to Source Control, including any untracked or uncommitted changes.

    The value of the **glide.sourcecontrol.default\_commit\_mode** property is ignored.

    This occurs because when the application is published, all the untracked and uncommitted changes are also published. Therefore, the state of the application in the Git repository matches what is published. See the [Legacy - Commit changes](t_CommitChanges.md) topic for more information about the **glide.sourcecontrol.default\_commit\_mode** property.

3.  A Source Control tag is created for the new version and the application is published.

    If needed, the sys\_app record is updated with the new store correlation ID.

    **Note:** If your application is linked to Source Control and you publish a new version outside of Studio, a source control commit and tag are not created.


**Parent Topic:**[Legacy - ServiceNow Studio](../concept/c_ServiceNowStudio.md)

