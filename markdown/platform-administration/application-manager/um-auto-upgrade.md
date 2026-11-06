---
title: Auto-upgrade
description: The auto-upgrade mechanism automatically upgrades ServiceNow-managed applications and plugins across your instances on a regular schedule without requiring manual intervention. Auto-upgrade applies exclusively to ServiceNow-managed applications and plugins; third-party applications aren't included in automatic upgrades.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/application-manager/um-auto-upgrade.html
release: australia
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2026-09-17"
reading_time_minutes: 1
breadcrumb: [Updating apps, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Auto-upgrade

The auto-upgrade mechanism automatically upgrades ServiceNow-managed applications and plugins across your instances on a regular schedule without requiring manual intervention. Auto-upgrade applies exclusively to ServiceNow-managed applications and plugins; third-party applications aren't included in automatic upgrades.

Auto-upgrade enables continuous delivery of ServiceNow-managed applications and plugins by automating the upgrade process, eliminating the need for your manual intervention. The system automatically schedules and installs upgrades at optimal times. This keeps your applications current with minimal effort.

## Key benefits

The auto-upgrade feature provides the following benefits:

-   Enables continuous delivery of ServiceNow-managed applications or plugins by removing the bottleneck of your initiated action.
-   Distributes installation load across the platform infrastructure by randomizing upgrade schedules within a 24-hour window.
-   Orchestrates multiple application or plugin upgrades in batches, reducing the number of installation operations across instances.

## How it works

The auto-upgrade mechanism operates through a combination of polling, scheduling, and batch orchestration to upgrade applications or plugins automatically:

-   Automated polling: Your instances poll the API every 2 hours to check for pending SN-managed application or plugin upgrades. When new upgrades are available, the system automatically schedules installations.
-   Blackout window enforcement: Control automated polling with blackout windows and system properties. The system honors your configured high-usage periods \(for example, Monday through Friday, 9 AM to 5 PM\) during which no automated installations occur. Instance upgrade schedules are treated as implicit blackout periods to prevent conflicts. You can manage polling frequency and auto-upgrade controls using three system properties in System Properties:
    -   sn\_app\_auto\_upgr.enabled

        **Note:** Automatic upgrades are enabled by default to keep your SN-managed applications current and secure.

    -   sn\_appclient.scheduled\_jobs\_config \(polling frequency and operational settings\)
    -   sn\_app\_auto\_upgr.platform\_upgrade\_lookahead\_hours \(platform upgrade detection window\)
-   Environment targeting: Application business units specify whether a release targets non-production environments, production environments, or both. Custom target dates can be configured beyond the default 24-hour window.

**Parent Topic:**[Updating applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/application-manager/updating-apps-app-manager.md)

