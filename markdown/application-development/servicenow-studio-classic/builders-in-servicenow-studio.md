---
title: Builders in ServiceNow Studio
description: Builders are specialized tools in ServiceNow Studio for editing metadata records associated with tables that extend sys\_metadata. Use builders to create and edit file types such as decision tables, flows, and forms as part of your app development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/builders-in-servicenow-studio.html
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

For a full list of the builders integrated in ServiceNow Studio, see [Integrated development tools for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/integrated-development-tools.md).

## How do builders open in ServiceNow Studio?

Decision tables and most other automation file types open in new tabs.

\[Omitted image "sn-studio-builder-dt-as1.png"\] Alt text: Decision tables open in the Workflow Studio builder.

Mobile App Builder opens in a new tab.

\[Omitted image "sn-studio-builder-mobile.png"\] Alt text: When you open Mobile App Builder, it opens in a new browser tab.

Some builders, such as Table Builder, display a short tutorial when you first open them.

\[Omitted image "sn-studio-builder-tutorial.png"\] Alt text: Some builders display a short tutorial when you first open them.

## How does scope work with builders?

Some builders override automatic scope switching. For example, when you use Table Builder to edit a form or table file, a message indicates that the scope is controlled by the builder.

\[Omitted image "sn-studio-scope-builder.png"\] Alt text: Some builders control the scope for apps open in ServiceNow Studio.

