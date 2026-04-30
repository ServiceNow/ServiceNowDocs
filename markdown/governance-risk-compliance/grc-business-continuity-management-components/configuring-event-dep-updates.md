---
title: Configuring sources for adding event dependencies
description: The BCM administrators configure the sources in the Event dependency source configuration record so that the impacted assets are added in the events and exercises based on the source data and relationships in the BIA, CMDB, and plans.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring sources for adding event dependencies

The BCM administrators configure the sources in the Event dependency source configuration record so that the impacted assets are added in the events and exercises based on the source data and relationships in the BIA, CMDB, and plans.

## Event dependency source configuration record

The Event dependency source configuration record contains the event dependency details such as the event record name, its target records, and sources as shown in the following example.

![Event dependency source configuration.](../image/event-dep-update-config-module.png)

Dependencies are incorporated into events from all sources through the selection of the **Update dependencies** UI action by the user. When an event is created and linked to a plan, the primary asset and its associated assets are automatically retrieved from the plan, provided that the Event Dependency Configuration is active and includes the plans in its Sources, without the need to select the **Update dependencies** UI action.

Dependencies are fetched from the following sources for the events:

-   BIA upstream dependency
-   BIA downstream dependencies
-   CMDB
-   Plan primary assets
-   Plan related assets

**Note:** In an event, the dependencies of all assets are added manually where the source is Manual.

For more information on configuring the Event dependency source configuration record, see [Configure Event dependency source configuration record](../task/conf-event-dep-source-confi-module.md).

-   **[Configure Event dependency source configuration record](../task/conf-event-dep-source-confi-module.md)**  
Configure the sources for adding the event dependencies in the Event dependency source configuration record.

**Parent Topic:**[Dependency Configuration records](dependency-config-modules.md)

