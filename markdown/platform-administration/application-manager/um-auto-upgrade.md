---
title: Auto-upgrade
description: The auto-upgrade mechanism automatically upgrades ServiceNow-managed applications across your instances on a regular schedule without requiring manual intervention. Auto-upgrade applies exclusively to ServiceNow-managed applications; customer-customized or third-party applications aren't included in automatic upgrades.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/application-manager/um-auto-upgrade.html
release: zurich
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [Updating apps, Application Manager, Administering applications, Get started, Administer]
---

# Auto-upgrade

The auto-upgrade mechanism automatically upgrades ServiceNow-managed applications across your instances on a regular schedule without requiring manual intervention. Auto-upgrade applies exclusively to ServiceNow-managed applications; customer-customized or third-party applications aren't included in automatic upgrades.

Auto-upgrade enables continuous delivery of ServiceNow-managed applications by automating the upgrade process, eliminating the need for your manual intervention. Instead of waiting for you to manually upgrade each application, the system automatically schedules and installs upgrades at optimal times, keeping your applications current with minimal effort.

## Key benefits

The auto-upgrade feature provides the following benefits:

-   Enables continuous delivery of ServiceNow-managed applications by removing the bottleneck of your initiated action.
-   Distributes installation load across the platform infrastructure by randomizing upgrade schedules within a 24-hour window.
-   Respects your high-usage periods by enforcing blackout windows during configured times.
-   Orchestrates multiple application upgrades in batches, reducing the number of installation operations across instances.

## How it works

The auto-upgrade mechanism operates through a combination of polling, scheduling, and batch orchestration to upgrade applications automatically:

-   Automated polling: Your instances poll the API every 2 hours to check for pending SN-managed application upgrades. When new upgrades are available, the system automatically schedules installations within a 24-hour window of publication.
-   Blackout window enforcement: Control automated polling with blackout windows and system properties. The system honors your configured high-usage periods \(for example, Monday through Friday, 9 AM to 5 PM\) during which no automated installations occur. Instance upgrade schedules are treated as implicit blackout periods to prevent conflicts. You can manage polling frequency and auto-upgrade controls using three system properties in System Properties:
    -   sn\_app\_auto\_upgr.enabled \(master on/off switch\)
    -   sn\_appclient.scheduled\_jobs\_config \(polling frequency and operational settings\)
    -   sn\_app\_auto\_upgr.platform\_upgrade\_lookahead\_hours \(platform upgrade detection window\)
-   Batch install orchestration: New application upgrade requests are added to existing active batch install plans if the target installation window is still open. If the window has closed, a new batch is created. The system handles multiple applications in a single batch and includes retry logic for failed installations.
-   Environment targeting: Application business units specify whether a release targets non-production environments, production environments, or both. Custom target dates can be configured beyond the default 24-hour window.
-   Read-only enforcement: All ServiceNow-managed application metadata is enforced as read-only at installation time, overriding any application-level settings to prevent your customizations.

## Auto upgrade failure resolutions

If an auto-upgrade installation fails, the system includes retry logic within the batch orchestration process. Depending on the failure, the system may automatically schedule a retry operation. If automatic retry does not resolve the issue, check the following areas:

-   Verify that the instance is not in a blackout window or explicit instance upgrade schedule during the scheduled installation time.
-   Check the status of auto-upgrade tasks to understand the progress and outcome of installations. Task status values indicate the stage of the upgrade operation:
    -   Assigned: The batch install plan has been created and the task is queued for execution
    -   In Progress: The batch install plan is currently executing the application upgrade
    -   Success: The application upgrade completed successfully
    -   Failed: The application upgrade failed; review the failure details and configure retry settings if needed
-   Resolve withdrawn application errors. If an application version is withdrawn from the store before auto-upgrade installation, the system treats it as a failed installation and displays an error message indicating the application is unavailable. Check the error details to determine next steps.

**Parent Topic:**[Updating applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/application-manager/updating-apps-app-manager.md)

