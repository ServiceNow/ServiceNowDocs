---
title: Legacy - Delta loading
description: "Delta loading" is an optimized way to load an application from a Git repository.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Delta loading

"Delta loading" is an optimized way to load an application from a Git repository.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

When you switch branches and apply remote changes, the Delta loading feature makes sure only changed updates load. Rather than having to perform a full uninstall and reinstall of the application, only the changes update. This speeds and eases the process for developers and does away with the need to use all branches during development. Data stored in tables is retained during these operations, lowering the need to load demo data back into the application after a reinstall or branch change operation.

## Benefits of Delta loading

-   **Time savings**

    Typically, the longest part of an application uninstall or reinstall is dropping and creating tables. Delta loading prevents that from occurring. Depending on the size of the application, not having to drop or create tables can significantly improve an operation's completion time.

-   **Test and demo data retained**

    Tables that contain test and demo data are no longer deleted, so data is not lost. Developers can save time if they don't need to reimport demo data each time.

-   **Cross-scope dependent references preserved**

    Items that are cross-scoped and share references are no longer lost when you apply changes. This used to occur when an item in scope B was associated to a parent item in scope A. Applying remote changes on scope A would delete the parent item and reinstall it, breaking the reference between both items, but not restoring that relationship. Delta loading prevents the uninstall, so the reference is not lost.

-   **Recommended practice**

    Delta loading is enabled by default on all instances starting with the ServiceNow Paris release. The feature is designed to help in application development and receives continued support and upgrades.


**Parent Topic:**[Legacy - Source Control integration](c_SourceControlIntegration.md)

