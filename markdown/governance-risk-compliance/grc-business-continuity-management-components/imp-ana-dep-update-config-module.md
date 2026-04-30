---
title: Configuring impact analysis dependency updates
description: The BCM administrators configure the Impact analysis dependency update configuration record so that an auto-update of the BIA dependencies can be scheduled based on the source data and relationships in the CMDB.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configuring impact analysis dependency updates

The BCM administrators configure the Impact analysis dependency update configuration record so that an auto-update of the BIA dependencies can be scheduled based on the source data and relationships in the CMDB.

## Impact analysis dependency update configuration record

The BCM administrators access the Impact analysis dependency update configuration record by navigating to **General Administration** in the application UI. The record contains the configuration details such as the name, order, target records, sources, and notification preferences as shown in the following example.

![Impact analysis dependencies update.](../image/impact-ana-dep-update-config.png)

## Configure the sources for adding the dependencies

Configure the sources in the Impact Analysis dependency update configuration record to retrieve the latest BIA dependencies. As shown in the example, select the CMDB source to read dependencies from the Configuration Management Database. The BIA's **Applies to** field specifies the input asset. The system retrieves dependencies from the CMDB based on the asset defined in the BIA.

**Note:** You can fetch the latest dependencies of the BIAs from the CMDB relationships only.

## Auto-update the dependencies and set the notification preferences

The BCM administrators select the **Auto-update dependencies** option to schedule an auto-update of the dependencies in the BIAs.

The BCM administrators select the **Send notification** option to notify the BIA owners about the updated dependencies. The email notification contains the details of the dependency updates for the BIA records as shown in the following example.

![Email preview.](../image/bia-email-preview.png)

The snapshot records are displayed in the Pending updates record of the BIA from the list view. The delta snapshot record displays details of the BIA and updated dependency configuration such as Added, Updated, and Deleted assets for the BIA.

BIA owners then update the CMDB assets and dependencies manually by selecting the **Update dependencies** UI action displayed in the Dependency assessment of the BIA. The BIA owners or BIA approvers then review the dependency updates and save the changes to the BIA.

For more information on configuring the Impact analysis dependency update configuration record, see [Set up Impact analysis dependency update configuration](../task/configure-imp-ana-dep-update-module.md).

-   **[Set up Impact analysis dependency update configuration](../task/configure-imp-ana-dep-update-module.md)**  
Configure the Impact analysis dependency update configuration record to configure the BIA record \(for which the dependencies are updated\), its target records, sources, and notification preferences.

**Parent Topic:**[Dependency Configuration records](dependency-config-modules.md)

