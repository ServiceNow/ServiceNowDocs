---
title: Example: Field mapping
description: The Category breakdown maps the Category field on the incident table to the Incident.Category breakdown source, which references the Choices\[sys\_choice\_list\] table.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a breakdown mapping on a breakdown record, Automated breakdowns, Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Example: Field mapping

The Category breakdown maps the **Category** field on the incident table to the Incident.Category breakdown source, which references the Choices\[sys\_choice\_list\] table.

In the first image, you see the Category breakdown with the Incident.Category breakdown source. This breakdown has a breakdown mapping to the **Category** field on the incident table.

![Category breakdown form showing breakdown source of Incident.Category and mapping to the category field on the incident table](../image/assignment-group-breakdown.png)

The Incident.Category breakdown source uses records in the Choices\[sys\_choice\_list\] table.

![The filled out breakdown source form for Incident.Category, showing facts table, field, and conditions](../image/CreatingBreakdownSourcesExample.png)

The next image shows the Choice \[sys\_choice\] table records that meet the conditions that are specified in the Incident.Category breakdown source. Note the Label field values.

![Filtered choice table records corresponding to breakdown source example.](../image/choices-table-category-element.png)

Finally, you see the Category field of some records on the Incidents table. This field is mapped to the Category breakdown. The field values match the Label fields of the records of the Choices\[sys\_choice\_list\] table that the Incident.Category breakdown source filters for.

![Category fields of Incident records. Field values match the Label field on the Choices table, to which the Category field is mapped.](../image/incident-table-category.png)

**Parent Topic:**[Create a breakdown mapping on a breakdown record](../task/t_CrtBkdnBreakdownMpngs.md)

