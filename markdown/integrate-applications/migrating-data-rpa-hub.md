---
title: Migrating data in RPA Hub
description: Learn how to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RPA Hub, Workflow Data Fabric]
---

# Migrating data in RPA Hub

Learn how to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment.

-   **[Restructuring RPA Hub tables](restructured-rpa-hub-tables-utah.md)**  
Starting with the Utah release, the Robotic Process Automation \(RPA\) tables are restructured to an application file, so that changes that you make to these tables are captured in the update sets and can be moved seamlessly across environments. With this process, you don't have to re-create the data records in the targeted environment.
-   **[Verify the associated schedules, parameters, packages, and queues in RPA Hub](../task/verify-botprocess-tasks.md)**  
Verify that the bot process has the associated schedule, process parameters, shared parameters, package, package version, and work queues in RPA Hub. You do this task when you’re migrating your data from a lower \(non-production\) environment to a higher \(production\) environment.
-   **[Migrating your data from a lower environment to a higher environment in RPA Hub](migrate-data-rpa-hub.md)**  
As a system administrator, after you restructure the RPA Hub tables to extend the Application file \(sys\_metadata\), you can use the update set capability to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment for real-time use.
-   **[Migrating the bot process configuration in RPA Hub](bot-process-migration.md)**  
In RPA Hub, you can migrate the bot process configuration and associated assets for an attended or unattended bot process from one environment to another environment. With this feature, you can create an automation and test it in a lower environment and then migrate it to a higher or production environment.

**Parent Topic:**[Workflow Data Fabric](../../../build/create-integrations-apps/concept/create-integrations-applications.md)

