---
title: Dependency Configuration records
description: The BCM administrators configure the Dependency Configuration records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/dependency-config-modules.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Dependency Configuration records

The BCM administrators configure the Dependency Configuration records.

Administrators configure the Dependency Configuration records in the administrator view \(UI 16 view\). They can schedule an auto-update of the BIA dependencies, related assets, and sources based on the source data and relationships in the CMDB.

**Note:** Beginning with the Xanadu release, you can access up-to-date information on dependencies related to Business Impact Analysis, Plans, and Events. To access the most recent updates for dependencies, choose **All records** or **Latest record only** from the **Source records to consider** option in the Impact analysis dependency update configuration, Planning dependency update configuration, and Event dependency source configuration records. Based on your selection, the application pulls dependencies from all sources or only from the latest record for each source.

The example shows the Planning dependency update configuration record.

\[Omitted image "plan-dep-update-config.png"\] Alt text: Updating the BCP dependencies.

Consider an example where you have 2 BIAs done on Acrobat and the configuration is shown in the example. When **All records** option is selected and you select **Update dependencies** UI action from the plan record, the application pulls all the dependencies in all BIA records that satisfy the requirement. As shown in the example, dependencies of both BIA Latest and BIA Old records are pulled into the plan.

\[Omitted image "source-records-dep-update-config.png"\] Alt text: Source records.\[Omitted image "all-bia-records.png"\] Alt text: All BIA.

When **Latest record only** option is selected and you select **Update dependencies** UI action, the application considers one BIA records and fetches its dependency assessment.

\[Omitted image "latest-bia.png"\] Alt text: Latest BIA.\[Omitted image "dep-assmt-latest-bia.png"\] Alt text: Dependency assessment from latest BIA.

The **Update dependencies** UI action in the plan record and the **Update BCP dependencies snapshot** scheduled job require specific configuration records. Establish the Impact analysis dependency update configuration, Planning dependency update configuration, and Event dependency source configuration records before use.

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

For information on configuring the impact analysis dependency updates, see [Configuring impact analysis dependency updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/imp-ana-dep-update-config-module.md).

For information on configuring the planning dependency updates, see [Configuring planning dependency updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/confi-planning-dep-updates.md).

For information on configuring the sources for adding the event dependencies, see [Configuring sources for adding event dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configuring-event-dep-updates.md).

-   **[Configuring impact analysis dependency updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/imp-ana-dep-update-config-module.md)**  
BCM administrators use the Impact analysis dependency update configuration record to schedule auto-updates of BIA dependencies. Updates are based on CMDB data.
-   **[Configuring planning dependency updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/confi-planning-dep-updates.md)**  
Configure the Planning dependency update configuration record to schedule auto-updates of related assets in plans based on CMDB and BIA source data.
-   **[Configuring sources for adding event dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configuring-event-dep-updates.md)**  
Administrators configure sources in the Event dependency source configuration record. Impacted assets are added to events and exercises based on source data and relationships in the BIA, CMDB, and plans.

**Parent Topic:**[General administration setup for BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/set-up-bcm-bcmadmin-tasks.md)

