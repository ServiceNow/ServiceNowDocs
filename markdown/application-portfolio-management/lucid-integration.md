---
title: Enterprise Architecture \(formerly Application Portfolio Management\) integration with Lucidchart
description: Create enhanced architectural diagrams for your Business Applications and Business Capabilities in Lucidchart and access them from your ServiceNow instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture \(formerly Application Portfolio Management\) integration with Lucidchart

Create enhanced architectural diagrams for your Business Applications and Business Capabilities in Lucidchart and access them from your ServiceNow instance.

You can model your organization’s architecture in a visual way, by including the current and future state in the Lucidchart application. You can then associate these diagrams to Architectural Artifacts in Enterprise Architecture \(formerly APM\).

As an Enterprise Architect, use the integration to perform the following tasks:

-   Push a Business Application hierarchy to Lucidchart.
    -   Select the entities to be included in the chart.
    -   Customize the shapes and colors of the entities how they appear in the chart.
    -   Keep a reference of the diagram as an Architectural Artifact version.
    -   View and edit the diagrams in Lucidchart.
-   Push Business Capabilities maps to Lucidchart.
    -   Select one or more capabilities including their child capabilities and business applications to include in the chart.
    -   Keep a Lucidchart reference of the diagram as an Architectural Artifact version.

The Lucidchart integration enhances the Architectural Artifacts functionality to associate a Lucidchart diagram as a URL for an artifact. The current integration works only one way to push the diagrams from the ServiceNow instance and model them in Lucidchart.

To create a diagram in Lucidchart and associate it with an Architectural Artifact in Enterprise Architecture, you must install the following store applications from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):

-   [Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=lucidchart-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) - Helps to establish a connection between ServiceNow and Lucidchart. It provides an action to create Lucidchart diagrams in Enterprise Architecture. The Lucidchart Diagramming spoke requires creating a workspace and custom app in your Lucid account to generate OAuth 2.0 tokens to authenticate ServiceNow requests. Also, you must create a connection and credential record for the Lucidchart application to authorize the create diagram action from Enterprise Architecture. For detailed information, see [Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=lucidchart-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US), [Create OAuth 2.0 Client in Lucidchart](https://www.servicenow.com/docs/access?context=set-up-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US), and [Create a connection and credential alias for the Lucidchart diagramming spoke](https://www.servicenow.com/docs/access?context=create-conn-cred-lucidchart&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   Lucidchart Integration – Helps to create Business Application or Business Capability diagrams in Lucidchart. You can also configure the shapes and colors of the entities to appear in Lucidchart. Install the application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)

**Parent Topic:**[Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications](apm-integration.md)

