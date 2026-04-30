---
title: Spotlight interactive analysis
description: Spotlight interactive analysis shows the key results of a Spotlight job. Access the analysis from a Spotlight Group record.
locale: en-US
release: xanadu
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Ranking records with Spotlight, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Spotlight interactive analysis

Spotlight interactive analysis shows the key results of a Spotlight job. Access the analysis from a Spotlight Group record.

To open the Spotlight interactive analysis, open the Spotlight Group record for the group of interest and click the **Launch Interactive Analysis** related link. The pa\_spotlight or admin role is necessary.

**Note:** Interactive analysis uses the Spotlight database view. Spotlight creates the database view for each Spotlight group when you create the group. If the database view is missing, a warning appears. If you have the pa\_spotlight or admin roles, a link also appears for generating a database view. For more information, see [Spotlight database views](spotlight-analyzing-data.md).

Using interactive analysis with any table other than incident requires fully enabled, subscription version of Performance Analytics. See [Activating your Performance Analytics subscription](c_PremiumPerformanceAnalytics.md#).

Interactive Analysis contains the following information:

-   The number of Spotlight records. This value is also the number of corresponding fact table records that exceeded the Spotlight Group threshold.
-   The number of unassigned facts table records that exceeded the Spotlight threshold. These records have no value in the Assigned To column.
-   The database view that joins the Spotlight table with the facts table of the main indicator. Each row of this view shows the columns from a Spotlight record and the corresponding facts table record.

    **Note:**

    -   If a user cannot see the values in this table, ensure that they have the itil role.
    -   If domain separation is enabled, a user can only see Spotlights records for corresponding fact table records that are included in their domains.
    -   You can create reports by using this database view as a data source. You can include these reports in dashboards. Each of the Analytics and Reporting Spotlight Solutions includes such a dashboard and reports.
    For more information, see [Spotlight database views](spotlight-analyzing-data.md).


You can apply interactive filters to the analysis. The following filters are available, for facts tables with the matching columns:

-   The **Priority** of the facts table record \(tasks only\)
-   When the record was **Opened**
-   The **Age** of the record
-   The **Assignment Group** \(tasks only\)
-   The **State** that the record is in

For information about adding or removing any of these filters, see [Add a filter to Interactive Analysis](../../dashboards/task/add-filter-to-ia.md) and [Remove a filter from Interactive Analysis](../../dashboards/task/remove-filter-from-ia.md).

**Note:** If you create an interactive filter for a Spotlight interactive analysis, the filter must be created on top of the relevant Spotlight database view. The admin role is necessary to access the database view. If you do not have this role, contact your system administrator.

To share the interactive analysis, share the URL from the Filter Info. The user with whom you share the interactive analysis must have the pa\_spotlight\_viewer role. For more information about the Filter Info, see [Interactive Analysis information panel](../../dashboards/concept/interactive-analysis-info-panel.md#).

**Parent Topic:**[Ranking records with Spotlight](spotlight.md)

