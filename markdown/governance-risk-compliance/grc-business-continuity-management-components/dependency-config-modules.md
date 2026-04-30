---
title: Dependency Configuration records
description: The BCM administrators configure the Dependency Configuration records.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Dependency Configuration records

The BCM administrators configure the Dependency Configuration records.

Administrators configure the Dependency Configuration records in the administrator view \(UI 16 view\) to schedule an auto-update of the BIA dependencies, related assets, and sources based on the source data and relationships in the CMDB.

**Note:** Beginning with the Xanadu release, you can access up-to-date information on dependencies related to Business Impact Analysis, Plans, and Events. To access the most recent updates for dependencies, choose **All records** or **Latest record only** from the **Source records to consider** option in the Impact analysis dependency update configuration, Planning dependency update configuration, and Event dependency source configuration records. Based on your selection, the application pulls dependencies from all sources or only from the latest record for each source.

The example shows the Planning dependency update configuration record.

![Updating the BCP dependencies.](../image/plan-dep-update-config.png)

Consider an example where you have 2 BIAs done on Acrobat and the configuration is shown in the example. When **All records** option is selected and you select **Update dependencies** UI action from the plan record, the application pulls all the dependencies in all BIA records that satisfy the requirement. As shown in the example, dependencies of both BIA Latest and BIA Old records are pulled into the plan.

![Source records.](../image/source-records-dep-update-config.png)![All BIA.](../image/all-bia-records.png)

When **Latest record only** option is selected and you select **Update dependencies** UI action from the plan record, the application considers one of the records of the two BIAs and it fetches the dependency assessment of that BIA record.

![Latest BIA.](../image/latest-bia.png)![Dependency assessment from latest BIA.](../image/dep-assmt-latest-bia.png)

For the **Update dependencies** UI action in the plan record and the **Update BCP dependencies snapshot** scheduled job to function, it is necessary to have the Impact analysis dependency update configuration, Planning dependency update configuration, and Event dependency source configuration records established.

## Pulling latest dependency updates for impact analysis, plans, and events

You can pull latest dependency updates for impact analysis, plans, and events. Choosing All records or Latest record only functionality is applicable for Impact analysis dependency update configuration, Planning dependency update configuration, and Event dependency source configuration records.

For Impact analysis dependency updates, pulling all BIA records or the latest BIA record may yield the same information. For planning dependency updates and event dependency updates, pulling all BIA records or the latest BIA record pulls the latest dependency updates.

Dependencies are fetched from these sources for the plans:

-   BIA upstream dependency
-   BIA downstream dependencies
-   CMDB

Dependencies are fetched from these sources for the events:

-   BIA upstream dependency
-   BIA downstream dependencies
-   CMDB
-   Plan primary assets
-   Plan related assets

For information on configuring the impact analysis dependency updates, see [Configuring impact analysis dependency updates](imp-ana-dep-update-config-module.md).

For information on configuring the planning dependency updates, see [Configuring planning dependency updates](confi-planning-dep-updates.md).

For information on configuring the sources for adding the event dependencies, see [Configuring sources for adding event dependencies](configuring-event-dep-updates.md).

-   **[Configuring impact analysis dependency updates](imp-ana-dep-update-config-module.md)**  
The BCM administrators configure the Impact analysis dependency update configuration record so that an auto-update of the BIA dependencies can be scheduled based on the source data and relationships in the CMDB.
-   **[Configuring planning dependency updates](confi-planning-dep-updates.md)**  
The BCM administrators configure the Planning dependency update configuration record so that an auto-update of the related assets in the plans can be scheduled based on the source data and relationships in the CMDB and BIA.
-   **[Configuring sources for adding event dependencies](configuring-event-dep-updates.md)**  
The BCM administrators configure the sources in the Event dependency source configuration record so that the impacted assets are added in the events and exercises based on the source data and relationships in the BIA, CMDB, and plans.

**Parent Topic:**[General administration setup for BCM](set-up-bcm-bcmadmin-tasks.md)

