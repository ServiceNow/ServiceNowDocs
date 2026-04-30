---
title: Contextual search plugin
description: The Contextual Search plugin \(com.snc.contextual\_search\) is activated by default in the base system. This plugin activates related plugins if they aren't already active.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Contextual search plugin, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Contextual search plugin

The Contextual Search plugin \(com.snc.contextual\_search\) is activated by default in the base system. This plugin activates related plugins if they aren't already active.

## Before you begin

Role required: admin

## About this task

If the related plugins aren't activated, Contextual Search activates the plugins.

<table id="table_zxy_fff_qgb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON Service request/response model\[com.snc.application.json\_service\]

</td><td>

Core components and helpers for a JSON request/response model. Includes JSON and XML transports for NG and GlideAjax support. An extension of the processor framework.

</td></tr><tr><td>

Contextual Search — Internal\[com.snc.contextual\_search.internal\]

</td><td>

An internal plugin component for Contextual Search.

</td></tr><tr><td>

GraphQL Schema for Contextual Search\[com.snc.contextual\_search.graphql\]

</td><td>

Provides GraphQL schema for contextual search services.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Contextual Search](../reference/components-installed-with-cxs.md)**  
Several types of components are installed with the activation of the Contextual Search plugin \(com.snc.contextual\_search\), including tables and user roles.

**Parent Topic:**[Contextual search plugin](../concept/contextual-search-plugins.md)

**Related topics**  


[List of plugins \( Yokohama \)](../../plugins/reference/list-of-plugins.md#)

