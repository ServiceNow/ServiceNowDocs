---
title: Configuring planning dependency updates
description: The BCM administrators configure the Planning dependency update configuration record so that an auto-update of the related assets in the plans can be scheduled based on the source data and relationships in the CMDB and BIA.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring planning dependency updates

The BCM administrators configure the Planning dependency update configuration record so that an auto-update of the related assets in the plans can be scheduled based on the source data and relationships in the CMDB and BIA.

## Planning dependency update configuration record

The BCM administrators configure details of the plan record, its target records, sources, and notification preferences in the Planning dependency update configuration record as shown in the following example.

![Updating the plan dependencies.](../image/plan-dep-update-config.png)

## Configure the sources for fetching the dependencies

The BCM administrators configure the sources for fetching the latest dependencies of the plan from different sources such as BIA upstream dependency, BIA downstream dependencies, and CMDB.

**Note:** In the plans, the dependencies are fetched for all primary scope assets.

## Auto-update the dependencies

The BCM administrators can select the **Auto-update dependencies** option in the Target tab of the Planning dependency update configuration record to schedule an auto-update of the related assets in the plans.

## Set the notification preferences

The BCM administrators select the **Send notification** option to set the notification preferences for the plan owners. For every planning dependency update, an automated email is sent to the plan owners about the planning dependency updates and links to the updated snapshot records as shown in the example.

![Email notification.](../image/bia-preview-email.png)

The plan owner and BCM lead reviews the dependency updates from the snapshot record. The delta snapshot record displays the updated dependencies such as Added, Updated, and Deleted assets for the selected plan record.

For more information on configuring the Planning dependency update configuration record, see [Set up Planning dependency update configuration](../task/conf-plan-dep-update-confi-module.md).

-   **[Set up Planning dependency update configuration](../task/conf-plan-dep-update-confi-module.md)**  
Configure the Planning dependency update configuration record to configure the plan record \(for which the dependencies are updated\), its target records, sources, and notification preferences.

**Parent Topic:**[Dependency Configuration records](dependency-config-modules.md)

