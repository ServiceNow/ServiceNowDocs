---
title: Activate Operational Sustainability Integration with Socialsuite
description: You can activate the Operational Sustainability Integration with Socialsuite plugin \(sn\_osm\_ma\) for Operational Sustainability Management if you have the admin role. The plugin enables you to import materiality assessment results from Socialsuite for reporting and compliance. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 2
breadcrumb: [Integrating Operational Sustainability Management with Socialsuite, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Activate Operational Sustainability Integration with Socialsuite

You can activate the Operational Sustainability Integration with Socialsuite plugin \(sn\_osm\_ma\) for Operational Sustainability Management if you have the admin role. The plugin enables you to import materiality assessment results from Socialsuite for reporting and compliance.

## Before you begin

Operational Sustainability Management requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

Tables and fields are installed with Operational Sustainability Integration with Socialsuite.

For more information on items installed with Operational Sustainability Management, see [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../reference/components-installed-with-esg.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Operational Sustainability Integration with Socialsuite plugin \(sn\_osm\_ma\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Configure the Material topic selection system property. Set the property to Socialsuite to enable the **Sync Topics** button and update the material topics visualization. For details, see [Set Material topic selection system property](../task/set-material-topic-selection-system-property.md).

**Parent Topic:**[Integrating Operational Sustainability Management with Socialsuite](integrate-operational-sustainability-with-SocialSuite.md)

