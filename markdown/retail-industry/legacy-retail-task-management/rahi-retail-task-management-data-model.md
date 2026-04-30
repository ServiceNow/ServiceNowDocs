---
title: Retail Task Management Core data model
description: Learn about the Retail Task Management application by viewing the data model and role relationship diagrams. These diagrams show the relationships between the tables and roles within the application and provide an overall picture of how the Retail Task Management application operates.
locale: en-US
release: zurich
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Retail Task Management, Retail]
---

# Retail Task Management Core data model

Learn about the Retail Task Management application by viewing the data model and role relationship diagrams. These diagrams show the relationships between the tables and roles within the application and provide an overall picture of how the Retail Task Management application operates.

## Retail Task Management data model

![Retail Task Management core data model.](../image/rtmc-data-model.png)

Installing Retail Task Management Core introduces the **Affected retail stores** field into the Retail case \[sn\_retail\_case\] table.

The **Affected retail stores** field in the Retail case \[sn\_retail\_case\] table is used to generate affected retail stores within a list for the multiple case creation context.

## Changes introduced by the Multi-case creation framework plugin

Installing Retail Task Management Core automatically installs the Multi-case creation plugin, adding a new internal field child case creation status to track the state of child case creation. If child case creation is completed successfully, the main State field of the parent case is set to Open.

The Multi-case creation plugin also introduces a new internal table Affected Service Organizations. This table maintains a many-to-one mapping between Service Organizations \(SOs\) and Cases.

![Affected service organizations in Retail Task Management Core.](../image/rtmc-case-so-data-model.png)

**Note:** Both the child case creation status field and the Affected Service Organizations table are hidden from end users. They're only used internally by the multi-case engine to manage and track case creation processes.

![Multiple case creation config in the Retail Task Management Core data model.](../image/rtmc-mccc-data-model.png)

Installing the Multi-case creation plugin adds the Multiple case creation config field into the Service Definition table. This field references a new table, Multi Case Creation Config, which is also created during the plugin installation.

The Multi Case Creation Config table holds the necessary information for multiple case creations.

For more detailed information on how these fields are involved with the multi-store creation process, refer to [Configuring Retail Task Management](../concept/rahi-retail-task-management-configuring.md).

**Parent Topic:**[Retail Task Management reference](../concept/rahi-retail-task-management-reference.md)

