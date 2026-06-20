---
title: Add CMDB tables or classes for impact calculation
description: Add the CMDB tables that contain application services to be considered during impact calculation, helping ensure accurate and relevant impact results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/add-cmdb-tables-impact-cal.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Add CMDB tables or classes for impact calculation

Add the CMDB tables that contain application services to be considered during impact calculation, helping ensure accurate and relevant impact results.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Organizations may have a vast number of CMDB tables—or classes—such as cmdb\_ci\_service\_by\_tags, cmdb\_ci\_service\_auto and many others. However, not all of these are required for impact calculation. To streamline analysis and avoid processing irrelevant data, you can selectively add or remove only those CMDB classes that represent critical infrastructure or components. The procedure below shows how to add a CMDB class. If you want to remove any CMDB table from the list, see [Remove CMDB tables or classes from impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/remove-cmdb-tables-impact-cal.md).

When you add a CMDB class, all application services related to that class are considered for impact calculation. However, if you do not want to include all services of a specific class and only want to select specific ones, you can do so on the Impact Filter Services page. For more information on how to include or exclude a service, see [Add application services for impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/add-impact-cal-services.md).

## Procedure

1.  Navigate to **All** and search for `em_impact_inclusion_class.list`.

    The Impact Inclusion Classes page opens, displaying a list of CMDB classes that are included in impact calculation.

    \[Omitted image "em-impact-cal-cmdb-tables-list.png"\] Alt text: A list of CMDB classes that are included in impact calculation.

2.  Select **New**.

    \[Omitted image "em-impact-cal-cmdb-tables-new.png"\] Alt text: The Impact Inclusion Class page.

3.  From the **Table** field, select a CMDB table.

    **Note:** The list contains only the CMDB tables supported for impact calculation, not all CMDB tables.

    \[Omitted image "em-impact-cal-cmdb-table-selection.png"\] Alt text: List of CMDB tables to select from.

    \[Omitted image "em-impact-cal-cmdb-tables-selected.png"\] Alt text: A table selected to be included in the list.

4.  Select **Submit**.

    The CMDB table adds to the list of impact inclusion classes.

    \[Omitted image "em-impact-cal-cmdb-tables-added.png"\] Alt text: The selected table is added to the list.


