---
title: Builders in ServiceNow Studio
description: Builders are specialized tools that provide an intuitive and efficient interface for editing metadata records primarily associated with tables extending sys\_metadata. In ServiceNow Studio, you can use builders to create a variety of file types to support your app development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/builders-in-servicenow-studio.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Builders in ServiceNow Studio

Builders are specialized tools that provide an intuitive and efficient interface for editing metadata records primarily associated with tables extending sys\_metadata. In ServiceNow Studio, you can use builders to create a variety of file types to support your app development.

Builders focus on enhancing user experience by offering features such as inline editing, customizable views, and integrated collaboration. Each builder remains agnostic of design libraries or implementations, ensuring adaptability to evolving technologies and frameworks.

When you open files like decision tables, flows, or tables in ServiceNow Studio, the files open in an integrated tab in their designated builder tool. Some other file types like mobile app configurations open in a new browser tab. Note that you must create or open a file or application to access a builder. You cannot open builders on their own in ServiceNow Studio.

For a full list of the builders integrated in ServiceNow Studio, see [Integrated development tools for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/integrated-development-tools.md).

## How builders open in ServiceNow Studio

Decision tables and many other types of automations open in integrated tabs.

\[Omitted image "sn-studio-builder-decision-table.png"\] Alt text: Decision tables are built in the Workflow Studio builder.

Mobile App Builder opens in a new tab.

\[Omitted image "sn-studio-builder-mobile.png"\] Alt text: When you open Mobile App Builder, it opens in a new browser tab.

When you open some tools like Table Builder, you may see a short tutorial to help you learn the tool.

\[Omitted image "sn-studio-builder-tutorial.png"\] Alt text: Some builders have a short tutorial that helps you learn the tool.

## Builders and application scope

When you're editing files in ServiceNow Studio, note that some builders such as Table Builder and UI Builder may not automatically update the scope of your application and need to be changed manually.

