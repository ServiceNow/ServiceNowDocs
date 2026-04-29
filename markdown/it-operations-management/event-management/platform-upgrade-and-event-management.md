---
title: Event Management during a platform upgrade
description: During a platform upgrade Event Management jobs whose Upgrade safe flag is marked as true remain running.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management during a platform upgrade

During a platform upgrade Event Management jobs whose **Upgrade safe** flag is marked as `true` remain running.

During an upgrade of the platform, the Event Management connectors are working and continue to retrieve events. The events are being processed, transformed to an alert using event rules and if there is a suitable alert management rule, a task is created. However, the impact calculation is not supported during the platform upgrade. When applying configuration changes or upgrades, all impacted MID Servers restart.

**Note:** Event Management jobs that started running before the platform upgrade commenced continue to run during the upgrade.

The following Event Management jobs remain running as their **Upgrade safe** flag is marked as `true` :

-   Event Management - Connector execution
-   Event Management - Update stuck connect
-   Event Management - Alert Priority Queue
-   Event Management - Close flapping alerts
-   Event Management - Close threshold alert
-   Event Management - Evaluate Scoped Alert Rules Management0
-   Event Management - Maintenance Calculator
-   Event Management - Process events

During the platform upgrade, all other Event Management jobs wait for the platform upgrade to finish.

**Note:** During an Event Management plugin upgrade, all Event Management jobs do not work.

