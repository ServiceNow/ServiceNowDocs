---
title: Available interactive filter UI control types
description: The interactive filter UI control type field provides several options for displaying the filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/core-ui-interactive-filters/r\_HomepagePublisherUIControlTypes.html
release: zurich
product: Core UI Interactive Filters
classification: core-ui-interactive-filters
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Available interactive filter UI control types

The interactive filter **UI control type** field provides several options for displaying the filter.

|UI control type|Description|
|---------------|-----------|
|Radio Buttons|Displays each filtering option as a radio button. Users can select only one radio button at a time.|
|Check boxes|Displays each filtering option as a check box. Users can select any number of check boxes at a time.|
|Select Single Input|Displays the filtering options as a choice list. Users can select only one choice at a time.|
|Select Multiple Input|Displays the filtering options as a choice list. Users can select any number of choices at a time. Click the X next to a selected choice to deselect that choice.|

**Note:**

Filtering behavior depends on the filter type when selecting multiple values using the **Check boxes** or **Select Multiple Input** control types. Choice filters use an AND query, meaning records must match all conditions. Date and reference filters use an OR query, meaning records must match at least one of the specified conditions.

A filter may be converted from the **Check boxes** to the **Select Multiple Input** control type for performance reasons.

**Parent Topic:**[Creating Interactive Filters of different types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/core-ui-interactive-filters/r_AvailableHomepagePublisherTypes.md)

