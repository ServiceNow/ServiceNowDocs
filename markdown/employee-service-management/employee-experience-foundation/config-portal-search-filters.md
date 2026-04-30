---
title: Configure topic search filter
description: Customize search experiences for different portals by configuring the search application and filters.​
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search for Curated Experiences, Setup search experience, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure topic search filter

Customize search experiences for different portals by configuring the search application and filters.​

## Before you begin

Role required: Admin

## About this task

You can configure the Topic content widget for a portal-specific search application. Using this, when a Topic page is opened in a portal the same search application and search filter are being applied.

-   Configure portal-specific search applications for the Topic search widget.
-   Customize search filters and settings for each portal while using cloned topic pages or portals.
-   Improve overall search efficiency as search settings are inherited from the portal context.
-   Deliver search results that are consistent with the portal-specific search settings.

## Procedure

1.  Navigate to **Content Taxonomy** &gt; **Topic Search Configuration**.

2.  Click **New** or open an existing record.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Portal|Name of the portal `Employee Center`.|
    |Application|Name of the application `Global`.|
    |Widget instance|Topic content widget instance, for example, `ESC Topic Page`. In the lookup, add filter condition \( widget=Topic content\) to filter the topic content widget instances.|
    |Search application|Default search application, for example, `ESC Portal Search Application`.|
    |Search filter|List of active search filters based on the search application such as ESC Portal catalogs, ESC Portal Knowledge bases, and Guided Self-Service.|
    |Active|Active indicates the status of the topic search configuration.|
    |Order|Order in which the items are sorted and displayed. Default value:100.|

4.  Click **Save**.

    Topic search is now configured.


## Result

Based on this configuration, your employees can filter content by Search Filter and view results specific to portal and topic search results. For example, when you select ESC portal catalogs as a filter, employees can filter and view the catalogs only.

