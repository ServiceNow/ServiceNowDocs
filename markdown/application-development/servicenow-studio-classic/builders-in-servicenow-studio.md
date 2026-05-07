---
title: Builders in ServiceNow Studio
description: Builders are specialized tools in ServiceNow Studio for editing metadata records associated with tables that extend sys\_metadata. Use builders to create and edit file types such as decision tables, flows, and forms as part of your app development.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Builders in ServiceNow Studio

Builders are specialized tools in ServiceNow Studio for editing metadata records associated with tables that extend sys\_metadata. Use builders to create and edit file types such as decision tables, flows, and forms as part of your app development.

Builders provide features such as inline editing, customizable views, and integrated collaboration. Each builder is independent of specific design libraries or implementations, so it adapts to different technologies and frameworks.

When you open files such as decision tables, flows, or tables in ServiceNow Studio, the files open in a new tab in their designated builder. Some file types, such as mobile app configurations, open in a new browser tab. To access a builder, you must first open a file or application — builders cannot be opened independently in ServiceNow Studio.

For a full list of the builders integrated in ServiceNow Studio, see [Integrated development tools for ServiceNow Studio](integrated-development-tools.md).

## How do builders open in ServiceNow Studio?

Decision tables and most other automation file types open in new tabs.

![Decision tables open in the Workflow Studio builder.](../image/sn-studio-builder-dt-as1.png)

Mobile App Builder opens in a new tab.

![When you open Mobile App Builder, it opens in a new browser tab.](../image/sn-studio-builder-mobile.png)

Some builders, such as Table Builder, display a short tutorial when you first open them.

![Some builders display a short tutorial when you first open them.](../image/sn-studio-builder-tutorial.png)

## How does scope work with builders?

Some builders override automatic scope switching. For example, when you use Table Builder to edit a form or table file, a message indicates that the scope is controlled by the builder.

![Some builders control the scope for apps open in ServiceNow Studio.](../image/sn-studio-scope-builder.png)

