---
title: Example: Field mapping
description: The Category breakdown maps the Category field on the incident table to the Incident.Category breakdown source, which references the Choices\[sys\_choice\_list\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/example-field-mapping.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a breakdown mapping on a breakdown record, Automated breakdowns, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Example: Field mapping

The Category breakdown maps the **Category** field on the incident table to the Incident.Category breakdown source, which references the Choices\[sys\_choice\_list\] table.

In the first image, you see the Category breakdown with the Incident.Category breakdown source. This breakdown has a breakdown mapping to the **Category** field on the incident table.

\[Omitted image "assignment-group-breakdown.png"\] Alt text: Category breakdown form showing breakdown source of Incident.Category and mapping to the category field on the incident table

The Incident.Category breakdown source uses records in the Choices\[sys\_choice\_list\] table.

\[Omitted image "CreatingBreakdownSourcesExample.png"\] Alt text: The filled out breakdown source form for Incident.Category, showing facts table, field, and conditions

The next image shows the Choice \[sys\_choice\] table records that meet the conditions that are specified in the Incident.Category breakdown source. Note the Label field values.

\[Omitted image "choices-table-category-element.png"\] Alt text: Filtered choice table records corresponding to breakdown source example.

Finally, you see the Category field of some records on the Incidents table. This field is mapped to the Category breakdown. The field values match the Label fields of the records of the Choices\[sys\_choice\_list\] table that the Incident.Category breakdown source filters for.

\[Omitted image "incident-table-category.png"\] Alt text: Category fields of Incident records. Field values match the Label field on the Choices table, to which the Category field is mapped.

**Parent Topic:**[Create a breakdown mapping on a breakdown record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/t_CrtBkdnBreakdownMpngs.md)

