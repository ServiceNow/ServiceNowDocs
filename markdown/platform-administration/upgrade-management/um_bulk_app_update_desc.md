---
title: Bulk application updates
description: The bulk application update console enables you to review, select, and update multiple applications in a single workflow, improving efficiency compared to updating applications individually through the Application Manager.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/upgrade-management/um\_bulk\_app\_update\_desc.html
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Bulk application updates

The bulk application update console enables you to review, select, and update multiple applications in a single workflow, improving efficiency compared to updating applications individually through the Application Manager.

## Benefits

As the number of applications and plugins in your ServiceNow instance increases, updating them individually through the Application Manager becomes increasingly time-consuming. The traditional method requires you to navigate to the Application Manager, search for each application, check the available version, and perform the installation one by one. This repetitive process is cumbersome and inefficient.

The bulk application update provides you a one-stop experience where you can:

-   View all available application updates at once
-   Select multiple applications to update in a single operation
-   Preview changes and validate compatibility before applying updates
-   Schedule updates for a future time to minimize system disruption

## Performance considerations

Update duration depends on the number of applications selected for update:

-   4–5 applications: Approximately 5 minutes
-   200+ applications: Significantly longer \(allow additional time\)

Compatibility checks and test execution also extend update time, as the system downloads application packages and processes test results. Plan update operations during maintenance windows or off-peak hours when possible to minimize user impact.

## When to use bulk updates vs. Application Manager

Use the bulk application update console when:

-   You need to update multiple applications at once
-   You want to preview and validate all changes before committing to any updates
-   You need to schedule updates for a specific time
-   You want to run automated tests on updates before they are applied

Use Application Manager when:

-   You need to update a single application
-   You want to install new applications or plugins
-   You need detailed information about an application's features or dependencies

-   **[Update multiple applications at once](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-bulk-app-update.md)**  
Use the bulk application update console to review, select, and update multiple applications in a single workflow instead of updating them individually through the app manager.

**Parent Topic:**[Configuring Upgrade Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-configure.md)

**Related topics**  


[Access guided upgrade on a non-production instance]()

[Access guided upgrade on a production instance]()

