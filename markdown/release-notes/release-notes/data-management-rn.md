---
title: Data Management release notes
description: The ServiceNow Data Management capabilities enable you to manage the growth of data in your instance. Data Management capabilities were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Data Management release notes

The ServiceNow® Data Management capabilities enable you to manage the growth of data in your instance. Data Management capabilities were enhanced and updated in the Yokohama release.

## Data Management highlights for the Yokohama release

-   View insights into storage consumption on your instance and implement data management policies directly from the Data Management Console.
-   Automatically delete older or unwanted records with improved table cleaner scalability.

See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

## Important information for upgrading Data Management to Yokohama

-   After upgrading a self-hosted instance to Yokohama, the sys\_physical\_table\_stats table doesn't display the latest data for table size, with the sample\_period\_start column showing dates prior to the upgrade. To see the correct table size, you can set the com.glide.stats.storage\_disk\_usage.information\_schema system property to true, which allows the statsGatherer job to use the information schema to generate the required database statistics.

-   A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

## New in the Yokohama release

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    View a summary of storage consumption on your instance and manage the growth of data directly from the Data Management Console.

-   **[Table cleaner scalability improvements](https://www.servicenow.com/docs/access?context=deleting-older-records&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Automatically delete older or unwanted records at scale.


## Changed in this release

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    You can now access data usage on your instance by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**.


## Activation information

Data Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

