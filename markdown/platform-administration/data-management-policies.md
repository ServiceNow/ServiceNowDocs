---
title: Managing the growth of data on your instance
description: Manage the growth and storage of data on your instance using data management policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/data-management-policies.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing the growth of data on your instance

Manage the growth and storage of data on your instance using data management policies.

## Overview of managing data growth

Data management policies streamline administration by allowing you to define multiple archive and table cleaner rules for a table within a single policy record. Additionally, you can easily activate or deactivate all rules simultaneously from the data management policy record.

-   [Create a data management policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/create-data-management-policy.md)

    Create a data management policy for any table that accumulates data that you want to archive or delete periodically.

-   [Create an archive rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_CreateAnArchiveRule.md)

    Move records in a primary table to an archive table, including any records in other tables that reference those records.

-   [Create a table cleanup rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/activate-table-cleanup.md)

    Prevent data from growing exponentially by implementing table cleanup rules.

-   [Activate database rotation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_ActivateDatabaseRotation.md)

    Preserve instance performance and mitigate risks associated with querying growing data sets.


-   **[Create a data management policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/create-data-management-policy.md)**  
Define a set of rules for managing table data on your instance.
-   **[Archiving records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/archiving-older-records.md)**  
Manage table size growth and improve query performance by archiving records.
-   **[Deleting older or unwanted records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/deleting-older-records.md)**  
Delete older, expired, or unwanted records from tables automatically.
-   **[Applying database rotation techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_DatabaseRotation.md)**  
Manage table size growth, archive data, and boost query performance by configuring database rotation.

**Parent Topic:**[Data Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_DataManagement.md)

