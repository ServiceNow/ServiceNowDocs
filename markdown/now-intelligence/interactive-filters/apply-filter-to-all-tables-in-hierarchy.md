---
title: Interactive filters on database views and table hierarchies
description: When you create an interactive filter on an extended table, you can also apply the filter to database views and to the other tables in the hierarchy. The hierarchy includes all parent, child, and sibling tables.
locale: en-US
release: yokohama
product: Interactive Filters
classification: interactive-filters
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interactive filters on database views and table hierarchies

When you create an interactive filter on an extended table, you can also apply the filter to database views and to the other tables in the hierarchy. The hierarchy includes all parent, child, and sibling tables.

When you create an interactive filter, you can:

-   **Select __All tables in the hierarchy__.**

    If the source table is incident, then the interactive filter applies to incident; its parent table, task; and to all of its sibling tables, including problem and change.

    Specify any possible targets in the **Interactive Filter References** section for this selection to be respected.

-   **Select __Apply filter to both [database views](../../performance-analytics/concept/performance-analytics-glossary.md#) and tables__.**

    If the source table is incident, then the interactive filter applies to both incident and, for example, the \[incident\_sla\] database view.

    Specify any possible targets in the **Interactive Filter References** section for this selection to be respected.

-   **Select both check boxes.**

    The interactive filter applies to all tables in the hierarchy and to database views.

-   **Select neither check box.**

    Interactive filters apply only to the source table, such as incident.

    **Note:** This is the default setting when you create an interactive filter.


![Apply Interactive Filter to hierarchy](../image/apply-if-to-hierarchy-db-views2.png)

Interactive filters applied to extended tables also apply to the other tables in the hierarchy.

**Note:** Interactive filters on a database view do not apply automatically to the siblings of the database view's source table. For example, \[problem\_sla\] is a database view created on the table \[task\_problem\]. Interactive filters applied to \[problem\_sla\] do not apply automatically to widgets based on the \[task\_change\] table, a sibling of \[task\_problem\], even if you have selected both options.

**Parent Topic:**[Creating Interactive Filters of different types](../../dashboards/reference/r_AvailableHomepagePublisherTypes.md)

