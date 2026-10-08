---
title: Instance explorer
description: The Instance Explorer is the Lux Lab connection point to your ServiceNow instance. Use it to connect to an instance, browse its tables for quick data lookups, and switch between instances without leaving the app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/instance-explorer.html
release: brazil
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Instance explorer, Instance switcher, Instance Explorer panel, Instance connections, Instance status indicators]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Instance explorer

The Instance Explorer is the Lux Lab connection point to your ServiceNow instance. Use it to connect to an instance, browse its tables for quick data lookups, and switch between instances without leaving the app.

## Instance switcher

The active instance appears in the top header bar of Lux Lab. Selecting the instance name opens the instance switcher, where you can do the following:

-   See all connected instances
-   Switch the active instance in one step
-   Add a new instance connection

## Instance Explorer panel

To open the dedicated panel, select the **Instance Explorer** icon in the Activity Bar. In the panel, you can browse ServiceNow tables and perform quick data lookups in the following ways:

-   Expand a table to see its records.
-   Search for specific tables or records using the search bar at the top of the panel.
-   Use the data as a reference while building your Lux application.

The panel provides lightweight, read-only data lookup during development. It does not function as a full record editor.

**Note:** To import an existing application into a new project, use the **Import** option in the New Project dialog. See [Create an experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-a-new-experience.md).

## Instance connections

For the full connection procedure, see [Connect Lux Lab to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/connecting-lux-lab-to-an-instance.md).

To switch the active instance, select the instance name in the top header bar, then select the instance you want to make active. Lux Lab uses the active instance for deployments, previews, and table browsing.

## Instance status indicators

The following table describes what each status indicator means.

|Indicator|Meaning|
|---------|-------|
|Green dot|Connected and responsive|
|Yellow dot|Connected but slow or degraded|
|Red dot|Connection failed or timed out|
|Gray dot|Disconnected|

