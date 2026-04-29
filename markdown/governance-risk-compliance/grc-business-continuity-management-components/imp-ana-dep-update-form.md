---
title: Impact analysis dependency update configuration form
description: Use the Impact analysis dependency update configuration form to configure the details of the dependency updates such as the BIA record name, target records, sources, and notification preferences.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Impact analysis dependency update configuration, Configuring impact analysis dependency updates, Dependency Configuration records, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Impact analysis dependency update configuration form

Use the Impact analysis dependency update configuration form to configure the details of the dependency updates such as the BIA record name, target records, sources, and notification preferences.

## Impact analysis dependency update configuration record form

For the description of the field values, see the table.

|Field|Description|
|-----|-----------|
|Name|Name of the dependency update configuration rule.|
|Active|Option to select the active configurations. Active configurations are used to update the dependencies. Inactive configurations are retired.|
|Order|Field to identify the first configuration that is fulfilled by the record. The identified configuration is used to update the dependencies. Multiple configurations can be done for the same record. When the filter conditions are the same, the least order such as 0 takes the preference.|
|Target|
|Target table|Impact analysis \[sn\_bia\_analysis\] table that contains the BIA records. These records are updated according to the configuration set up in the Impact analysis dependency update configuration record.|
|Filter condition|Filter conditions to identify specific records in the target table. These records are updated according to the configuration set up in the Impact analysis dependency update configuration record.|
|Fields to be updated in the target table|Fields in the target record that can be updated with a specific value in addition to the dependencies.|
|Auto-update dependencies|Option to update the dependencies automatically. BCM administrators can specify if the updates should be done automatically or if a user review is needed before the update.|
|Sources|
|Sources|Applicable sources for adding dependencies to the impact analysis. For the BIA record, the source used is CMDB.|
|Source records to consider|Option to select a specific record or all records. When selecting source records from the specified sources, the system retrieves dependencies from either all matching records or only from the most recently matched BIA record.|
|Notification|
|Send notification|Option to notify the users or user groups on the updates.|
|Users/groups in fields|Option to select the users or groups fields in sn\_bia\_analysis who should receive a notification about the updates. For example, you can select the BIA owner and BCM lead to receive the updates.|

**Parent Topic:**[Set up Impact analysis dependency update configuration](../task/configure-imp-ana-dep-update-module.md)

