---
title: Exploring RPA Hub
description: Learn about the RPA Hub features that enable you to govern, manage, and supervise your digital workforce.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [RPA Hub, Workflow Data Fabric]
---

# Exploring RPA Hub

Learn about the RPA Hub features that enable you to govern, manage, and supervise your digital workforce.

## RPA Hub overview

Use RPA Hub to streamline automation processes, improve efficiency, monitor, and optimize your automation initiatives effectively.

By using multi-tenancy, you can create logical partitions to effectively manage your robots \(unattended and attended\) for different customers \(internal or external\) from a single instance. Each logical instance has its own access control list \(ACL\), robots, licenses, and execution logs.

## RPA Hub users

|User|Description|
|----|-----------|
|Release manager|Creates bot processes and robots in RPA Hub. Add developers to the Managed by group of the bot process so that they can customize the bot process. Configures and publishes the bot process.|
|Developer|Configures bot processes to assign business applications, robots, credentials, process parameters, schedules, and so on. Creates and deploys automations in a low-code environment. Manages data, schedules, work items, and other configuration parameters.|
|Support user|Identifies, diagnoses, and resolves the issues that are related to bot processes. Performs first-level troubleshooting. Publishes and manages a bot process.|

## RPA Hub workflow

The following illustration describes the basic tasks involved in creating an attended or unattended automation using RPA Hub. For detailed instructions, see [Configuring RPA Hub](rpa-hub-setup.md).

![Basic tasks related to configuring bot process. Infographic showing how release managers and developers create, test, and publish bot processes and how RPA support user manages bot process.](../image/rpa-hub-workflow-diagram.png "Creating automations using RPA Hub")

1.  As a release manager, create a bot process and define robots. Add developers to the Managed by group of the bot process so that the developer can continue to configure the bot process.
2.  As a developer, configure the bot process to associate a package, business applications, robots, parameters, and credentials so that robots can use them to run automations.
3.  As a developer, build automation packages, tests the automation projects, and handles exceptions in RPA Desktop Design Studio.
4.  As a developer, publish the configured bot process to execute, manage, and monitor automations.
5.  As a support user, diagnose, troubleshoot, and resolve issues with bot process and then publish the bot process.

## RPA Hub benefits

-   Enables you to deploy, monitor, manage, and verify the compliance of all robots at an enterprise level from a centralized location.
-   Manages the metadata that includes robots, packages, bot processes, queues, schedules, shared parameters, and alerts. For more information about these terms, see [Robotic Process Automation \(RPA\) Hub glossary](../reference/rpa-hub-glossary.md#).
-   Triggers unattended robots with the execution details.
-   Provides insights into the complete Robotic Process Automation \(RPA\) practice via a dashboard. From this dashboard, you can see the current execution status \(jobs and queues\) and event correlation between the various configuration items.

## What to explore next

To learn more about configuring and managing RPA Hub, see:

-   [Configuring RPA Hub](rpa-hub-setup.md)
-   [Using RPA Hub](managing-rpa-hub.md)
-   [RPA Hub reference](../reference/rpa-hub-reference.md)

**Related topics**  


[Internationalization support for RPA Hub](rpa-hub-international-language-support.md)

[Restructuring RPA Hub tables](restructured-rpa-hub-tables-utah.md)

[Migrating your data from a lower environment to a higher environment in RPA Hub](migrate-data-rpa-hub.md)

[Obtaining client authentication and code signing certificates for RPA Hub](../../rpa-core/concept/code-signing-certificate-rpa.md)

[Applying the CSDM guidelines to RPA Hub](../../rpa-core/concept/rpa-hub-apply-csdm.md)

[Domain separation and Robotic Process Automation \(RPA\) Hub](../../rpa-core/concept/domain-separation-rpahub.md)

[Migrating the bot process configuration in RPA Hub](bot-process-migration.md)

