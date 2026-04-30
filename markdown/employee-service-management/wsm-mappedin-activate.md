---
title: Install the Mappedin integration
description: Activate the Mappedin integration if you have the admin role.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Mappedin, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Install the Mappedin integration

Activate the Mappedin integration if you have the admin role.

## Before you begin

Role required: admin

## About this task

Mappedin is integrated with Workplace Service Delivery depending on the release version:

-   For the Rome and later releases, install the Workplace Service Delivery with Mappedin \(sn\_wsd\_mappedin\) plugin and the Mappedin plugin from store.

-   For the New York release with the full Workplace Service Delivery Suite \(sn\_wsd\_suite\) or just a few applications, ServiceNow Customer Service must first activate the following plugins:

    -   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
    -   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
    After these plugins are activated, activate Workplace Space Mapping \(sn\_wsd\_space\_map\).


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configure Mappedin](../concept/mappedin-integration-topics.md)

